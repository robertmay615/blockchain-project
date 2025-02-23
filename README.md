# blockchain-project
基于区块链的供应链金融平台-2020年秋季《区块链原理与技术》课程大作业

## 小组成员及分工
| **姓名** | **学号** |                           **分工**                           |
| :------: | :------: | :----------------------------------------------------------: |
|  李骁达  | 18340095 |     编写智能合约完成基本功能，实现同态加密，编写实验报告     |
|  陈家豪  | 18308013 | 构思平台底层逻辑，完成后端，对平台结构调试优化，完成平台应用化 |
|  刘业畅  | 18340120 |    设计网页，完成前端工作，实现合约附加功能，编写实验报告    |

组长：陈家豪

## 代码运行说明
源代码和相关依赖在 `src` 文件夹中；按照[FISCO-BCOS官方教程](https://fisco-bcos-documentation.readthedocs.io/zh_CN/latest/docs/sdk/python_sdk/index.html)准备好python-sdk和相关依赖环境后，将platform.sol放在python-sdk/contracts/下，其余文件放在python-sdk/下；此外需要额外使用`pip install Django`和`pip install phe`下载Django包和phe包。

启动方式：使用命令行进入路径python-sdk/，首先运行使用命令`python INIT.py`编译、部署智能合约，完成初始化，并获得同态加密密钥对；然后使用命令`python manage.py runserver 0.0.0.0:8000`运行Django web框架。打开浏览器访问http://主机IP地址:8000 ，即可使用（ 例如在主机上操作时，访问http://127.0.0.1:8000 ）。

初次使用时首先需要注册，然后才能登录相应账户。

cd fisco
bash nodes/127.0.0.1/start_all.sh
cd python-sdk
pyenv activate python-sdk
python INIT.py
python manage.py runserver 0.0.0.0:8000
firefox http://localhost:8000/login/

## 加分项
加分项的实现与代码说明请移步报告文件 `report.pdf` 的 Chapter2，简要说明如下：
+ 实现了附加功能：包括企业破产申请与处理、撤销交易、完备的身份验证、部分偿还、信任机构审批账单等功能；
+ 通过同态加密实现链上数据隐私保护；
+ 使用 Django 框架，实现了友好高效的用户界面；

## 联系方式
Email: chenjh328@mail2.sysu.edu.cn；lixd36@mail2.sysu.edu.cn
