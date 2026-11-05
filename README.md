# EDA paso a paso: Premier League 2015/16 con datos de StatsBomb

Análisis exploratorio de datos (EDA) completo, explicado en español, sobre la temporada en que el Leicester City ganó la Premier League con cuotas de 5000 a 1. Usa los [datos abiertos de StatsBomb](https://github.com/statsbomb/open-data).

Cada paso tiene tres partes: **qué hacemos y por qué**, el código, y **qué vemos** en el resultado.

## Contenido

| Paso | Pregunta |
|---|---|
| 1 | ¿Qué queremos saber? |
| 2-3 | Carga de datos y primera mirada |
| 4 | Calidad de datos y reglas del dominio |
| 5 | Variables derivadas y validación contra la tabla oficial |
| 6 | Univariado (los goles siguen una Poisson) |
| 7 | Bivariado (ventaja de local, diferencia de gol vs. puntos) |
| 8 | Evolución en el tiempo |
| 9 | Casos atípicos |
| 10 | Eventos del Leicester: tiros, xG, mapa de ocasiones |
| 11 | Conclusiones y límites |

## Algunos hallazgos

- 2,7 goles por partido; el local gana el 41 %, empata el 28 % y pierde el 31 %.
- La diferencia de gol explica el 92 % de la variación de puntos (r = 0,96).
- El ataque del Leicester rindió lo esperado (68 goles con 66,3 xG); su defensa recibió 10 goles menos que los esperados (36 con 46,1).

## Cómo correrlo

```bash
pip install -r requirements.txt
jupyter notebook EDA_Premier_League_2015_16.ipynb
```

El notebook descarga los JSON necesarios a `data_pl/` la primera vez (~105 MB) y los reutiliza después.

## Datos

Datos de [StatsBomb Open Data](https://github.com/statsbomb/open-data). Si publicás análisis o gráficos basados en ellos, StatsBomb pide citar la fuente y usar su logo; revisá los [términos de uso](https://github.com/statsbomb/open-data/blob/master/LICENSE.pdf).
