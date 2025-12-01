
sudo apt update

sudo apt-get install docker.io

sudo apt install git

sudo apt install nano

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Hello from AWS</h1>
</body>
</html>

open gitbash

git init

git add.

Git commit -m "first commit"

create git repo in github

git branch -M main

git remote add origin <https url>

git push -u origin main

can see file in git repo

copy http path

git clone<copied http url>   (cmd powershell thing)

cd Aws

ls

Nano Dockerfile

FROM nginx:alpine

COPY ./usr/share/nginx/html

sudo docker build -t mywebapp .

sudo  docker run -d -p 80:80 mywebapp

go to instance and copy ipv4 address and paste it in browser


sudo docker ps

sudo docker stop<container-id>

then terminate instance and end lab