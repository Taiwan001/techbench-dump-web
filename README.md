# techbench-dump-web
An easy to use website to generate links for Microsoft products.

The official website can be found here: https://techbench.luzea.ovh

## Installation
```
cd /var/www/html <-- your website root
git clone https://github.com/luzeagithub/techbench-dump-web.git .
wget https://techbench.luzea.ovh/dump.json
```

You can download regulary updated dumps using the link from above or generate them yourself using [techbench-json-dump](https://github.com/luzeagithub/techbench-json-dump).

You also want to rewrite the URLs so that without specifying the `.html` file extension, HTML files are still loaded and no error 404 occurs. If you're using NGINX, add this to your site configuration:
```
location / {
    try_files $uri $uri.html $uri/ =404;
}
```
Apache is also capable of rewriting URLs.

## Contributing
Yes, please. Fork this repository and start working. After you are done with it, submit a pull request and I will review your changes.

## License
This project is licensed under the [MIT License](LICENSE).
