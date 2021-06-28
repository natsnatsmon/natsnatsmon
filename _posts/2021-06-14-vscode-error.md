---
title: [PowerShell][VSCODE] 이 시스템에서 스크립트를 실행할 수 없으므로 파일을 로드할 수 없습니다. 자세한 내용은 about_Execution_Policies를 참조하십시오.
author: author
license: true
tags: VSCODE, PowerShell
---



이 시스템에서 스크립트를 실행할 수 없으므로 파일을 로드할 수 없습니다. 
자세한 내용은 about_Execution_Policies(https://go.microsoft.com/fwlink/?LinkID=135170)를 참조하십시오.

+   ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : 보안 오류: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess


해결 방법
1. PowerShell ExcutionPolicy 확인하기

  1) PowerShell 관리자 권한 실행

  2) Get-ExcutionPolicy 결과가 RemoteSigned인지 확인

  3) RemoteSigned가 아니면, Set-ExcutionPolicy RemoteSigned로 권한 변경
 
  4) Get-ExecutionPolicy로 RemoteSigned 권한 변경된 것 확인

2. VSCODE 실행 shell을 cmd로 바꿔주기
  1) Select Default Profile
  
  ![image](https://user-images.githubusercontent.com/32382140/121857601-c27c9180-cd30-11eb-9ffa-7073baf3ed9f.png)
 
  2) Command Prompt 선택
  
  ![image](https://user-images.githubusercontent.com/32382140/121857680-d6c08e80-cd30-11eb-9671-8e2bc4a45749.png)
  
  3) Terminal 재시작


<script src="https://utteranc.es/client.js"
        repo="natsnatsmon/natsnatsmon.github.io"
        issue-term="pathname"
        label="Comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
