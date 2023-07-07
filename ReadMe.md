aar上传github maven仓库
1. 把aar上传到maven目录（后续需要同步到github的路径）
  dcapi/maven-dcapi.gradle 里面maven路径改成自己的路径
          maven {
              url  "/Users/wangqin/work/git/maven"
          }
2. 生成maven文件
  cd android 
  ./gradlew publish 
3. /Users/wangqin/work/git/maven上传同步到指定github
4. 使用maven引入aar
  在下面gradle中添加：
      repositories {
          maven { url "https://raw.github.com/yimengyuanyun/maven/main" }
      }
  在需要引入的项目gradle中添加：
    implementation 'com.dcapi:dcapi_lib:0.0.1'



