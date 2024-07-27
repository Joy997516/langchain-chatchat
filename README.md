# 环境安装
```python
conda create -n chatchat
conda activate chatchat
##要用这个版本号，不然会出现
# bash: chatchat-config: command not found
pip install langchain-chatchat==0.3.0.20240625
pip install langchain-chatchat[xinference] -U
conda create -n xinference
conda activate xinference
pip install "xinference[transformers]"
```

# 启动Xinference
```python
xinference-local
```

register model可加载本地模型
把路径改成本地，模型选择对应的本地模型名称

添加language model
点击模型，配置选好点launch，就会出现在Running Models 
和上面一样添加embedding model m3e

# 更改默认模型
```python
conda activate chatchat
chatchat-config model --default_llm_model Qwen1.5
chatchat-config model --default_embedding_model m3e
```
# 自定义模型接入配置
```python
这里应为 "CHATCHAT_ROOT" 变量指向目录
cd /root/anaconda3/envs/chatchat/lib/python3.11/site-packages/chatchat
vim model_providers.yaml
```

# 没添加数据库可以直接启动
```python
chatchat -a
```

