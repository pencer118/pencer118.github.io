---
date: 2021-06-08
layout: post
title: 몽고디비 설치 및 설정
  
image: https://res.cloudinary.com/dm7h7e8xj/image/upload/v1559822138/theme9_v273a9.jpg
optimized_image: https://res.cloudinary.com/dm7h7e8xj/image/upload/c_scale,w_380/v1559822138/theme9_v273a9.jpg
category: Mongo
tags:
  - 몽고
  - 디비
  - mongo
  - db
author: SUB
paginate: true
---

## 1. centos에 설치

>공식 배포 사이트에서 OS 별로 받을 수 있는 버전을 제공하고 있습니다.

https://fastdl.mongodb.org

>설치할 버전을 선택한 후 wget 명령어로 다운 받습니다.

$ wget https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-rhel70-4.0.18.tgz

>tar 명령어로 압축을 해제합니다.

$ tar xvfz mongodb-linux-x86_64-rhel70-4.0.18.tgz

>mongodb에 적용할 설정파일을 미리 작성합니다.

$ vi /etc/mongodb.conf

```js
// 설정 이미지 가져오기

// Create a function that takes two arguments and returns the sum of those arguments
var adder = new Function("a", "b", "return a + b");

// Call the function
adder(2, 6);
// > 8
```

>설정 파일에 입력한 디렉터리를 생성합니다.

$ mkdir /usr/local/mongodb

$ mkdir /var/log/mongodb

>mongodb를 실행합니다.

$ /usr/local/src/mongodb-linux-x86_64-rhel70-4.0.18/bin/mongod -config /etc/mongodb.conf

>mongo 명령어로 MongoDB 쉘에 접속할 수 있습니다.

$ /usr/local/src/mongodb-linux-x86_64-rhel70-4.0.18/bin/mongo 

>편리하게 사용하기 위해 환경 변수를 등록합니다.

$ vi /root/bash_profile

