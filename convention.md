## GitHub Convention

### [예시] '1차 코드' 라는 이슈 #10이 존재하는 경우

1. **공용 브랜치 생성**
   - 작업을 시작하는 사람이 `issue10`이라는 이름의 브랜치를 생성한다.

   ```bash
   git checkout main
   git checkout -b issue10
   ```

2. **각자 작업 브랜치 생성**
   - `issue{number}_{name}`: 이슈 번호와 각자 자신의 이니셜을 포함한 브랜치를 생성하여 작업한다.
   - ex. `issue10_kh`, `issue10_cy`
   - 주의! 브랜치는 `issue10`에서 뻗어 나가야 함

   ```bash
   git checkout -b issue10_kh
   ```

3. **작업 내용 커밋 및 푸시**
   - 작업이 완료되면 변경 사항을 커밋하고, 원격 저장소에 푸시한다.
   ```bash
   git add .
   git commit -m "update ooo"
   git push origin issue10_kh
   ```

4. **Pull Request(PR) 작성**
   - 각자 작업한 브랜치에서 `issue10` 브랜치로 PR을 생성한다. 
   - PR 작성 시 서로를 리뷰어로 설정한다.
   - 회의 전까지, 각자 댓글로 코드에 대한 피드백을 작성한다.

5. **코드 리뷰 및 수정**
   - 회의 후, 피드백에 따라 각자 코드를 적절히 수정하고 `issue10` 브랜치에 머지한다.

6. **최종 PR 및 머지**
   - `issue10` 브랜치의 코드가 정리가 완료되면 `main` 브랜치로 최종 PR을 생성하고, 리뷰 후 머지한다.
