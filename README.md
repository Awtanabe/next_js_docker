## 参考記事

https://blog.kapiecii.com/posts/2022/07/24/docker-and-nextjs/

## Setup

### Setup

プロジェクト作成

```
docker-compose run --rm app npx create-next-app sample-app
```


sample-appの中の作成されたファイルを1階層あげる

原因は下記
```
➜  next_docker docker-compose run --rm app npx create-next-app .         
WARN[0000] Found orphan containers ([Portfolio_view]) for this project. If you removed or renamed this service in your compose file, you can run this command with the --remove-orphans flag to clean it up. 
Need to install the following packages:
  create-next-app
Ok to proceed? (y) 
The directory src contains files that could conflict:

  Dockerfile
  docker-compose.yml

Either try using a new directory name, or remove the files listed above.

npm notice 
npm notice New major version of npm available! 8.11.0 -> 9.4.2
npm notice Changelog: https://github.com/npm/cli/releases/tag/v9.4.2
npm notice Run npm install -g npm@9.4.2 to update!
npm notice 
```

起動

```
docker-compose up
```