- 커밋 기록에서 특정 파일 제거
    
    git filter-branch -f --index-filter 'git rm --cached --ignore-unmatch app/src/main/java/com/example/readdirectly/Config.java`
    
- 이미 커밋한 메시지 수정

    혼자 작업했을 경우만 rebase로 겨우 수정 가능

    git rebase -i HEAD~숫자

    git rebase -i —root
