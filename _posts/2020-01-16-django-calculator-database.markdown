---
layout: post
title:  "Add Calculation History Feature"
date:   2020-01-16 17:00:00 +0900
categories: jekyll update
---
# 계산 기록 추가하기
## 개요
계산 기록을 CRUD(Create Read Update Delete) 하는 기능을 추가한다.


## models.py
수식과 답을 저장할 데이터베이스 형식을 python class로 구현할 수 있다.

models.Model을 상속받는 Expression class 생성한다.

```python
# some python code
```


## 데이터 migration 생성 & migrate
```zsh
python manage.py makemigration
python manage.py migrate
```


## views.py
데이터베이스에 저장된 객체를 읽어 home.html에 paramater로 전달한다.(Read)

```python
# some python code
```

입력한 수식을 데이터베이스에 저장한다.(Create)

```python
# some python code
```

리스트의 수식들 중 삭제 버튼이 눌린 식을 데이터베이스에서 삭제한다.(Delete)

```python
# some python code
```

리스트의 수식들 중 수정 버튼이 눌린 식을 1 + 1 로, 답을 2로 수정한다.(Update)

```python
# some python code
```


## home.html
```html
<!-- some html code -->
```


## update-history.html
```html
<!-- some html code -->
```


## delete-history.html
```html
<!-- some html code -->
```


# Development Environment

| Type | OS | IDE | Language | Framework |
|:--|:--:|:--:|:--:|:--:|
| Name | Windows 10 64bit | Visual Studio Code | Python | Django |
| Version | 1909 | 1.41.1 | 3.8.1 | 3.0.2 |
| Build | 18363.418 |
