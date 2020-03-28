## First Web App on `nginx`

1. Create a sample `webapp.html`.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sample Web App </title>
</head>
<body>
    This is a sample web page.
</body>
</html>
```
2. Write  the ```nginx.conf``` file to tell server the configs.

```apacheconf
server {
    root /www;
}
```

3. Write the Dockerfile.

```Dockerfile
FROM nginx:latest

ADD index.html /www/
# ADD does the decompressing part tool if there are .zip file.
# We can also use COPY command.

ADD nginx.conf /etc/nginx/conf.d/default.conf

# Exposing the port
EXPOSE 80
EXPOSE 443

# Semicolon is required here.
CMD nginx -g "daemon off;"

```

4. Build the image.
```sh
docker build -t webapp:latest
```

5. Run the docker image.
```sh
docker run webapp
```