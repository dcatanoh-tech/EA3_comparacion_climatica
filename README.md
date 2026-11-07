# EA3 – Comparación de datos climáticos: Medellín y Madrid (2024)

Analítica de Datos – IU Digital de Antioquia
Daniela Cataño Hernández · John Freddy Ocampo Ochoa · Óscar Alonso De La Pava Suárez

**Pregunta guía:** ¿Qué similitudes y diferencias se observan en las variables climáticas de Medellín y Madrid durante el mismo periodo?

## Contenido

| Ruta | Descripción |
|---|---|
| `EA3_comparacion_climatica/EA3_Catano_Daniela.ipynb` | Notebook ejecutado: planteamiento, carga y revisión, análisis con NumPy, tres gráficas e interpretación. |
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

Abrir `EA3_comparacion_climatica/EA3_Catano_Daniela.ipynb` con esa carpeta como directorio de trabajo y ejecutar **Restart → Run All**. El notebook usa los CSV de `datos/`; si no existen, los descarga desde los enlaces anteriores.
