# OWASP ZAP
## USAGE
### Full Scan
```
docker run -v $(pwd):/zap/wrk/:rw -t softwaresecurityproject/zap-stable zap.sh -cmd -autorun /zap/wrk/zap.yaml
```

### API Scan
```
docker run -v $(pwd):/zap/wrk/:rw -t softwaresecurityproject/zap-stable zap.sh -cmd -autorun /zap/wrk/zap-api.yaml
```