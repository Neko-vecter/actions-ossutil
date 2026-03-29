# actions-ossutil

使用 Node 24 的阿里云（Aliyun）ossutil 工具

```yml
steps:
  - uses: actions/checkout@v6

  - uses: Neko-vecter/actions-ossutil@v1.0.0
    with:
      endpoint: ${{ secrets.OSS_ENDPOINT }}.aliyuncs.com
      access-key-id: ${{ secrets.OSS_ACCESS_KEY_ID }}
      access-key-secret: ${{ secrets.OSS_ACCESS_KEY_SECRET }}
      sts-token: ${{ secrets.OSS_ACCESS_STS_TOKEN }}
  - run: ossutil cp -rf ./build oss://bucket/path
```
