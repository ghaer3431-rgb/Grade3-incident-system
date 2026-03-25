공유형 Firebase 버전 안내

포함 파일
- index.html : Google 로그인 + Firestore 실시간 공유 + 삭제 확인창 포함
- vercel.json : 정적 배포 설정
- firestore.rules.example : 예시 보안 규칙
- README.txt : 설정 안내

반드시 해야 하는 설정
1. Firebase 프로젝트 생성
2. Authentication > Google 로그인 사용 설정
3. Firestore Database 생성
4. Web 앱 등록 후 Firebase config를 index.html의 FIREBASE_CONFIG에 붙여넣기
5. teacherAccounts의 email 값을 실제 교사 Google 계정 이메일로 채우기
   - 지금은 이름만 넣어둔 상태라 임시로 displayName 매칭도 허용됨
   - 실제 운영은 email 기준 권장
6. Authorized domains에 배포 도메인 추가

배포
1. 압축 풀기
2. index.html 열어서 FIREBASE_CONFIG 수정
3. vercel.com/new 접속
4. 로그인
5. 파일 업로드 후 배포

중요
- 이 버전은 여러 교사가 같은 데이터를 실시간으로 공유함
- 삭제 버튼은 확인창을 한 번 거친 뒤 삭제됨
