# Análisis de Redes Sociales del Trap Argentino en X (Twitter)

Este repositorio contiene el código utilizado para el análisis y visualización de una red social construida a partir de tweets relacionados con la escena del *trap argentino*. El objetivo del trabajo es identificar comunidades, detectar nodos centrales y extraer conclusiones a partir de datos reales obtenidos mediante web scraping.

---

##  Objetivo

Analizar la estructura de las conversaciones sobre el trap argentino en la plataforma X (Twitter) para:

- Detectar comunidades y fandoms conectados
- Analizar las palabras clave más co-ocurrentes
- Identificar los nodos más importantes
- Visualizar la red de interacciones y temas

---

##  Dataset

Se recolectaron **2843  tweets** con Selenium y `undetected_chromedriver` a partir de una lista de palabras clave y hashtags relacionados con:

- Artistas de trap argentino (Duki, YSY A, Bizarrap, etc.)
- Polémicas y conflictos entre fandoms
- Eventos relevantes de la escena
- Comportamientos virales y comunidades

---

##  Estructura del repositorio

📂 trap-argentino-red-social

├── data/

│   └── tweets_trap_argentino.csv          # Tweets scrapeados con keywords

│   └── nodos_temas.csv                    # Nodos (palabras clave)

│   └── aristas_temas.csv                  # Aristas (co-ocurrencias)


├── src/

│   └── scraper.py                         # Código de scraping con Selenium

│   └── analisis_red_y_visualizacion.py                    # Construcción y análisis de red y visualización con NetworkX y matplotlib

└── README.md



---

##  Análisis de red

- Red construida por co-ocurrencia de palabras clave dentro de los tweets
- Detección de comunidades con el algoritmo de **Louvain**
- Medidas de centralidad calculadas:
  - 🔹 Grado
  - 🔹 Intermediación (betweenness)
  - 🔹 Cercanía (closeness)

---

##  Visualización

- Grafo con nodos coloreados según comunidad detectada
- Tamaño de nodo proporcional a su centralidad
- Layout utilizado: `spring_layout` (posición de nodos según fuerzas)

---

##  Conclusiones

- Las comunidades giran en torno a fandoms de artistas clave (Duki, YSY A, Paulo Londra)
- Algunas palabras clave actúan como puentes entre fandoms o controversias
- Las polémicas y conflictos (como YSYSMO) generan estructuras densas

---




