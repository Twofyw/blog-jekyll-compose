# blog-jekyll-compose

Before building your blog, you can generate a new site by running the following `docker run`(create the directory manually to avoid permission conflict between the host and docker). Don't forget to change the UID and proxy environment variable if you are not me :).

```
docker run --rm -v $(pwd)/jekyll/site:/srv/jekyll -v $(pwd)/jekyll/bundle:/usr/local/bundle -e JEKYLL_UID=50011 -e HTTP_PROXY="http://172.17.0.1:8118" -e HTTPS_PROXY="http://172.17.0.1:8118" -it jekyll/builder jekyll new .
```
