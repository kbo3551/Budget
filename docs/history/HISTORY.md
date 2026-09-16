# HISTORY

### [1] 2026-09-16 09:19 (KST) | 작업자: Codex
- 요청/목적: `가계부-설치.exe`와 `가계부-설치.7z`를 GitHub `kbo3551/Budget` 저장소에 업로드.
- 수행 내용: 빈 로컬 디렉터리를 `main` Git 저장소로 초기화하고, GitHub의 100MB 제한을 넘는 두 파일을 Git LFS(`*.exe`, `*.7z`)로 추적하여 초기 커밋 후 `origin/main`에 푸시.
- 변경 파일: `.gitattributes`, `가계부-설치.exe`, `가계부-설치.7z`, `docs/history/HISTORY.md`, `docs/memory/MEMORY_01.md`.
- 실행 명령: `git init -b main`, `git lfs install --local`, `git lfs track`, `git add`, `git commit`, `git remote add`, `git push -u origin main`, `git ls-remote`, `git lfs ls-files`, `Get-FileHash`.
- 검증: 원격 `main`이 커밋 `c42c75461252d61c8a6bc6c008318566deb455eb`을 가리킴. LFS 업로드 2/2(360MB) 완료. SHA-256은 EXE `21C517E3C21872BB5FE225BA605FBE9198320B8E85338F531AC3303D493283E0`, 7z `A1DC9FB4AD96045A5CD746C7AD3E084793A92CF78A23CE7759A086F1F82F8192`.
- 오류: 최초 샌드박스 내 `git add`에서 Git `sh.exe` 신호 파이프 생성 오류(Win32 error 5). 제한 밖에서 동일 명령을 재실행하여 성공.
- 결과: 두 배포 파일이 Git LFS 객체로 `origin/main`에 정상 업로드됨.
- 다음 액션: 없음.

---
