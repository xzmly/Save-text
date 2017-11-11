#### 这里给sqlite3安装做一个补充

- 很多同学可能都困扰再sqlite3安装问题中，明明就快做完毕设了，竟然一个npm卡着整晚睡不着
- 有位大神已经说出了自己解决的例子，这里我说说我的解决办法

- 执行以下步骤之前，请确认是不是安装了nvm  
~~~
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
~~~
- 还要你要安装了nrm，并切换到淘宝路径
~~~
npm install nrm
nrm use taobao
~~~

1. 首先我是下载node 6.10.3版本的，详细命令就是
~~~
nvm install 6.10.3
~~~
2. 然后我们通过以下命令，更换node版本
~~~
nvm use 6.10.3
~~~
3. 接着我们去看项目课程里若愚老师给出的sqlite3 和 sequelize 版本
~~~
//老师的版本
"sequelize": "^3.30.2",
"sqlite3": "^3.1.8",
~~~
4. 照着版本去安装，不要问为什么，我都不知道
~~~
npm install --save sequelize@3.30.2
npm install --save sqlite3@3.18
~~~

5. 当你下载sqlite3的时候,中间会卡住，因为被墙了，这时候我们ctrl+c停止下载，把地址复制下来，复制到浏览器的地址上，自己把他下载下来

6. 下载好后把文件解压，然后我们进入你的node_modules/sqlite3/lib/binding 替换里面的
node-v48-linux-x64文件夹

7. 尝试去执行视频里的操作，可能，或者，应该，成功了！

#### ps：这里多谢张同学张大神的见解，没他也写不出来这文章。
