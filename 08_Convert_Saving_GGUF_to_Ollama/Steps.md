_ Ollama Modelfile_

```pyhton
FROM mervinpraison/Llama-3.1-8B-bnb-4bit-python/unsloth.Q5_K_M.gguf

TEMPLATE """Below are some instructions that describe some tasks. Write responses that appropriately complete each request.{{ if .Prompt }}

### Instruction:
{{ .Prompt }}

{{ end }}### Response:
{{ .Response }}<|end_of_text|>"""

PARAMETER stop "<|start_header_id|>"
PARAMETER stop "<|eot_id|>"
PARAMETER stop "<|end_header_id|>"
PARAMETER stop "<|end_of_text|>"
PARAMETER stop "<|reserved_special_token_"
```


_Grabbing a Huggingface TOKEN _

grabbing a Huggingface Token from 


![](https://github.com/basharourabi/Llama_Fine-Tuning/blob/main/00_Assets/images/Screenshot%202024-09-20%20094403.png)

_Ollama Create Custom Model_

```bash
ollama create -f Modelfile me/llama3.1-python
ollama run me/llama3.1-python
ssh-keygen -t ed25519 -N ""
sudo cp ~/.ssh/id_ed25519 /usr/share/ollama/.ollama
ollama push me/llama3.1-python
```
