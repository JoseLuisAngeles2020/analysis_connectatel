# analysis_connectatel

# Objetivo del proyecto
El objetivo del proyecto fue analizar el comportamiento de uso de los clientes de ConnectaTel, una empresa de telecomunicaciones con operaciones en México y Colombia, para entender cómo utilizan los servicios móviles, principalmente llamadas y mensajes.
A partir de este análisis, se buscó identificar patrones de uso, valores atípicos, diferencias entre segmentos de clientes según edad, plan contratado y nivel de uso, con el fin de generar insights accionables que ayuden a mejorar la oferta comercial y la experiencia del cliente.

# Datasets utilizados

Se trabajó con tres archivos principales:
plans.csv
Contiene el catálogo de planes disponibles, incluyendo precios, minutos incluidos, GB incluidos y costos por excedente.
users_latam.csv
Incluye información de los usuarios, como identificador, edad, ciudad, fecha de registro, plan contratado y fecha de churn.
usage.csv
Registra la actividad real de los usuarios, incluyendo llamadas, mensajes, duración de llamadas y longitud de mensajes.

Etapas del análisis realizadas

# Durante el proyecto se desarrollaron las siguientes etapas:

1. Carga y exploración inicial de datos
Se cargaron los tres datasets y se revisó su estructura general, columnas, tipos de datos y primeras filas.
2. Identificación de problemas de calidad
Se detectaron valores nulos, sentinels y datos inconsistentes, como:
edades con -999
ciudades con "?"
fechas fuera de rango
valores faltantes en columnas clave
inconsistencias entre tipo de registro, duración y longitud
3. Limpieza básica de datos
Se aplicaron reglas de limpieza para:
reemplazar sentinels
convertir fechas a formato correcto
marcar fechas imposibles como nulas
conservar nulos que en realidad significaban “no aplica”, como en duration y length
4. Construcción de métricas por usuario
Se agregaron los datos de uso por user_id para crear un perfil por cliente con:
cantidad de mensajes
cantidad de llamadas
minutos totales de llamada
5. Resumen estadístico
Se obtuvieron estadísticas descriptivas para analizar el comportamiento general de variables numéricas y la distribución del tipo de plan.
6. Visualización de distribuciones
Se crearon histogramas para analizar la forma de distribución de:
edad
cantidad de mensajes
cantidad de llamadas
minutos de llamada
7. Detección de outliers
Se utilizaron boxplots y el método IQR para identificar valores extremos y decidir si debían eliminarse o mantenerse. En este caso, se concluyó que los outliers representaban comportamientos reales de uso y no errores evidentes.
8. Segmentación de clientes
Se construyeron segmentos por:
nivel de uso: bajo, medio y alto
grupo de edad: joven, adulto y adulto mayor
9. Visualización de segmentos
Se generaron gráficos para analizar la distribución de los usuarios dentro de los grupos creados.
10. Insight ejecutivo final
Se redactaron conclusiones de negocio orientadas a stakeholders, incluyendo hallazgos, segmentos valiosos, patrones de uso extremo y recomendaciones comerciales.
