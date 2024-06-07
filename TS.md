---------------------------------------------配置TS环境--------------------------------------------- </br>
1、进入官网安装Nodejs </br>
2、cmd命令行输入 node -v,npm -v查看是否安装成功 </br>
3、安装TS编译器 npm i -g typescript </br>
4、cmd 命令行输入tsc查看是否安装成功  </br>
5、创建Hello.Ts文件输入 </br>
    console.log("Hello"); </br>
6、编译文件 </br>
  cmd输入ts所在文件目录 </br>
  tsc+文件名即 tsc Hello.ts 无提示信息编译出.js即成功 </br>

---------------------------------------------虚幻配置puer环境每个项目需要一次--------------------------------------------- </br>
1、官网GitHub拉取puerts项目  https://github.com/Tencent/puerts.git           可参考官方文档https://puerts.github.io/docs/puerts/unreal/install  </br>
2、解压拷贝puerts/unreal下的Puerts目录到您项目的Plugins目录下 </br>
3、下载V8,并解压，参考官方文档 </br>
    将解压文件夹放入    项目名/Plugins/Puerts/ThirdParty目录下 </br>
4、命令行进入BlockBreakerStarter/Plugins/Puerts，执行命令：`node enable_puerts_module.js`  </br>
5、双击 项目.uproject 打开项目，点击puerts的生成按钮，这步骤会生成UE API的TypeScript声明。  </br>
![](https://github.com/Eric-Monkey/memo/blob/main/Imgs/Ts.png) </br>
  </br>
参考知乎
https://zhuanlan.zhihu.com/p/346531865
