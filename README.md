## Usage

### Run with explicit credentials
```bash
docker run -p 9200:9200 \
  -e AWS_ACCESS_KEY_ID=<key>
  -e AWS_SECRET_ACCESS_KEY=<secret_key> \
  --rm -it citizensadvice/aws-es-proxy \
  aws-es-proxy -listen 0.0.0.0:9200 -endpoint <es-endpoint>
```

### Run with credentials mounted as volume
```bash
docker run -p 9200:9200 \
  -v $HOME/.aws:/root/.aws \
  --rm -it citizensadvice/aws-es-proxy \
  aws-es-proxy -listen 0.0.0.0:9200 -endpoint <es-endpoint>
```
