# Impacto de Eventos por Origen de País en Volatilidad

Sistemas de alerta ante shocks regulatorios

## 📌Descripción General

Este proyecto analiza cómo eventos regulatorios negativos impactan la volatilidad posterior del precio, comparando ese impacto entre distintos países.

No todos los mercados reaccionan igual ante una mala noticia regulatoria.
Este insight mide dónde los eventos generan shocks más violentos, ayudando a construir sistemas de alerta y gestión de riesgo geográfico.

## 📍Insight Clave

- ¿En qué países un Problema Regulatorio genera mayor inestabilidad de precios en los días posteriores al evento?

Una volatilidad post-evento elevada indica:
- menor previsibilidad regulatoria,
- mayor incertidumbre institucional,
- reacciones de mercado más emocionales o desordenadas.

## 💼Valor de Negocio

Identifica riesgo país desde el comportamiento real del mercado.

Permite:
- ajustar exposición geográfica,
- diseñar alertas automáticas,
- calibrar stops y sizing por país.

Fundamental para:
- carteras internacionales,
- análisis de riesgo regulatorio,
- trading event-driven.

Complementa ratings soberanos con datos empíricos.

Fuentes de Datos
- eventos_corporativos
- ticker_id
- fecha
- tipo_evento
- tickers
- ticker_id
- bolsa_mercado
- precios_diarios
- ticker_id
- fecha
- open
- close

## 🧠Lógica del Análisis

- Se filtran eventos corporativos del tipo Problema_Regulatorio.

- Para cada evento se calcula la volatilidad de los 3 días posteriores, usando:
  - desviación estándar de retornos intradía.

- Se asegura consistencia exigiendo exactamente 3 días post-evento.
- Se agrupan los resultados por país / mercado.
- Se calcula la volatilidad promedio post-evento por país.
- Se descartan países con baja muestra estadística.

## 📊Interpretación de Resultados

Alta volatilidad post-evento
→ Mercado sensible e inestable ante shocks regulatorios.
→ Riesgo operativo elevado.

Volatilidad moderada o baja
→ Capacidad del mercado para absorber malas noticias.
→ Mayor eficiencia institucional.

Diferencias claras entre países
→ Evidencia empírica de primas de riesgo regulatorias.

## 🧩Casos de Uso

- Sistemas de alerta temprana por país.
- Ajuste de exposición internacional antes de eventos.
- Evaluación comparativa de riesgo regulatorio.
- Modelos de stress geográfico.
- Priorización de mercados para inversión institucional.

## 🚀Posibles Extensiones

- Comparar Problemas Regulatorios vs. otros eventos.
- Analizar ventanas de 5 y 10 días post-evento.
- Normalizar por volatilidad histórica del país.
- Integrar con kurtosis y skewness post-evento.
- Evaluar asimetría (volatilidad al alza vs. a la baja).

## ✒️Nota Final

El riesgo regulatorio no se mide en comunicados.
Se mide en cómo tiembla el mercado después.

Este insight no pregunta si hubo un problema, pregunta dónde ese problema realmente desestabiliza todo 🌍⚠️

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
