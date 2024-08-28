# LLM Repositorio de prueba
Repositorio de trabajo con modelos de lenguaje largo usando OLLAMA

## 1. Instalación de Ollama

Para instalar Ollama accedemos a la pagina de
[Ollama](https://ollama.com/download)
En caso de que sea SO LINUX se ejecuta el siguiente comando

````bash
$ curl -fsSL https://ollama.com/install.sh | sh
````
## 2. Ejecutar el servidor

Una vez instalado se ejecuta el servidor de Ollama
con el siguiente comando

````bash
$ ollama serve
````

## 3. Descargar algún modelo LLM

En la página de [modelos](https://ollama.com/library)
de Ollama se busca el modelo deseado y se descarga con el siguiente comando:

````bash
$ ollama pull tinyllama
````


