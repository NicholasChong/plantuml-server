```shell

# 打包
mvn clean package -Dmaven.test.skip=true

# 构建镜像
docker image build -f Dockerfile.tomcat -t plantuml-server:local .

# 打标签
docker tag plantuml-server:local  dongze/plantuml-server:latest

# 推送远程仓库
docker push dongze/plantuml-server:latest

# 启动服务
docker run -d -p 8080:8080 dongze/plantuml-server:latest

```
