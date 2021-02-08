---
layout: post
title: "TIL(3)_django에 css 적용하기"
date: 2021-02-07T14:25:52-05:00
author: HyeongJune Lee
categories: TIL
---

하.. 글을적기전부터 정말 힘들었다..
별것 아닌걸수도 있는데 위의 제목처럼 django에 css적용하기,,,

이방법 구글링하면 수도없이 많이 나온다.
하지만 이방법 저방법 왠지는 모르겠지만 전혀 적용이 안되서 힘들었다.

그래서 됐던 방법은 이러하다.

1. setting.py에

```{.python}
    STATIC_URL = '/static/'
    STATICFILES_DIRS = [
        os.path.join(BASE_DIR, 'static'),
    ]
```

이렇게 적어줄것!

2. 나의 프로젝트 디렉터리에 static이란 디렉터리를 생성한후 css파일들을 넣어준다.

3. css파일이 들어갈 base.html의 css경로에 /static/style.css를적어준다.

구글링을 하며 본것중 {% load static %} {% static '~~~~' %}등의 방법이 있었는데
이방법은 일단 개인프로젝트가 끝난후 제대로 적용시켜봐야겠다.
