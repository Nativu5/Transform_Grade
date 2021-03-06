# TransformGrades

本程序参照《山东省深化高等学校考试招生综合改革试点方案》中的相关规定编写，利用Python将原始卷面成绩转换为等级成绩（即最终成绩）。

转换规则如下：

> 将每门等级考试科目考生的原始成绩从高到低划分为A、B+、B、C+、C、D+、D、E共8个等级。参照正态分布原则,确定各等级人数所占比例分别为3%、7%、16%、24%、24%、16%、7%、3%。等级考试科目成绩计入考生总成绩时,将A至E等级内的考生原始成绩,依照等比例转换法则,分别转换到91-100、81-90、71-80、61-70、51-60、41-50、31-40、21-30八个分数区间,得到考生的等级成绩。

## 使用方法

* 如果计算机无Python环境，可以到[Release](https://github.com/0x7ffffff/Transform_Grade/releases)页面下载打包好的.exe程序。
* 如果已安装Python环境，请确保同时安装了[openpyxl](https://openpyxl.readthedocs.io/en/stable/index.html#installation) 库。

1. 打开程序运行目录下的 `原始成绩.xlsx` ，将需要转换的成绩单按照 `原始成绩.xlsx` 的格式制作好。
2. 将制作好的成绩单粘贴到 `原始成绩.xlsx` 中，不要改变表头等信息。
3. 关闭 `原始成绩.xlsx` 后再打开程序，按照程序要求进行操作。
4. 查看程序运行目录下的`分数区间.xlsx` 、`转化成绩.xlsx` 。

## 常见问题

* 只有某科选考人数大于等于 34 或者等于 0 时才能进行赋分。如果不足 34 人，将无法分出 8 个等级。
* 本程序会自动剔除不合法的数据（例如某考生仅选考一科或选考了四科）。剔除后的原始成绩在程序目录下的 `合法原始.xlsx` 中。
* 如果提示 `Permisson Denied`，请关闭所有已经打开的Excel表格。
* 如果提示程序文件不完整，请重新下载。
* 如果运行时出现错误，很有可能是 `原始成绩.xlsx` 或 `分数区间.xlsx` 内的表格格式被修改（例如缺少表头，缺少了某一列等等），请重新下载。
* .exe程序仅在 Windows 10 x64 和 Windows 7 x64 平台上测试过，其他平台未测试。
