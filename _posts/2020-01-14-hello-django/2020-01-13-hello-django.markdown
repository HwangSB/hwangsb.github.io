---
layout: post
title:  "Hello Django!"
date:   2020-01-14 17:00:00 +0900
categories: jekyll update
---
# 환경설정
## Python venv 생성
프로젝트 폴더에 venv(Virtual Environment)를 만든다.

`python3 -m venv [directory_name]`

```console
python3 -m venv venv
```

현재 폴더에 venv를 활성화 시킨다.

```console
venv/Scripts/activate.bat
```


# Django 시작하기
## Django 설치
pip 명령을 사용하여 Django를 설치한다.

```console
pip install django
```


## Django 프로젝트 생성
Django Project를 생성한다.

`django-admin startproject [project_name]`

```console
django-admin startproject django_project
```


## Django 서버 실행
프로젝트 생성 후 동작을 확인한다.

```console
cd django_project
python manage.py runserver
```

| ![image](hello_django_0.png) |
|:--:|
| 127.0.0.1:8000으로 접속한 모습 |

`Ctrl + C`로 종료할 수 있다.


## Django 앱 생성
Django App을 생성한다.

`python manage.py startapp [app_name]`

```console
python manage.py startapp django_app
```


## 홈페이지 만들기
Django App 폴더 안에 templates 폴더를 만들고 home.html 파일을 추가한다.


# 참고
[Django 설치하기][https://tutorial.djangogirls.org/ko/django_installation/]

[나의 첫 번째 Django 프로젝트!][https://tutorial.djangogirls.org/ko/django_start_project/]

[파이썬 웹프로그래밍 - 장고(Django)설치][https://offbyone.tistory.com/77]
