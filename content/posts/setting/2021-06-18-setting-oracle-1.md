---
title: "[Setting] oracle 실습 환경 준비(docker)"
date: "2021-06-18T20:40:32.169Z"
template: "post"
draft: false
slug: "setting/oracle/no1"
category: "setting"
tags:
  - "oracle"
  - "TIL/oracle"
  - "oracle11g"
  - "setting"
  - "docker"
description: "맥에서 오라클 실습 환경 준비"
---

# MAC에서 oracle 실습 환경 준비
- - - -

## 특징

맥에서 오라클을 사용할 수 없기 때문에 Docker를 이용하였음.
오라클 11g 사용


## 1. DOCKER DOWNLOAD

도커 맥 다운로드 링크 https://docs.docker.com/docker-for-mac/install/


## 2. DOCKER LOGIN

```
$ docker login
```

## 3. DOCKER에서 ORACLE 다운로드

```
$ docker search oracle-xe-11g
$ docker pull jaspeen/oracle-xe-11g
```

docker search oracle 까지만 검색해도 나옴.
마음에 드는거 pull한다

## Docker image 실행

```
$ docker run --name oracle11g-test -d -p 8888:8888 -p 1521:1521 jaspeen/oracle-xe-11g
```

oracle11g-test는 컨테이너명이기 때문에 수정해서 사용하면 됨

-d : 백그라운드 실행

-p : 호스트(host) 컴퓨터에서 컨테이너에서 리스닝하고 있는 포트로 접속할 수 있도록 설정



## 컨테이너 확인
```
$ docker ps
```
