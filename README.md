# EA3 – Comparación de datos climáticos: Medellín y Madrid (2024)

Analítica de Datos – IU Digital de Antioquia
Daniela Cataño Hernández · John Freddy Ocampo Ochoa · Óscar Alonso De La Pava Suárez

**Pregunta guía:** ¿Qué similitudes y diferencias se observan en las variables climáticas de Medellín y Madrid durante el mismo periodo?

## Contenido

| Ruta | Descripción |
|---|---|
| `EA3_comparacion_climatica/EA3_GRUPO_3.ipynb` | Notebook ejecutado: planteamiento, carga y revisión, análisis con NumPy, tres gráficas e interpretación. |
| `EA3_comparacion_climatica/datos/medellin.csv` | Datos diarios de Medellín, 2024-01-01 a 2024-12-31. |
| `EA3_comparacion_climatica/datos/ciudad_otro_pais.csv` | Datos diarios de Madrid (España), mismo periodo. |

Columnas de ambos CSV: `fecha`, `tmax_c`, `tmin_c`, `tmedia_c` (°C) y `precip_mm` (mm).

## Fuente de los datos

Open-Meteo, *Historical Weather API* (reanálisis ERA5 / ERA5-Land de Copernicus): https://open-meteo.com/en/docs/historical-weather-api

- Medellín: https://archive-api.open-meteo.com/v1/archive?latitude=6.2518&longitude=-75.5636&start_date=2024-01-01&end_date=2024-12-31&daily=temperature_2m_max,temperature_2m_min,temperature_2m_mean,precipitation_sum&timezone=America%2FBogota&temperature_unit=celsius&precipitation_unit=mm
- Madrid: https://archive-api.open-meteo.com/v1/archive?latitude=40.4168&longitude=-3.7038&start_date=2024-01-01&end_date=2024-12-31&daily=temperature_2m_max,temperature_2m_min,temperature_2m_mean,precipitation_sum&timezone=Europe%2FMadrid&temperature_unit=celsius&precipitation_unit=mm

## Cómo ejecutar

```bash
pip install numpy pandas matplotlib jupyter
```

Abrir `EA3_comparacion_climatica/EA3_GRUPO_3.ipynb` con esa carpeta como directorio de trabajo y ejecutar **Restart → Run All**. El notebook usa los CSV de `datos/`; si no existen, los descarga desde los enlaces anteriores.

## Resultados principales (2024)

| Indicador | Medellín | Madrid |
|---|---|---|
| Temperatura media anual | 20,8 °C | 15,8 °C |
| Mes más frío → mes más cálido | 19,7 °C (nov) → 22,1 °C (mar) | 6,2 °C (dic) → 28,4 °C (ago) |
| Temperaturas extremas | 13,9 °C / 31,8 °C | −2,6 °C / 40,4 °C |
| Precipitación total | 2.176 mm | 491 mm |
| Días lluviosos (≥ 1 mm) | 259 | 80 |

- **Diferencia:** la temperatura de Madrid cambia 22,2 °C entre su mes más frío y el más cálido; la de Medellín, solo 2,5 °C.
- **Similitud:** en junio y septiembre las medias mensuales de ambas ciudades quedaron a menos de 2 °C, y la amplitud térmica diaria es parecida (10,6 °C en Medellín y 11,5 °C en Madrid).
- **Diferencia:** Medellín acumuló 4,4 veces más lluvia, con dos temporadas húmedas (máximos en mayo y noviembre); Madrid no registró lluvia en julio.

Son asociaciones observadas en un solo año de datos de reanálisis; no permiten afirmar causas ni describen el clima de largo plazo.
