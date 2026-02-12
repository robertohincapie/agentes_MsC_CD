# agentes_maestria_CD
# Se debe tener instalado UV
curl -LsSf https://astral.sh/uv/install.sh | sh
uv --version

# Organización del repositorio para poder correr los agentes. 
uv init
uv venv

# add dependencies
uv add --pre langgraph langchain langchain-openai
uv add --pre langchain-anthropic
uv add "fastapi[standard]"

# add dev dependencies
uv add "langgraph-cli[inmem]" --dev
uv add ipykernel --dev
uv add grandalf --dev
uv add langchain-tavily
uv add langchain-community

# run the agent
#uv run langgraph dev



# instalar el proyecto con la estructura apropiada
uv pip install -e .

# Cuando se instala el repositorio
# Debe haber una instalacion previa de Python sobre Windows, buscarlo en: 
# En el proyecto necesitamos python >=3.12
https://www.python.org/downloads/windows/

# Creación del ambiente virtual:
uv venv

# Instalar los paquetes desde UV al ambiente creado. 
uv sync
