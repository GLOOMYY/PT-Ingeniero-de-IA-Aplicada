# 📄 Análisis Técnico

## 1. 🧠 Modelo de Embeddings

- Se utilizó **`all-MiniLM-L6-v2`** por ser un modelo **ligero, eficiente** para uso en local con poca exigencia computacional.
- Se empleó un `chunk_size` de **500 caracteres** con un `chunk_overlap` de **50** para mantener coherencia semántica entre los fragmentos de texto.

---

## 2. 🗃️ Vector Store

- Se eligió **FAISS** por su simplicidad, velocidad de búsqueda y compatibilidad con entornos **solo CPU**.

---

## 3. 🤖 Modelo Generativo (LLM)

- El modelo utilizado fue **`google/flan-t5-base`** debido a:

  - Su **disponibilidad gratuita y open-source**.
  - Su **bajo consumo de recursos**, ideal para CPU.
  - Se puede reemplazar por modelos más avanzados como **Mistral** o **Llama** si se dispone de GPU.

---

## 4. 🎯 Prompting Controlado

- El prompt fue diseñado con instrucciones explícitas para responder solo usando el contexto proporcionado.
- Esto mejora la fidelidad de la respuesta y reduce alucinaciones típicas de los LLM.

---

## 5. 🧪 Evaluación

- Se realizaron pruebas manuales con multiples preguntas.
- Se utilizó una métrica básica de similaridad semántica (`cosine_similarity`) para comparar la respuesta generada con el contexto recuperado.

---

## 6. ⚖️ Trade-offs

| Precisión | Rendimiento | Explicación                                                       |
| --------- | ----------- | ----------------------------------------------------------------- |
| 🔼        | 🔽          | LLMs pequeños como FLAN-T5 son rápidos pero menos precisos.       |
| 🔼        | 🔼          | El modelo de embeddings ofrece un excelente balance.              |
| 🔽        | 🔼          | No se usaron re-rankers ni re-phrasing para mantener simplicidad. |

---

## 7. 🚀 Posibles mejoras

- Reemplazar `flan-t5-base` por un modelo más robusto como Mistral o Llama si se dispone de GPU.
- Incluir un sistema de **re-ranking**.
- Mejorar el **chunking** estructurándolo por secciones semánticas del HTML (titulares, subsecciones).
- Contruir una API Rest con FastAPI para facilitar la integración del sistema.

---
