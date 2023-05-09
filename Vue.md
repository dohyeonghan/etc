
# Vue

const { data } = await getPosts() -> 구조분해 할당

async await -> promise 객체와 동일
promise 객체 -> .then(response~~~)
-> 비동기 처리

promise 객체 출력하려면 : console.dir(response) 
결과값이 object면 : 구조 분해 할당으로
const {data}

-> 구조 분해 할당으로 Object 값이 들어 가는 거 넣는 줄 모르고
data1, data2 이러고 있어서 값이 안나옴

Object에는 config, data, headers, request, status, statusText 등등 있음

const { data } = await getPosts()
posts.value = data; 로 할당할 수도 있지만

({ data: posts.value } = await getPosts())로 할당할 수도 있음


등록 개발
form 객체 생성

v-model로 엮어주기

@submit.prevent로 저장 버튼 클릭시 save 메소드 호출하도록

디테일 개발

...data로 전체 넣지 말고 필요한 것들 추려서 setPost 함수 만들어주기

수정 구현
form 객체 생성

일단 조회 getPostbyId

조회했으면 setForm으로 넣어주면 됨

v-model로 각각 바인딩
-> 데이터 불러오는 부분

수정
edit 메소드 
updatePost id, form 객체 
수정후에는 상세 페이지로 바로 이동 

삭제
detail에서 구현
remove 메서드 
props.id로 삭제
삭제후 리스트로 이동 
confirm 하나 띄우기 

if 문이 중첩되면 안티패턴
-> false면 return 
true면 로직 그대로
!도 잘 안보이니까 === false



