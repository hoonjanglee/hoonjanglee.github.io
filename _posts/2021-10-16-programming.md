---
layout: post
title: GA 추가 및 tag 기능 추가
tags: [programming]
---

### Google analytics 추가
 페이지의 트레킹을 확인하고 싶어서 google analytics를 이용하기로 했다. 먼저 lanyon 테마에 적용할 수 있는 google analytics는 유니버셜 계정 (UA-XXXX-X)을 만들어주어야 한다.
 구글 애널리틱스 회원가입을 해준 다음에 "Property Settings" -> ** Admin ** -> Property column 에 들어가서 Property Setting을 확인해주면 Tracking id에 들어가서 본인의 아이디를 확인할 수 있다.

 그렇게 Github blog의 페이지에서 _config.yml에 들어가서 
 
Custom vars
version:             1.1.0
google_analytics_id: UA-XXXX-X 

 부분에서 본인의 id를 입력하면 된다.
 그런 다음, Root page에다가 google_analytics.html이라는 파일을 만들어주고 그 안에다가 코드
 
<img width="661" alt="스크린샷 2021-10-16 오후 10 11 18" src="https://user-images.githubusercontent.com/50545088/137588910-bd7d3729-8bbc-45cc-ba57-9f1abf62bc40.png">

를 넣어주고 

마지막으로 head.html에 들어가서 
<img width="563" alt="스크린샷 2021-10-16 오후 10 02 07" src="https://user-images.githubusercontent.com/50545088/137588688-980de4fc-b415-44a7-8436-9f1ff613e8ca.png">


를 적어주고 구글 애널리틱스 페이지에 다시 들어가서 확인을 해보면 실시간 트레킹부터 유입 경로까지 확인을 할 수 있다.


### Lanyon 테마에다가 Archive, tags 만들기
#### archive 만들기
기본적으로 Lanyon 페이지에서는 Archive 기능을 제공해주지 않는다. 홈에서는 pagination으로 10개씩 볼 수 있도록 만들었지만,
글 전체를 볼 수 있도록 편하게 만드는 것도 중요하다고 생각이 되어서 Archive 페이지를 만들어주었다.
Root 에다가 archive.md 라는 파일을 만들어주고,

<img width="743" alt="스크린샷 2021-10-16 오후 10 07 05" src="https://user-images.githubusercontent.com/50545088/137588804-e68face7-f42f-4fa8-b3cf-bc47746c478c.png">
를 적어주면 된다. 이건 간단해서 pass

#### tags 만들기
tag 기능은 기본적으로 있기 떄문에 그것을 사용하였고, 페이지 상에서, [Lanyon](https://jekyllrb.com) 긁어오고 디자인적으로 안 좋은 것들만 조금 바꾸었다. 코드는 아래와 같다.

<img width="1001" alt="스크린샷 2021-10-16 오후 10 03 34" src="https://user-images.githubusercontent.com/50545088/137588754-5afb932e-6e70-4697-84b3-79b21cfee301.png">

다음과 같이 작성을 하면, 카테고리 별로 보이게 된다. 각 카테고리별로 몇개의 글이 있는지도 보여줄 수 있는 것 같은데 그건 딱히 추가하지 않았다. 아니면 괄호 안에다가 보여주게 만드는 것도 방법 일지도?

남은 것
* SEO 넣기
* 클릭해서 유튜브, 인스타그램에 바로 갈 수 있는 버튼 만들기