# RE: 유튜브 임베드 문제 해결 가이드

## 현재 사용 중인 영상 ID 목록
- 메인 가이드 (vikv9VoZ1vs)
- Groq API 발급 (Jc2WmLiXyjg)
- GPT-4o-mini API 발급 (u9Aplb30JPE)

## 체크리스트
- [x] HTTPS 사용
- [x] `/embed/VIDEO_ID` 형식 사용
- [x] 반응형 래퍼 적용
- [x] loading="lazy" 적용
- [ ] 테스트 페이지 확인

## 표준 임베드 코드
```html
<iframe 
    src="https://www.youtube.com/embed/VIDEO_ID" 
    title="YouTube video player" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    allowfullscreen
    loading="lazy">
</iframe>
```

## 반응형 래퍼
```html
<div style="position:relative;width:100%;padding-top:56.25%;">
  <iframe
    src="https://www.youtube.com/embed/VIDEO_ID"
    style="position:absolute;inset:0;width:100%;height:100%;border:0;"
    title="YouTube video player"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen
    loading="lazy">
  </iframe>
</div>
```

## 문제 발생 시 대체 방법
1. `?si=` 파라미터 추가 시도
2. `youtube-nocookie.com` 사용
3. F12 콘솔에서 에러 확인
4. 테스트 페이지(test-youtube-embed.html)에서 확인
