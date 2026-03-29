# 📈Medición del Sesgo Intradía por Sector

Detección de Comportamientos Sistemáticos y Oportunidades de Arbitraje

## 📌Descripción

Este proyecto analiza el sesgo intradía del mercado a nivel sectorial, midiendo el rendimiento promedio entre el precio de apertura y el precio de cierre de las acciones durante la jornada de negociación.

El objetivo es identificar sectores donde:
- El precio tiende a subir consistentemente durante el día (sesgo comprador)
- O, por el contrario, donde el rendimiento intradía es negativo (sesgo vendedor)

Este tipo de análisis es clave para estrategias de trading intradía, especialmente aquellas que operan:
- En la apertura
- En el cierre
- Con rebalanceos diarios

## 🧠 Insight clave

- ¿Qué sector presenta el mayor rendimiento promedio entre la apertura y el cierre, indicando una presión compradora persistente durante la jornada?

Un sesgo intradía positivo sugiere que:
- La demanda se concentra durante el horario regular
- Hay acumulación progresiva (institucional o sistemática)
- El sector puede beneficiarse de estrategias open-to-close

## 📊Valor de negocio

Este análisis aporta valor en:

- Trading intradía y cuantitativo
Identificar sectores con ventaja estadística durante la sesión.

- Estrategias de timing
Decidir si conviene entrar en la apertura o esperar retrocesos.

- Detección de arbitraje estructural
Sesgos persistentes pueden indicar ineficiencias explotables.

- Análisis de microestructura
Diferenciar sectores dominados por flujo institucional vs. minorista.

## 🗂️Estructura de datos requerida

- precios_diarios
- ticker_id
- fecha
- open
- close
- tickers
- ticker_id
- sector

## ⚙️Lógica del análisis

- Cálculo del rendimiento intradía

(Precio de Cierre − Precio de Apertura) / Precio de Apertura


- Ventana temporal

Se analizan los datos del último mes para capturar patrones recientes.

- Agregación sectorial

Se calcula el promedio del rendimiento intradía por sector.

- Ranking

Los sectores se ordenan de mayor a menor sesgo intradía.

## 📈Interpretación de resultados

- Rendimiento intradía positivo alto
- Fuerte presión compradora durante el día
- Ideal para estrategias buy at open / sell at close
- Rendimiento cercano a cero
- Mercado balanceado
- Poca ventaja intradía estructural

- Rendimiento negativo
- Distribución durante la sesión
- Potencial sesgo vendedor o toma de ganancias

## 🚀Posibles extensiones

- Separar por días de la semana
- Analizar solo días con alto volumen
- Comparar intradía vs. overnight (close-to-open)
- Ajustar por volatilidad o beta sectorial
- Construir un Índice de Sesgo Intradía Sectorial

## 🧪Notas técnicas

Recomendado usar índices en:

precios_diarios (ticker_id, fecha)

*El análisis asume mercados con sesiones bien definidas (no cripto).*

*Puede combinarse con filtros de liquidez para mayor robustez.*

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.

***
⏱️ **El mercado también tiene “personalidad” dentro del día**

No todo ocurre en el largo plazo.
Hay sectores que tienden a subir durante la jornada… y otros que pierden fuerza.

👉 Analicé el **sesgo intradía por sector**, midiendo el rendimiento promedio entre la apertura y el cierre en el último mes.

💡 **Insight clave:**
Algunos sectores muestran un **sesgo sistemático de compra durante el día**, cerrando consistentemente por encima de su precio de apertura.

---

📊 **¿Qué medí?**

* Rendimiento intradía: *(Close - Open) / Open*
* Promedio por sector
* Ventana de análisis: últimos 30 días

---

🧠 **¿Cómo interpretarlo?**

* Sectores con rendimiento intradía positivo → presión compradora durante la jornada
* Sectores con rendimiento negativo → ventas predominantes o toma de ganancias
* Posible evidencia de patrones de comportamiento repetitivos (*intraday bias*)

---

⚡ **¿Por qué importa?**

Porque abre la puerta a estrategias como:

* **Open-to-Close trading**
* Ajuste de timing en ejecuciones institucionales
* Detección de flujos sistemáticos por sector

---

📌 Pregunta para la comunidad:
¿Han identificado sesgos intradía consistentes en ciertos sectores o mercados?

#QuantFinance #Trading #DataScience #StockMarket #Intraday #Analytics #SQL #Alpha
