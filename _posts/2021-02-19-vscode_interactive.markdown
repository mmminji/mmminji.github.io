---
layout: post
title:  "VSCode 설정하기"
date:   2021-02-19 17:39:07
categories: VisualStudioCode Settings
---
알아두면 편리한 설정

내가 VSCode에서 실제로 사용하는 몇 가지 기능들을 소개하려고 한다.

## 1. line-by-line 실행

`.py`파일을 jupyter notebook처럼 line-by-line으로 실행시킬 수 있다.

가장 흔히 사용되는 방법은 코드 위에 주석 형태로 `#%%`를 입력하는 것이다. 

![](https://github.com/mmminji/mmminji.github.io/blob/main/assets/post_pics/cell.PNG?raw=true){: width="600" height="300"}

Shift + Enter 를 누루면 `#%%`와 다음 `#%%` 사이의 코드들을 실행시켜준다. 이 방법은 실행시키고 싶을 때마다 `#%%`를 입력해야 한다는 번거로움이 존재한다.  
그래서 주석없이 드래그한 코드를 실행시킬 수 있는 방법이 있다.

Ctrl + Shift + p -> Preferences: Open Settings (JSON) 에서 아래 코드를 추가해주면 된다.

```python
"jupyter.sendSelectionToInteractiveWindow": true,
"jupyter.interactiveWindowMode": "perFile"
```

그러면 주석없이도 내가 원하는 코드만큼 드래그한 후 Shift + Enter를 누르면 코드를 실행시킬 수 있다.

