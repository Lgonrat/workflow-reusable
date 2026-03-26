# 🤖 Linter IA — Reusable Workflow

El workflow **Linter IA** analiza automáticamente los cambios realizados en una Pull Request y genera un resumen legible con todos los archivos modificados y sus diferencias.  
Está diseñado como un **workflow reutilizable**, lo que permite invocarlo desde múltiples repositorios sin duplicar lógica.

Este análisis sirve como base para procesos de IA posteriores (TestPlanIA, ExecuteTests, etc.).

---

## 🚀 Características principales

- Obtiene el **diff real** entre la PR y la rama base (por defecto `main`).
- Genera un archivo Markdown con el resumen: `linter-summary.md`.
- Publica automáticamente un comentario en la Pull Request con los cambios detectados.
- Expone un output para encadenar otros workflows.

---

## 📌 ¿Para qué sirve?

Este workflow es útil para:

- Revisar rápidamente qué ha cambiado en una PR.
- Generar resúmenes formateados y fáciles de leer.
- Servir como entrada a otros procesos automáticos basados en IA o reglas.
- Asegurar visibilidad clara de los cambios antes de aprobar una PR.
- Implementar pipelines IA como *Linter IA → TestPlanIA → ExecuteTests*.

---

## 📁 ¿Cómo usarlo desde otro repositorio?

Crea este archivo en el repo donde quieras activar el análisis automático de PRs: **.github/workflows/linter-on-actions-pr.yml**
Con esto, cada vez que se abra o actualice una PR, se ejecutará el Linter IA.