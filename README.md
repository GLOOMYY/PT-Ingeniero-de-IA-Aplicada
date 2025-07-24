# 🧠 Prueba Técnica – Ingeniero de IA Aplicada

Este repositorio corresponde a una prueba técnica para la vacante de **Ingeniero de IA Aplicada**.  
Se desarrolló un sistema de **Recuperación Aumentada con Generación (RAG)** que integra un **modelo de lenguaje (LLM)** para responder preguntas en lenguaje natural a partir de información extraída de la documentación de **LangChain**.

---

## 🧩 ¿Qué hace este proyecto?

- Extrae y limpia texto desde múltiples páginas HTML con la documentación de LangChain.
- Divide el texto en chunks y genera embeddings semánticos.
- Utiliza FAISS como motor de búsqueda vectorial.
- Recupera el contexto más relevante según la consulta del usuario.
- Genera una respuesta con un modelo LLM (`flan-t5-base`) basado en el contexto recuperado.
- Evalúa la similitud semántica entre la respuesta generada y el contexto.

---

## 🚀 Cómo ejecutarlo

1. Clona este repositorio:

   ```bash
   git clone https://github.com/tu_usuario/nombre_repositorio.git
   cd nombre_repositorio
   ```

2. Instala las dependencias:

   ```bash
   pip install -r requirements.txt
   ```

3. Ejecuta el notebook:

   - Abre sistema-rag.ipynb en Jupyter Notebook, VSCode, Google Colab, o el entorno de tu preferencia.

   - Ejecuta todas las celdas en orden.
