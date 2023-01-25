## Firebase App Distribution CD 구축

작성자: 성빈  
유형: 자동화  
마일스톤: 이 DEEP 이 승인되고 3일 내로 완성  
마지막 수정일: 2023. 01. 25.

### 요약

`develop` 브런치로 PR 이 올라올 때마다 앱을 빌드하여 Firebase App Distribution 으로 배포합니다.

### 필요한 이유

새로운 피쳐가 개발돼 PR 이 올라오면 해당 피쳐가 제대로 작동하고 UI 가 디자인과 일치하는지 확인 후 approve 해야 합니다. 이를 확인하기 위해 앱을 빌드하여 실행해 보는 과정이 필요한데, 매번 로컬로 pull 하여 빌드하는 작업은 번거롭고 귀찮습니다. 이 귀찮은 과정을 자동화하여 우리의 생산성을 높이고자 합니다.

### 목표

- 앱 서명 키 생성
- PR 이 올라오면 앱이 제대로 빌드되는지 확인하는 CI 추가
- 위 CI 에 성공했고 `deploy` label 이 붙어있다면 해당 PR 로 빌드된 apk 를 `local-app-tester` group 에 배포
- 성공적으로 배포되면 디스코드와 해당 PR 에 메시지 남김

### 비 목표

- app version-code 자동 조정
- app version-name 자동 수정

### 계획

1. 던던 파이어베이스를 만듭니다.
2. App Distribution 을 활성화합니다.
3. 던던 안드로이드 개발팀과 실시간 앱 테스트에 희망하는 팀원분을  `local-app-tester` group 에 초대합니다.
4. PR 이 올라오면 `./gradlew build` 를 통해 앱이 정상적으로 빌드되는지 확인합니다.
5. 4번 과정에 성공했다면 `local-app-tester` group 에 빌드된 apk 를 배포합니다.

### 논의 사항

앱이 정상적으로 설치되기 위해선 release 로 빌드하고 배포해야 합니다. 이를 위해 앱 서명 키를 생성하려고 합니다.
