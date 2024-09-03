# LLM_HR

Repositorio de proyecto de trabajo con modelos de lenguaje largo usando ollama

# 1.  Instalación 

Como primer paso descargamos [ollama] (HTTPS://ollama.com/download/linux) de su pagina web, y ejecutamos el siguiente comando

....bash

curl -fsSL HTTPS://ollama.com/install.sh | sh


# 2. Ejecutar el servidor 

ejecutar el servidor de API rest de ollama con el siguiente comando

ollama serve 



# 3. Descargar un modelo 
crear una nueva consola para ejecutar lo siguiente 


En la pagina de ollama (HTTPS:ollama.com/library)
utiliza el siguiente  comando 

.....bash
ollama pull qwrn:0.5by

Listar ias

Ver modelos instalados

ollama list

#Ejecutar consultas sobre un modelo

ollama run tinyllama why sky is blue?


# 4. Realizar un request a la API REST

emitir y que me retorne una respuesta (metodo) (/URI"URL") (datos)

post /api/generate

curl -X POST http://localhost:11434/api/generate -d '{"model":"tinyllama","prompt": "why is the sky blue?"}'

para que la salida la alamcene en un archivo y ver la cantidad de tokens(mode stream)

curl -X POST http://localhost:11434/api/generate -d '{"model":"tinyllama","prompt": "why is the sky blue?"}' -o salida.md

para que la salida se entrege completa y no por tokens

curl -X POST http://localhost:11434/api/generate -d '{"model":"tinyllama","prompt": "why is the sky blue?", "stream": false}' -o salida.md

# 5. guardar informacion de git

git add .
git commit -m "UPDATED README.md"
git push origin


# Webgrafia

[ejemplo de readme.md] (HTTPS://github.com/salvadorhm/introduccion_iq_generarivs/wiki)
[Introducción ollama ] (https://github.com/salvadorhm/introduccion_ia_generativa/wiki/3.-Introduccion-a-Ollama)
[documentación de API ollama] (https://github.com/ollama/ollama/blob/main/docs/api.md)