# ISY0101 — EP3: Observabilidad del Agente — Ripley Chile

Evaluación Parcial N°3 — Ingeniería de Soluciones con IA — DuocUC 2025

## Descripción
Implementación de métricas de observabilidad, análisis de logs, dashboard de monitoreo y protocolos de seguridad sobre el agente de gestión de reclamos postventa de Ripley Chile desarrollado en el EP2.

## Métricas implementadas
- **Precisión**: porcentaje de clasificaciones correctas
- **Latencia**: tiempo de respuesta por ejecución
- **Tasa de éxito/error**: ejecuciones exitosas vs fallidas
- **Uso de herramientas**: herramientas invocadas por llamada
- **Frecuencia de escalamiento SERNAC**: casos derivados al regulador

## Requisitos
- Cuenta en [Groq](https://console.groq.com) — API Key gratuita (`gsk_...`)
- Cuenta en [ngrok](https://dashboard.ngrok.com) — Auth Token gratuito
- Google Colab (no requiere instalación local)

## Cómo ejecutar

### Paso 1 — Abrir en Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Misa323/ISY0101-EP3-Observabilidad/blob/main/ISY0101_EP3_Observabilidad_Ripley_.ipynb)

### Paso 2 — Ejecutar celdas en orden (1 → 12)

| Celda | Descripción |
|---|---|
| 1 | Instalar dependencias |
| 2 | Ingresar GROQ_API_KEY |
| 3 | Crear datos simulados |
| 4 | Indexación FAISS |
| 5 | Definir herramientas del agente |
| 6 | Construir agente con sistema de logging |
| 7 | Ejecutar batería de 8 pruebas |
| 8 | Analizar logs y trazabilidad |
| 9 | Protocolos de seguridad |
| 10 | Generar dashboard Streamlit |
| 11 | Lanzar dashboard con ngrok |
| 12 | Propuesta de mejoras |

### Paso 3 — Credenciales requeridas
En la **Celda 2** ingresa tu GROQ_API_KEY cuando se solicite.

En la **Celda 11** reemplaza `"TU_TOKEN_NGROK_AQUI"` con tu token de ngrok antes de ejecutar.

### Paso 4 — Ver el dashboard
La Celda 11 genera una URL pública. Ábrela en el navegador para ver el dashboard interactivo con todas las métricas.

## Estructura del proyecto
| Archivo | Descripción |
|---|---|
| `ISY0101_EP3_Observabilidad_Ripley_.ipynb` | Notebook principal con observabilidad completa |
| `README.md` | Este archivo |

## Stack tecnológico
- **LLM:** Llama 3.3 70B via Groq API
- **Framework:** LangChain 0.2.16
- **Vector Store:** FAISS (local)
- **Embeddings:** sentence-transformers 2.7.0 + huggingface_hub 0.23.4
- **Dashboard:** Streamlit + Plotly
- **Túnel público:** ngrok
- **Logging:** CSV automático en logs/metricas_agente.csv

## Notas importantes
- Los resultados de las métricas varían entre sesiones por la variabilidad del servidor Groq
- El token de ngrok debe ser regenerado si da error 502
- Si aparece error de rate limit (429), espera 1 minuto antes de reejecutar la Celda 7

## Uso de IA
Claude (Anthropic) fue usado como apoyo en diseño y depuración.
Citación: https://bibliotecas.duoc.cl/ia
