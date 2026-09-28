``` bash
docker run --rm -v "$PWD:/app" -w /app golang:1.24 go mod init github.com/xxxx/xxxx
```

なお、`golang:1.24`は、Docker Hubで配布されている公式Goイメージのタグ。
