# InsightReach: segmentación de clientes de restaurantes

**Proyecto Integrador · Módulo 1 · Data Science (Henry)**
Autora: Laura Garmendia · Octubre de 2026

Análisis de datos para una empresa de marketing digital: integración de una base de clientes de restaurantes con la oferta real de la ciudad, obtenida de la API de Yelp, para responder **a qué clientes dirigir cada campaña de marketing y con qué propuesta**.

> 📄 **Documentación completa:** [README.pdf](DOCUMENTACION/README.pdf) (metodología, criterios, funciones y resultados) · [Recomendaciones.pdf](DOCUMENTACION/Recomendaciones.pdf) (propuestas para el cliente)

---

## Contexto

**InsightReach** diseña campañas personalizadas para negocios locales y busca mejorar su estrategia de segmentación. A partir de su base de **30.000 clientes de restaurantes en 10 ciudades de EE. UU.**, se eligió **Chicago** (la ciudad con más clientes), se limpiaron y transformaron los datos, se integraron con **920 restaurantes de Yelp** y se analizaron para proponer segmentos accionables.

## Resultados principales

- **El estrato socioeconómico ordena el consumo.** Las relaciones aparentes entre frecuencia, ingreso y gasto desaparecen dentro de cada estrato.
- **El valor está concentrado:** en Chicago, el 17 % de los clientes (estrato Muy Alto) genera el 50 % del gasto en restaurantes.
- **Chicago gasta menos por visita:** con el mismo ingreso y las mismas visitas, el estrato Medio gasta 17,5 USD por comida contra 25,5 USD en las otras ciudades.
- **Demanda sin atender:** 392 clientes vegetarianos y veganos de alto gasto no tienen restaurantes en su rango de precio.
- **Campaña a enfatizar: alta gama.** Retener al estrato Muy Alto y abrir oferta vegetariana y vegana premium (22 % de los clientes, 58 % del gasto), con una estrategia específica para cada estrato.

## Estructura del repositorio

```
ProyectoM1_LauraGarmendia/
├── AVANCES/
│   ├── Avance_EDA_Laura_Garmendia.ipynb       Avances 1 y 3: exploración, limpieza, análisis y segmentación
│   └── Avance_API_Yelp_Laura_Garmendia.ipynb  Avance 2: integración con la API de Yelp
├── ARCHIVOS/
│   ├── base_datos_restaurantes_USA_v2.csv     Base original
│   ├── clientes_chicago_limpio.csv            Salida del Avance 1
│   ├── yelp_chicago_raw.json                  Respuesta de la API (caché)
│   ├── yelp_chicago_negocios.csv              Restaurantes de Yelp limpios
│   └── clientes_chicago_enriquecido.csv       Clientes + oferta de Yelp
└── DOCUMENTACION/
    ├── README.pdf                             Documentación técnica completa
    └── Recomendaciones.pdf                    Propuestas de segmentación
```

## Cómo ejecutarlo

1. Clonar o descargar el repositorio completo, conservando la estructura de carpetas.
2. Instalar Python 3 y las librerías `pandas`, `numpy`, `matplotlib`, `seaborn` y `requests`.
3. Abrir los notebooks de `AVANCES` en Jupyter o VS Code y ejecutar con *Run All*. Los datos se leen de `ARCHIVOS` mediante una ruta relativa.
4. El notebook de Yelp usa la respuesta guardada en `yelp_chicago_raw.json`, así que **no necesita API key**. La clave nunca se escribe en el código: si se quisieran descargar datos nuevos, se pide de forma oculta.

## Tecnologías

Python 3 · Jupyter Notebook · VS Code · pandas · numpy · matplotlib · seaborn · requests · Yelp Places API
