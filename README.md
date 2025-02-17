# SciChart
## 简介
待补充
## 部署要求
* python 3.8及以上版本
* pytorch 1.12及以上版本，推荐2.0及以上版本
* 建议使用CUDA 11.4及以上（GPU用户需考虑此选项）
<br>

## 快速使用
在开始前，请确保你已经配置好环境并安装好相关的代码包。最重要的是，确保你满足上述要求，然后安装相关的依赖库。

```bash
pip install -r requirements.txt
```
因为API调用需要密钥，请提前在环境变量中添加
```bash
export LMM_API_KEY="your_api_key"
```
### 使用API进行图文问答
```bash
python API.py
```
* 根据提示从data/选择数据集输入  
* 在instructions.py文件夹下修改各类问题对应的指令
* 在注释处修改所需要api
* 输出结果保存在output文件夹下
### 使用gptacc评测API的图文问答能力
```bash
python eval_gptacc.py
```
* 根据提示从output文件夹下选择数据集输入  
* 程序运行完后直接显示测评结果 
### 评测API的图文问答能力
```bash
python eval_relaxedacc.py
```
* 根据提示从output文件夹下选择数据集输入  
* 程序运行完后直接显示测评结果 
