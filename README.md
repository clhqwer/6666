# 一.argparse的使用步骤
## 1.定义命令行解析器对象
```
import argparse         #导入库
parser = argparse.ArgumentParser(description='test')  #定义命令行解析器对象
```
## 2.添加命令行解析器对象
```
parser.add_argument('--sparse', action='store_true', default=False, help='GAT with sparse version or not.')
parser.add_argument('--seed', type=int, default=72, help='Random seed.')
parser.add_argument('--epochs', type=int, default=10000, help='Number of epochs to train.')
```
## 3.从命令行中结构化解析参数
```
args = parser.parse_args()
print(args.sparse)
print(args.seed)
print(args.epochs)
```
