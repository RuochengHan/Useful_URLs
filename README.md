# Useful_URLs

## Chemistry
1. 保护基：https://mp.weixin.qq.com/s/diKGDjocu93W5jdxXUk89g https://zhuanlan.zhihu.com/p/485056277
2. pKa：http://ibond.nankai.edu.cn/pka
3. 物理化学性质数据库（pKa等）：https://ochem.eu/home/
4. 分子骨架相关：https://nextmovesoftware.github.io/molhash/introduction.html

## SMILES SMARTS
1. SMARTS editor https://www.zbh.uni-hamburg.de/forschung/amd/software/smartseditor.html
2. online SMARTS viewer https://smarts.plus/smartsview

## Picture
1. 去水印：https://dewatermark.ai/upload
2. 去除背景：https://remove-white-background.imageonline.co/

## LLM
1. Ollama3 ubuntu教程：https://zhuanlan.zhihu.com/p/694331045
2. Ollama3 isntall：增加github ip 指向；使用IQ2-XS(https://www.datalearner.com/llm-blogs/llama_3_70b_benchmark_on_single_3090)
```bash
$ sudo vim /etc/hosts
#add
140.82.114.3 github.com
199.232.69.194 github.global.ssl.fastly.net
185.199.108.153 assets-cdn.github.com
185.199.109.153 assets-cdn.github.com
185.199.110.153 assets-cdn.github.com
185.199.111.153 assets-cdn.github.com

# then download is quicker
$ curl -fsSL https://ollama.com/install.sh | sh

# import a model
$ vim llama-3-70b-iq2-xs.mf
# add

FROM *.gguf
TEMPLATE """
{{- if .First }}
### System:
{{ .System }}
{{- end }}

### User:
{{ .Prompt }}
### Response:
"""

SYSTEM """"""


$ ollama serve
$ ollama create llama-3-70b-iq2-xs -f llama-3-70b-iq2-xs.mf

# run model
$ ollama run llama-3-70b-iq2-xs

```
3. llama3 chinese install, need to install git-lfs first
```bash
$ sudo apt-get install git-lfs
$ git clone *.git
$ git lfs pull
```
To use 终端推理 in https://github.com/CrazyBoyM/llama3-Chinese-chat
```bash
$ pip install -i https://pypi.tuna.tsinghua.edu.cn/simple --trusted-host pypi.douban.com transformers peft dataclasses typing torch torchvision torchaudio
```

## ML
1. Bayesian optimization https://distill.pub/2020/bayesian-optimization/, https://leovan.me/cn/2020/06/bayesian-optimization/#%E9%AB%98%E6%96%AF%E8%BF%87%E7%A8%8B%E5%9B%9E%E5%BD%92, https://zhuanlan.zhihu.com/p/150555551
