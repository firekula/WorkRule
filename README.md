# 注意事项

## 代码规范

* 属性及方法命名遵循小驼峰式命名法
    ```typescript
    private userName: string = "";
    private setUserName(user: string){}
    ```
* 类名及枚举命名遵循大驼峰式命名法
    ```typescript
    class User{}
    enum UsetState{}
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
## 代码提交
* 提交代码时需说明本次提交的修改
* 实现一个大功能即提交一次，尽量不要一次修改很多东西才提交
* 代码同步若遇到冲突，需双方讨论代码取舍，若场景冲突，则舍弃修改少的一方，同步后再修改