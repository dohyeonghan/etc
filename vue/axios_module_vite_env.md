# main.js와 quasar

## main.js
: main.js는 프로그램의 진입점이다.

## quasar의 main.js 
: quasar의 main.js는 boot file로 대체된다.

# VITE에서 환경변수 설정하기
- 루트폴더에 .env 파일, .env.development 파일 생성
- .env가 기본으로 들어가고, dev 환경일 경우 development 파일이 덮어쓴다.
- .env를 prod로 지정하면 될듯
- vite.config.js에서 mode가 안나와있는데, npm run dev로 실행하므로 development 버전이 기본으로 설정되어 있다. prod로 바꾸고 싶으면 mode: 'production'으로 지정해주면 된다. 




