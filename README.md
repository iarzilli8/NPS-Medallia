# NPS-Medallia

> **Proyecto Final - Diplomatura: Inteligencia Artificial Aplicada a Entornos Digitales de Gestión (FCE-UBA)**
> **Nivel de Alcance:** Nivel 2 (Maqueta Navegable / Prototipo de Interfaz)

---

Enlaces del Proyecto
* **Despliegue en Vivo (Vercel):** https://nps-medallia-w9pe.vercel.app/

## ¿Qué hace el proyecto?
Este proyecto es una **maqueta interactiva navegable** diseñada para el área de Backoffice y Customer Experience (CX) de Samsung. Su función principal es simular la confección automatizada de un reporte basado en el procesamiento y análisis masivo de encuestas de satisfacción de clientes provenientes de la plataforma **Medallia NPS**. 

El sistema permite inyectar el criterio histórico de analistas humanos mediante la técnica de *Few-Shot Learning*, logrando que la Inteligencia Artificial asimile la lógica institucional de categorización en segundos para clasificar nuevos reportes sin necesidad de reentrenar código.

---

## Objetivo
En la operación diaria, la clasificación manual de comentarios de clientes insatisfechos (detractores) consume muchas horas de trabajo analítico y posterga la ejecución de acciones correctivas urgentes en momentos críticos (como lanzamientos de productos o eventos masivos de venta como Hot-Sale, CyberMonday o BlackFriday).

Este proyecto busca transferir el tiempo humano utilizado en confeccionar el reporte hacia tareas que permitan la utilización de los resultados del reporte en sí.

---

## 🛠️ ¿Cómo se usa?

Al tratarse de un prototipo interactivo (Single Page App estructurada en HTML, JavaScript nativo), el flujo operativo se simula de manera local en el navegador del usuario en tres  pasos:

1. **Sección de Carga (Entrenamiento):**
   * **Paso 1:** Se simula la carga de la *Matriz de Criterio General (Histórico Humano)* que contiene las clasificaciones históricas del negocio. Aquí es donde se alimentaría a la IA de todas las encuestas que analizamos manualmente hasta el moemnto y que por temas de privacidad no puedo utilizar aquí.
   * **Paso 2:** Se vincula la *RawData Actual de Medallia* del día/semana/mes que se desea auditar.
   * *Nota para evaluación rápida:* Se disponibiliza el botón **"Cargar simulación rápida de archivos (Inyectar MockData)"** para realizar el test con bulks simulados.
2. **Procesamiento:** 
   * Se presiona el botón **"Clonará Criterio Humano y Procesar Lote"**. La consola interactiva de la derecha mostrará en tiempo real el log lógico del pipeline de IA.
3. **Sección Dashboard:**
   * Al conmutar de pestaña, el panel se actualiza dinámicamente exponiendo la *Cantidad de Detractores*, su *Representación Porcentual* sobre el volumen total de la muestra y el cuadro analítico **"Top 5 detractor cause"** ordenado de mayor a menor frecuencia.
   * Al final del panel, se despliega la *Pivot Table* consolidada. Presionando el botón azul **"Exportar Reporte (Excel)"**, la aplicación empaqueta los resultados y fuerza la descarga de un archivo `.csv` real compatible con Microsoft Excel para la distribución operativa.

---
