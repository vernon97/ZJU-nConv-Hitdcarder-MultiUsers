# ZJU-nCov-Hitcarder-MultiUsers

修改自https://github.com/Tishacy/ZJU-nCov-Hitcarder, 实验室集体打卡用(逃
只需要新建 users.json文件, 保存所有打卡人的浙大通行证账号密码即可;
users.json文件格式↓
```
{
    "219xxxxx":"password111",
    "315xxxxxx":"password222",
    "217******":"password333"
}
```
然后`python daka.py`开起来即可 依赖安装可以按照原作者的教程
---------------------------分割线--------------------------------

浙大nCov肺炎健康打卡定时自动脚本

 - 可定时，默认为每天6点5分
 - 默认每次提交上次所提交的内容（只有时间部分更新）
 - 更新表单杭州健康码部分，默认已领取绿卡，如更改选项，见`daka.py`中第84行注释
 - 已更新表单至4月18日状态

 项目用于学习交流，仅用于各项无异常时打卡，如有身体不适等情况还请自行如实打卡~

<img src="https://github.com/Tishacy/ZJU-nCov-Hitcarder/raw/master/demo.png" width="500px"/>

> 感谢[conv1d](https://github.com/conv1d)同学，已使用requests直接登录浙大统一认证平台，不再依赖phantomjs
>
> ~~增加了各操作系统的phantomjs和自动选driver的功能，结果导致库变得较大，如果想自行下载对应版本的phantomjs，可以切换到`neat`分支（只保留了windows系统的phantomjs）下载本项目。~~

## Usage

1. clone本项目（为了加快clone速度，可以指定clone深度`--depth 1`，只克隆最近一次commit），并cd到本目录
    ```bash
    $ git clone https://github.com/Tishacy/ZJU-nCov-Hitcarder.git --depth 1
    $ cd ZJU-nCov-Hitcarder
    ```
    
2. 安装依赖

    ```bash
    $ pip3 install -r requirements.txt
    ```

3. 将config.json.templ模板文件重命名为config.json文件，并修改 config.json中的配置
  
    ```javascript
    {
        "username": "你的浙大统一认证平台用户名",
        "password": "你的浙大统一认证平台密码",
        "schedule": {
            "hour": "6",    // 6点
            "minute": "5"   // 5分 
        }
    }
    ```

4. 启动定时自动打卡脚本

   ```bash
   $ python3 daka.py
   ```


## Tips

- 为了防止电脑休眠或关机时程序不运行，推荐把这个部署到VPS上
- 测试程序是否正常运行：可以先把定的时间放在最近的一个时间（比如下一分钟）看下到时间是否可以正常打卡
- 想指定自己打卡地理位置的童鞋可以参考[8#issue](https://github.com/Tishacy/ZJU-nCov-Hitcarder/issues/8#issue-565719250)


## Thanks

感谢贡献者

<a href="https://github.com/conv1d"><img src="https://avatars2.githubusercontent.com/u/24759956" width="100px" height="100px"></a>


## LICENSE

Copyright (c) 2020 tishacy.

Licensed under the [MIT License](https://github.com/Tishacy/ZJU-nCov-Hitcarder/blob/master/LICENSE)



=======
# ZJU-nConv-Hitdcarder-MultiUsers
>>>>>>> 9f65c195115cfe9c42b7d071ece90940567107d9
