---
link: https://chirpy.cotes.page/
---
# About
이 블로그는 `Jekyll`(정적사이트 생성 프레임워크)의 `Chirpy`테마를 적용 해 만들었습니다.
기존 마크다운 형식의 글을 Chirpy를 통해 게시함에 있어서,
적용 되지 않는 마크다운 및 마크업 문법, Chirpy에서 지원하는 추가적인 문법들,
그리고 Chirpy를 사용함에 있어서 주의사항 등을 정리 해 두려고 합니다.
(저의 경우 마크다운 에디터로 `옵시디언`을 사용하고 있으며,
내용 상 실제 마크다운 문법이 아닌 <font color="#ff0000">옵시디언에서만 적용</font>되는 문법이 포함되어 있을 수 있습니다.)

# 포스팅 미지원 & 지원 사항
## Chirpy 미지원
### 마크다운 미지원
- 헤더5`#####`,헤더 6`######`이 적용되지 않습니다.
-  디바이더`---`가 적용되지 않습니다.

### 마크업 미지원
-  iframe을 통한 영상삽입이 지원되지 않습니다.

## Chirpy 지원
### 유튜브 영상삽입
```
{% include embed/youtube.html id='__영상ID__' %}
```
-  유튜브 영상주소(`https://www.youtube.com/watch?v=__영상ID__`) 중 `__영상ID__`부분을 위의 `__영상ID__`에 입력합니다.
- 예시) 첨부하고자 하는 유튜브 영상의 주소가`https://www.youtube.com/watch?v=dsM9IJMDe3k`일 경우
	- `{% include embed/youtube.html id='dsM9IJMDe3k' %}`

### prompt박스 삽입
#### 특이사항
- 여러 줄로 작성해도 한 줄로 들어가게 됩니다.
- 내부에서 헤더 작성시 이상해지므로 자제합니다.
#### info
![](assets/img/attachment/README.png)
```
> 내용
{: .prompt-info }
```

#### tip
![](assets/img/attachment/README-1.png)
```
> 내용
{: .prompt-tip }
```

#### warning
![](assets/img/attachment/README-2.png)
```
> 
{: .prompt-warning }
```

#### danger
![](assets/img/attachment/README-3.png)
```
> 내용
{: .prompt-danger }
```


# 깃헙배포시 유의사항
### 포스트 디렉터리 관리
- `_posts`디렉터리 내부의 디렉터리명은 가급적 영어
- chirpy는 `_posts` 디렉터리 내부의 모든 글들을 읽어오므로, 작성자는 `_posts`디렉터리 내부 구조를 원하는데로 만들 수 있습니다.
- 다만 디렉터리 명이 한글이면서 띄어쓰기가 존재하면, Github Action으로 배포까지는 문제가 없는데 제대로 정적사이트가 렌더링 되지 않는 문제가 있습니다.
