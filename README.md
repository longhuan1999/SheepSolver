# SheepSolver
> 本项目主要用于计算《羊了个羊》微信小程序的解题步骤

# 项目公示
> 由于算法采用简单的回溯算法，且操作过程中存在大量牌面，故能否在短时间内成功解答取决于运气<br>
> 如果解题时间超过5分钟，建议放弃挑战并重新开始

# 使用教程
## 部署第三方项目
- 下载并部署该[开源项目](https://github.com/BugMaker888/sheep)

## 修改本地文件
- 修改`web/sheep.py`文件中第13行代码，将路径修改为本项目的绝对路径，如下面所示
```text
# 替换前
self.solve_origin_path = "path/to/your/SheepSolver/online_data.json"
# 替换后
self.solve_origin_path = "/home/root/SheepSolver/online_data.json"
```

## 替换第三方项目
- 把`web/html`目录下的内容，替换到已成功部署的第三方项目的路径`three.js/examples`
- 把`web`目录下的两个文件，替换到已成功部署的第三方项目的根路径

## 获取游戏地图数据
- 按照说明，启动`mitmweb`服务和`npm`服务
- 打开小程序并进入游戏
- 注意此时本项目根路径下的`online_data.json`文件会更新

## 求解答案并加载到网页上面
- 打开终端并进入到本项目的根路径
- 执行命令`python main.py`
- 等到结果成功打印出来后，把倒数第二行的数据复制出来
- 把结果粘贴到已成功部署的第三方项目文件`three.js/examples/sheep.html`的第50行代码，如下面所示

```text
# 替换前
let answer = ["把答案粘贴到这里"];
# 替换后
let answer = [29, 37, 56, ......];
```

# 许可证
GNU AFFERO GENERAL PUBLIC LICENSE Version 3, 19 November 2007
