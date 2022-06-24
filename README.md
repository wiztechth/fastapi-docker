# fastapi-docker

This is code sniplet from Wiztechth's channel on Youbute, https://youtu.be/vO-mrQV-tD0

### How to clone and build container image
```Shell
git clone https://github.com/wiztechth/fastapi.git

# build docker image
cd fastapi-docker
build -t myapi .
```

### How to run
```Shell
# ไปที่ fastapi direcotry
cd fastapi

# run dokcer พร้อม option ในการ mount host directory ไปยัง /code/app ของ container
docker run -it -p 80:80 --mount src="$(pwd)",target=/code/app,type=bind myapi

# then use the browser and goto http://127.0.0.1/hello/Wiztech
```
