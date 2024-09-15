## Ollama下载



**网址**：[Ollama](https://ollama.com/)  

**流程**：

**1.创建Modelfile**文件来加载自己模型， 教程文档：[ollama/docs/import.md at main · ollama/ollama (github.com)](https://github.com/ollama/ollama/blob/main/docs/import.md)

##### Importing a model from Safetensors weights

First, create a `Modelfile` with a `FROM` command which points to the directory containing your Safetensors weights:

```
FROM /path/to/safetensors/directory
```

**2.创建本地模型**

```
ollama create mymodel -f ./Modelfile
```

**3.测试本地模型**

```
ollama run my-model
```



## Open WebUI

**网址**：[open-webui/open-webui: User-friendly WebUI for LLMs (Formerly Ollama WebUI) (github.com)](https://github.com/open-webui/open-webui)

**docker下载**：

Install Docker Desktop on Mac :[Mac | Docker Docs](https://docs.docker.com/desktop/install/mac-install/)



**流程**：

**1.直接启动docker并且自动配置好WebUI**

### Installation with Default Configuration

- **If Ollama is on your computer**, use this command:

  ```
  docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
  ```



**2.注册(第一个为管理)登录后选择模型直接用即可(ollama的模型)**

<img src="C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20240915224450708.png" alt="image-20240915224450708" style="zoom:50%;" />