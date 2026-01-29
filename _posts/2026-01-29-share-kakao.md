---
layout: post
title:  "카카오톡 공유하기 기능 추가하기"
categories: javascript
---

## 카카오톡 공유하기

카카오톡 공유하기 기능을 테스트하는 페이지입니다.

<script src="https://t1.kakaocdn.net/kakao_js_sdk/2.7.7/kakao.min.js" integrity="sha384-tJkjbtDbvoxO+diRuDtwRO9JXR7pjWnfjfRn5ePUpl7e7RJCxKCwwnfqUAdXh53p" crossorigin="anonymous"></script>

<script>
  Kakao.init('0f89c9f62c6d24955c061f6bb295212e');  // 사용하려는 앱의 JavaScript 키 입력
</script>

<a id="kakaotalk-sharing-btn" href="javascript:shareMessage()">
  <img src="https://developers.kakao.com/assets/img/about/logos/kakaotalksharing/kakaotalk_sharing_btn_medium.png"
    alt="카카오톡 공유 보내기 버튼" />
</a>

<script>
  function shareMessage() {
    Kakao.Share.sendDefault({
      objectType: 'feed',
      content: {
        title: '딸기 치즈 케익',
        description: '#케익 #딸기 #삼평동 #카페 #분위기 #소개팅',
        imageUrl:
          'http://k.kakaocdn.net/dn/bLPLfX/dJMcacayNt1/iWQpxLOqbqcyg2hxzKCEE1/kakaolink40_original.png',
        link: {
          // [내 애플리케이션] > [플랫폼] 에서 등록한 사이트 도메인과 일치해야 함
          mobileWebUrl: 'https://kimluffy.github.io',
          webUrl: 'https://kimluffy.github.io',
        },
      },
      social: {
        likeCount: 286,
        commentCount: 45,
        sharedCount: 845,
      },
      buttons: [
        {
          title: '웹으로 보기',
          link: {
            mobileWebUrl: 'https://kimluffy.github.io/javascript/2026/01/29/share-kakao.html',
            webUrl: 'https://kimluffy.github.io/javascript/2026/01/29/share-kakao.html',
          },
        },
        {
          title: '앱으로 보기',
          link: {
            mobileWebUrl: 'https://kimluffy.github.io/javascript/2026/01/29/share-kakao.html',
            webUrl: 'https://kimluffy.github.io/javascript/2026/01/29/share-kakao.html',
          },
        },
      ],
    });
  }
</script>