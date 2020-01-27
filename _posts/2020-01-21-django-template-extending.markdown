---
layout: post
title:  "Template Extending"
date:   2020-01-21 17:00:00 +0900
categories: jekyll update
---
# 개요


# Template
## base.html
모든 화면에서 Navbar와 Sticky footer를 공통으로 사용한다.

공통으로 사용할 부분만 코드를 작성하고 바뀔 부분은 {% raw %} {% block name %} {% endraw %} 과 {% raw %} {% endblock %} {% endraw %} 으로 감싸준다.

```html
<!DOCTYPE html>
<html lang="ko">

<head>
  <!-- Required meta tags -->
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

  <!-- CSS -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css"
    integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">

  <title>Blog</title>
</head>

<body>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <a class="navbar-brand" href="#">Hwang's Blog</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item active">
          <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Portfolio</a>
        </li>
      </ul>
      <form class="form-inline my-2 my-lg-0">
        <div class="input-group mb-0">
          <input type="text" class="form-control" placeholder="Search" aria-label="Search"
            aria-describedby="basic-addon2">
          <div class="input-group-append">
            <button class="btn btn-outline-light" type="button">Search</button>
          </div>
        </div>
      </form>
    </div>
  </nav>

  {% raw %} {% block content %} {% endraw %}
  {% raw %} {% endblock %} {% endraw %}

  <footer id="sticky-footer" class="py-4 bg-light text-black-50">
    <div class="container text-center">
      <small>Copyright &copy; hwangsb.github.io</small>
    </div>
  </footer>

  <!-- JavaScript -->
  <script src="https://code.jquery.com/jquery-3.4.1.slim.min.js"
    integrity="sha384-J6qa4849blE2+poT4WnyKhv5vZF5SrPo0iEjwBvKU7imGFAV0wwj1yYfoRSJoZ+n"
    crossorigin="anonymous"></script>
  <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js"
    integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo"
    crossorigin="anonymous"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js"
    integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6"
    crossorigin="anonymous"></script>
</body>

</html>
```


## home.html


# Development Environment

| Type | OS | IDE | Language | Framework | Library |
|:--|:--:|:--:|:--:|:--:|:--:|
| Name | Windows 10 64bit | Visual Studio Code | Python | Django | Bootstrap |
| Version | 1909 | 1.41.1 | 3.8.1 | 3.0.2 | 4.4.1 |
| Build | 18363.418 |
