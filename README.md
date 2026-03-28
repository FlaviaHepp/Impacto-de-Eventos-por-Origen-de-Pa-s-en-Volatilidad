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

***
📊⚡ **No todos los eventos mueven el mercado igual… y eso es una ventaja**

En trading, muchas estrategias reaccionan a eventos:

📢 Earnings
🔀 Splits
🏦 Cambios regulatorios

Pero hay una pregunta clave que pocas veces se cuantifica bien:

👉 **¿Qué eventos realmente generan volatilidad?**

---

💡 Estuve analizando esto con un enfoque simple:

Medir la **volatilidad en los 3 días posteriores** a cada evento corporativo.

---

🔥 **El insight:**

Clasificar eventos según cuánto “mueven” el precio después de ocurrir.

No todos tienen el mismo impacto:

* Algunos generan movimientos explosivos
* Otros… prácticamente nada

---

🧠 **¿Por qué es importante?**

Porque te permite anticipar el comportamiento del mercado:

👉 Antes del evento, ya sabés qué esperar después.

---

📈 Aplicaciones prácticas:

* Ajustar stops y gestión de riesgo
* Elegir qué eventos tradear (y cuáles ignorar)
* Diseñar estrategias event-driven
* Priorizar oportunidades con mayor potencial de movimiento

---

⚡ Ejemplo conceptual:

* Earnings → alta volatilidad esperada
* Split → impacto más moderado
* Otros eventos → depende del contexto

👉 Pero ahora, en lugar de suponerlo… lo medís.

---

💬 El mercado no reacciona igual a todas las noticias.

👉 Y entender *cómo reacciona* es más valioso que la noticia en sí.

---

En trading cuantitativo, medir el impacto es mejor que asumirlo.

¿Alguna vez te sorprendió que una noticia “importante” no moviera el precio… o al revés? 👇

***
🌍 **No todos los mercados reaccionan igual ante malas noticias.**

Cuando aparece un **problema regulatorio**, sabemos que va a haber impacto.

Pero hay una pregunta más profunda:

🧠 **¿En qué países ese impacto es más violento?**

---

📊 En este análisis medí:

👉 La **volatilidad en los 3 días posteriores** al evento
👉 Usando desviación estándar de los retornos
👉 Y comparando… **por país / mercado**

---

⚠️ Resultado clave:

👉 Algunos mercados muestran una reacción **mucho más volátil**
👉 Otros absorben el impacto de forma más estable

---

💡 ¿Por qué pasa esto?

Porque cada mercado tiene:

* Diferente nivel de eficiencia
* Distinta profundidad de liquidez
* Regulaciones y transparencia variables

---

🚨 Insight clave:
**El mismo evento no genera el mismo riesgo…
depende del mercado donde ocurre.**

---

🔍 ¿Qué permite este análisis?

✔️ Detectar mercados más sensibles a eventos negativos
✔️ Ajustar exposición geográfica
✔️ Construir sistemas de alerta más precisos

---

📉 Porque en trading global, el riesgo no solo está en el activo…
está en el contexto donde opera.

---

#Quant #Trading #DataScience #RiskManagement #Volatility #GlobalMarkets #Finanzas
