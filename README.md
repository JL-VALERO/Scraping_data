# Scraping_data

## Tarea 1: Extracción de datos web — Resultados del examen de admisión de la UNMSM

1. What does the project do?
   
   Este proyecto extrae automáticamente los resultados del examen de admisión del sitio web de la UNMSM para una categoría
   de admisión específica. Recopila los datos carrera por carrera, descifra los nombres de los solicitantes que aparecen
   ocultos y consolida toda la información en archivos CSV y Excel.

   
3. How to install the dependencies?
   
    pip install requests beautifulsoup4 pandas openpyxl

import pandas as pd
import time
import requests
import base64          -En el HTML de UNMSM el nombre del postulante esta codificado en base64.

-Herramientas recomendados por codex-openai para web scraping

from bs4 import BeautifulSoup      #Para leer y analizar el HTML 
from urllib.parse import urljoin   #para unir enlaces relativos con la URL base

   
5. How to run the script?
   
   Ejecuta el script python scraper.py
   El script accederá a la página de resultados de la UNMSM, detectará todos los enlaces de resultados profesionales,
   extraerá los datos de cada tabla y generará automáticamente los archivos finales.
   

7. What does the output contain?
   
   El resultado contiene un conjunto de datos consolidado con las siguientes columnas:
   Código, Nombre, Carrera, Puntaje, Mérito EP, Observación e Ingresó. Se exporta como archivo Excel.

   
