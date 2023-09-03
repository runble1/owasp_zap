# OWASP ZAP


## USAGE
### CLI Scan
```
docker pull owasp/zap2docker-weekly
docker run -v $(pwd):/zap/wrk/:rw -t owasp/zap2docker-weekly zap-api-scan.py -t /zap/wrk/openapi.yaml -f openapi -r report.html
```

### Automation Framework
```
docker run -v $(pwd):/zap/wrk/:rw -t softwaresecurityproject/zap-stable zap.sh -cmd -autorun /zap/wrk/zap.yaml
```

## DEBUG
ログを見る
```
docker ps -a
docker logs <CONTANINER_ID>
```

シェルを開く
```
docker run -v $(pwd):/zap/wrk/:rw -it --entrypoint /bin/sh owasp/zap2docker-weekly
```
