# 工作注意  
* 确认素材图是否有问题（是否缺图或者素材图这样切可能不够好）并**及时反馈**给美术  
* 动态效果或其他不明白的地方**及时询问**美术  
* 觉得设计可以改进的地方**及时**和美术讨论  
* 游戏完成后发游戏链接并让美术确认  
* **每天**都要关注负责项目的美术进度（让美术将完成的图发群），及时拿到素材并反馈问题  
* 收到修改或需修复的bug，如没有在项目管理平台发布任务，需要自己在项目相关任务评论中添加（由XXX发布修改XXX）  
* 没有经过美术得到的界面布局修改等，需要**及时反馈**给美术  
* 对美术需要修改的地方，都要在项目管理平台发布任务  

# 代码规范

* 属性及方法命名遵循小驼峰式命名法
    ```typescript
    private userName: string = "";
    private setUserName(user: string){}
    ```
* 类名及枚举命名遵循大驼峰式命名法
    ```typescript
    class User{}
    enum UserState{}
    ```
* 类名、变量名和方法名等，尽量使用英文单词
* 使用 `Typescript` 时，变量及方法声明，需要把类型也写好
 
    ```typescript
    //例
    private userName: string = "";

    @property(cc.Node)
    private userNode: cc.Node = null;

    public getUserInfo(): UserInfo{ return this.userInfo }
    ```
* 方法尽量添加注释
    ```typescript
    /** 获取状态 */
    public getState(){}
    
     /**
     * 将指定摄像机的内容渲染到Sprite上
     * @param camera 摄像机
     * @param targetSprite sprite
     */
    public static renderCamera(camera: cc.Camera, targetSprite: cc.Sprite) {
        ...
    }
    ```

# 代码提交
* 提交代码时需说明本次提交的修改
* 实现一个大功能即提交一次，尽量不要一次修改很多东西才提交
* 代码同步若遇到冲突，需双方讨论代码取舍，若场景冲突，则舍弃修改少的一方，同步后再修改

# 发包
* 发包时压缩包的名字命名规则为 `游戏名`-`平台名(构建默认名称)`-`日期(0318)第几个包(01)` 例: `游戏名-web-mobile-031801.zip`

# Github配置
* [Git 下载地址](https://git-scm.com/downloads)
* 使用 `Github` 上的ssh链接来配置远程链接
* `ssh-keygen -t rsa -C "example@mail.com"` 来配置本地ssh密钥
* `cd ~/.ssh` + `cat id_rsa.pub` 来获取公钥  
  ![](./image/github1.png)
* 在 `Github` 上点击设置  
  ![](./image/github2.png)
* 选择左侧 `SSH and GPG keys`  
  ![](./image/github3.png)
* 点击 `New SSH key` 将密钥拷贝进去之后点击 `Add SSH key` 即可  
  ![](./image/github4.png)
* 新建空文件夹，右键打开 `Git bash`  
  ![](./image/git1.png)
* 输入 `git clone 存储库ssh地址` 克隆项目到本地  
  ![](./image/git2.png)
* 之后将克隆下来的文件夹里的 `.git` 文件夹拷贝到项目中，即可在 VSCode 中提交
* `git config --global user.name` 可以设置全局 `git` 用户名，该信息会在提交时附带  
* `git config --global user.email` 可以设置全局 `git` 邮箱，该信息会在提交时附带  
* 可以通过先在 `Github` web修改一些东西提交，本地查看提交记录来得到 `Github` 上配置的用户名和邮箱，来防止网页提交和本地提交变为两个用户  
    ![](./image/tip1.png)

# `VSCode` 建议安装的插件 
* `Cocos Creator JS` 
  
    ![](./image/tip2.png)

* `GitLens`  

    ![](./image/tip3.png)
    ![](./image/tip4.png)
    
* `TSLint`
    
    ![](./image/tip5.png)