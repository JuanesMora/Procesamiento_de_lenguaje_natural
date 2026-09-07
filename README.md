# Sistema de Reservas Inteligente con Asistente Conversacional de IA

Proyecto académico desarrollado en equipo para automatizar la gestión de reservas de canchas deportivas mediante una interfaz web, flujos de automatización y un asistente conversacional apoyado por modelos de lenguaje.

## Objetivo

Construir una solución capaz de centralizar consultas y procesos frecuentes de una cancha deportiva, permitiendo al usuario consultar información de reservas, tarifas y condiciones de uso desde una interfaz conversacional.

## Arquitectura general

```text
Usuario
  |
  v
Interfaz Streamlit
  |
  v
Webhook / API
  |
  v
Flujo de automatización en n8n
  |------------------------|
  |                        |
  v                        v
Gemini                 Base de reservas
  |                        |
  v                        |
Consulta contextual <------|
  |
  v
Respuesta al usuario
```

La solución combina una interfaz en **Streamlit**, comunicación con servicios externos mediante **ngrok**, automatización de procesos con **n8n** e integración con **Gemini**. Para las preguntas relacionadas con políticas, tarifas y condiciones de uso, el sistema consulta información técnica previamente definida e indexada.

## Funcionalidades principales

- Interfaz web para interacción con el usuario.
- Asistente conversacional para consultas frecuentes.
- Integración de un modelo de lenguaje mediante Gemini.
- Comunicación entre frontend y servicios externos mediante Webhooks/APIs.
- Automatización de procesos con n8n.
- Consulta de información sobre tarifas, condiciones y reglas de reserva.
- Uso de una base de reservas en formato tabular.

## Tecnologías

| Tecnología | Uso en el proyecto |
|---|---|
| Python | Lógica y procesamiento principal |
| Streamlit | Interfaz web |
| n8n | Automatización y orquestación de flujos |
| Gemini API | Modelo de lenguaje para el asistente |
| ngrok | Exposición temporal de servicios locales |
| Webhooks / APIs | Comunicación entre componentes |
| Excel / datos tabulares | Base de información de reservas |

## Contenido actual de la carpeta

```text
Proyecto_Chatbot/
├── Base_Reservas_Canchas_Google_Sheets_WEB (3).xlsx
├── Especificaciones_Reserva_Canchas_version_final (2).pdf
└── Proyecto_final_PLN (2).ipynb
```

- **Proyecto_final_PLN (2).ipynb:** notebook principal del proyecto.
- **Base_Reservas...xlsx:** información utilizada para la gestión de reservas.
- **Especificaciones...pdf:** documento de referencia con reglas y condiciones del sistema.

## Ejecución

1. Clonar el repositorio.
2. Abrir el notebook `Proyecto_final_PLN (2).ipynb` en Jupyter Notebook, JupyterLab o Google Colab.
3. Configurar las credenciales o claves de servicios externos cuando sean necesarias.
4. Configurar el flujo correspondiente en n8n.
5. Si se ejecuta un servicio local, utilizar ngrok para exponer el endpoint requerido.

> **Nota:** no se deben publicar claves de API, tokens ni credenciales dentro del repositorio. Se recomienda usar variables de entorno o archivos `.env` excluidos mediante `.gitignore`.

## Mejoras recomendadas

- Exportar y añadir al repositorio el workflow de n8n en formato JSON.
- Añadir una captura o GIF corto del funcionamiento del chatbot.
- Incluir un archivo `requirements.txt` con las dependencias de Python.
- Separar el código de la aplicación del notebook si se desea convertir el proyecto en una demo ejecutable.

## Contexto académico y autoría

Proyecto desarrollado de forma colaborativa en el marco de la formación en Ingeniería Electrónica de la **Universidad Nacional de Colombia - Sede Manizales**.

Repositorio personal de **Juan Esteban Mora Diaz**, quien participó en el desarrollo, integración y documentación de la solución.
