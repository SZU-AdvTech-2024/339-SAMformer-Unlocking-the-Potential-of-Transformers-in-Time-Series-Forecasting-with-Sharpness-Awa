## SAMformer (ICML'24 Oral)

## 安装
要开始使用 SAMformer，请克隆此存储库并安装所需的软件包。

```bash
git clone https://github.com/romilbert/samformer.git
cd SAMformer
pip install -r requirements.txt
```

确保您已安装 Python 3.8 或更高版本。

## 模块
SAMformer 由几个关键模块组成：
- `models/`: 包含 SAMformer 架构以及用于规范化和优化的必要组件。
- `utils/`: 包含用于数据处理、训练、回调和保存结果的实用程序。
- `dataset/`：用于存储实验中使用的数据集的目录。为了便于说明，此目录仅包含 .csv 格式的 ETTh1 数据集。您可以在此处https://drive.google.com/drive/folders/1ZOYpTUa82_jCcxIdTmyr0LXQfvaM9vIy下载我们实验中使用的所有数据集(ETTh1、ETTh2、ETTm1、ETTm2、electricity、weather、traffic和exchange_rate）)。

## 要启动培训和评估过程，请使用带有相应参数的脚本：run_script.sh
sh run_script.sh -m [model_name] -d [dataset_name] -s [sequence_length] -u -a

## 脚本参数
-  `m`：型号名称。
-  `d`：数据集名称。
-  `s`：序列长度。默认值为 512。
-  `u`：激活锐化感知最小化 （SAM）。自选。
-  `a`：激活其他结果保存。自选。

## Example
```bash
bash run_script.sh -m transformer -d ETTh1 -u -a
```