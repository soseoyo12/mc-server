# 마크 서버

## 셋업

```bash
git clone <이 저장소 URL>
cd mc-server
docker compose up -d
```

## 명령어

- 서버 켜기: `docker compose up -d`
- 서버 끄기: `docker compose down`
- 로그 보기: `docker compose logs -f mc`
- 콘솔 명령어 입력: `docker exec -i mc-server rcon-cli`
- 백업: `tar -czf backup-$(date +%Y%m%d).tar.gz data/`

## 사전 준비 (새 머신에서 처음 셋업할 때만)

1. Docker Desktop 설치: `brew install --cask docker`
2. 슬립 방지: `sudo pmset -a sleep 0 disablesleep 1`
3. Playit 설치: `brew install --cask playit`

## 메모

- 마크 버전 바꾸려면 `docker-compose.yml`의 `VERSION` 수정 후 `docker compose up -d --force-recreate`
- 친구 op 추가: `OPS` 환경변수에 콤마로 추가하거나, 콘솔에서 `op 닉네임` 입력

