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

luego abrimos otra terminal

## 3. Descargar algún modelo LLM

En la página de [modelos](https://ollama.com/library)
de Ollama se busca el modelo deseado y se descarga con el siguiente comando:

````bash
$ ollama pull tinyllama
````
## 4. Prueba de request a la API REST

Para realizar una petición básica a la API de Ollama se sigue la siguiente estructura

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
}'
````

### 4.1 Consulta a la API REST sin stream

Este comando sirve para obtener una petición sin stream

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?",
  "stream": false
}'
````

## 5. Realizar request a groq

Realizar consultas a groq

````bash
curl "https://api.groq.com/openai/v1/chat/completions" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ${GROQ_API_KEY}" \
  -d '{
         "messages": [
           {
             "role": "user",
             "content": "¿por qué el cielo es azul?"
           }
         ],
         "model": "gemma-7b-it",
         "stream": false
       }'
````
