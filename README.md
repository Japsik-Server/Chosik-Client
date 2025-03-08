# Chosik Client
Chosik을 위한 Minecraft 모드 클라이언트입니다.
Helios Core 기반 런처에서 사용할 수 있습니다.

## Git Subtree를 사용해 클라이언트 데이터 가져오기
##### 모든 명령어는 [JapsikLauncher-Data](https://github.com/Japsik-Server/JapsikLauncher-Data) 리포지토리의 root 디렉토리에서 실행하세요.
클라이언트 데이터를 처음 가져올 때는, 아래 명령어를 사용해 Subtree에 추가합니다.

- `git subtree add -P live/servers/Chosik-1.21.1 https://github.com/Japsik-Server/Chosik-Client.git <BRANCH_OR_TAG> --squash`

  - `<BRANCH_OR_TAG>` : Subtree에 추가할 branch 또는 tag
  - `[--squash]` : Merge 시 여러개의 커밋을 하나로 합치기(권장)

예시) `git subtree add -P live/servers/Chosik-1.21.1 https://github.com/Japsik-Server/Chosik-Client.git 1.0.0 --squash`

클라이언트를 특정 branch 또는 tag의 버전으로 변경하고 싶다면, 아래 명령어를 사용해 Subtree의 branch를 변경합니다.

- `git subtree pull -P live/servers/Chosik-1.21.1 https://github.com/Japsik-Server/Chosik-Client.git <BRANCH_OR_TAG> --squash`

  - `<BRANCH_OR_TAG>` : Subtree에 추가할 branch 또는 tag
  - `[--squash]` : Merge 시 여러개의 커밋을 하나로 합치기(권장)

예시) `git subtree pull -P live/servers/Chosik-1.21.1 https://github.com/Japsik-Server/Chosik-Client.git 1.0.1 --squash`

### 주의사항
- 클라이언트의 모든 Merge 커밋들은 `<CLIENT_NAME> <VERSION>` 형식으로 이름을 짓습니다.

  - 예시) `Chosik-Client 1.0.0`

- 만약 Subtree를 추가하거나 pull 할 때 오류가 발생한다면 이 명령어를 사용해 보세요. `git reset --hard`

  - 이 명령어는 현재까지의 모든 작업 내용 *(push 하지 않은 커밋들 또는 커밋을 생성하지 않은 작업 내용들)* 을 초기화합니다.