# DevOps Automated Deployment with Surge & GitHub Actions 🚀

Este proyecto fue desarrollado para la materia **Electiva II: DevOps**. El objetivo principal es diseñar e implementar un pipeline automatizado de **Integración Continua y Despliegue Continuo (CI/CD)** para eliminar los despliegues manuales, asegurando que cualquier cambio en el código fuente se publique en producción de forma segura e instantánea al realizar un *push* a la rama principal.

La aplicación estática se despliega automáticamente en **Surge.sh** mediante flujos de trabajo en la nube.

---

## 🛠️ Conceptos de DevOps Implementados

*   **Integración Continua (CI):** Centralización del código en el repositorio con validación y seguimiento de versiones mediante Git.
*   **Despliegue Continuo (CD):** Automatización del ciclo de liberación de software empleando runners en la nube para publicar el sitio web sin intervención humana.
*   **Infraestructura como Código / Automatización de Tareas:** Definición del pipeline de despliegue mediante archivos de configuración declarativos estructurados en YAML.

---

## 📁 Arquitectura del Repositorio

*   **`index.html`**: El sitio web o interfaz estática base utilizada como artefacto para validar el correcto funcionamiento del entorno de despliegue.
*   **.github/workflows/main.yaml**: El núcleo del pipeline de DevOps. Contiene la secuencia de instrucciones lógicas de GitHub Actions (configuración del entorno, instalación de dependencias de Surge y ejecución del comando de publicación utilizando variables de entorno protegidas o tokens de autenticación).

---

## 🧰 Tecnologías y Herramientas Utilizadas

*   **Orquestador de CI/CD:** GitHub Actions.
*   **Plataforma de Hosting:** Surge.sh (Static web publishing).
*   **Lenguajes:** HTML5 / YAML (para la configuración del workflow).

---

## 🚀 Cómo Funciona el Pipeline

El flujo automatizado se desencadena bajo las siguientes condiciones:

1. **Trigger:** Un desarrollador realiza un `git push` a la rama principal (`main` o `master`).
2. **Ambiente Virtual:** GitHub Actions levanta un contenedor (ej. Ubuntu) de forma efímera.
3. **Autenticación:** El pipeline extrae de manera segura el token de autenticación configurado en los *Repository Secrets* de GitHub.
4. **Despliegue:** Se ejecuta el comando automatizado de Surge para transferir los archivos del proyecto al dominio público asignado en internet.

---

## 🎓 Contexto Académico
Este laboratorio práctico sirvió para asimilar las bases fundamentales de la cultura DevOps, orientándose al uso de herramientas modernas de automatización y entrega de software de calidad de manera ágil y eficiente.
