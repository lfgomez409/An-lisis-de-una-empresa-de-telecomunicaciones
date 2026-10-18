# 📊 Proyecto 6 — Análisis de una empresa de telecomunicaciones (ConnectaTel)

---

## 📂 Introducción
Eres analista de datos en **ConnectaTel**, una empresa de telecomunicaciones con operaciones en México y Colombia.  
El objetivo del proyecto es entender cómo los clientes usan realmente los servicios móviles (llamadas y mensajes) para:

- Identificar patrones de uso.  
- Detectar comportamientos atípicos (outliers).  
- Comprender qué segmentos de clientes muestran necesidades diferenciadas.  

La meta final es **optimizar la oferta comercial y mejorar la experiencia del usuario**.

---

## 💡 Preguntas del negocio
- ¿Qué segmentos de clientes muestran mayor o menor uso de llamadas y mensajes?  
- ¿Qué usuarios presentan valores atípicos que puedan indicar comportamientos inusuales, fraude o errores de registro?  
- ¿Cómo varía el uso según la edad y el tipo de plan contratado?  
- ¿Qué patrones pueden ayudar a diseñar mejores planes, optimizar la oferta y mejorar la satisfacción del cliente?  

---

## 🎯 Objetivos de aprendizaje
Al finalizar este proyecto serás capaz de:  
- Integrar y limpiar bases de datos provenientes de tres fuentes distintas.  
- Aplicar técnicas de validación, estandarización de tipos de datos y detección de valores inconsistentes.  
- Construir un perfil estadístico del uso (llamadas y mensajes) por cliente y por segmentos demográficos.  
- Detectar outliers y comportamientos atípicos mediante métodos estadísticos y visuales.  
- Crear segmentaciones de clientes basadas en edad, país y comportamiento de uso.  
- Visualizar diferencias entre segmentos y extraer insights comerciales relevantes.  
- Documentar todo el proceso en un Jupyter Notebook, junto con un README reproducible para subirlo a GitHub.  

---

## 🛠️ Herramientas
- **Jupyter Notebook**  
- **Python**: pandas, numpy, seaborn, matplotlib  
- **GitHub** para documentación y versionado  

---

## 📂 Datasets
1. **plans.csv** → catálogo de planes (precio, minutos incluidos, GB incluidos, costo por extra).  
2. **users_latam.csv** → información de clientes (edad, ciudad, fecha de registro, plan contratado, churn).  
3. **usage.csv** → detalle de uso real (llamadas: duración, mensajes: longitud).  

---

## 🔄 Flujo general del proyecto
| Paso | Acción | Resultado |
|------|--------|-----------|
| 1 | Cargar y explorar datasets | Visión clara de estructura y tipos de columna |
| 2 | Identificación de problemas de calidad | Lista priorizada de problemas que pueden sesgar decisiones |
| 3 | Limpieza básica | Datos consistentes y listos para análisis |
| 4 | Estadísticas descriptivas | Medidas clave de comportamiento típico y extremo |
| 5 | Visualización & outliers | Histogramas y boxplots para detectar patrones |
| 6 | Segmentación | Grupos accionables para diseñar ofertas y campañas |
| 7 | Insight ejecutivo | Conclusiones y recomendaciones comerciales |
| 8 | Publicación | Notebook limpio + README en GitHub |

---

## 📊 Insights ejecutivos

### ⚠️ Problemas detectados
- Valores faltantes en `city`: 469 registros (≈11,7%).  
- Edad inválida (-999) → reemplazada por mediana.  
- Fechas futuras en `reg_date`: 40 registros en 2026 (≈1%) → excluidos.  
- Valores faltantes estructurales en `usage`:  
  - `duration`: 22.076 (55,2%).  
  - `length`: 17.896 (44,7%).  
- Tipos de datos erróneos en fechas → corregidos.  

### 🔍 Segmentos por Edad
- **Jóvenes (<30 años):** uso intensivo de mensajería y servicios digitales.  
- **Adultos (30–59 años):** consumo equilibrado, segmento predominante.  
- **Adultos mayores (≥60 años):** menor actividad, preferencia por llamadas tradicionales.  

### 📊 Segmentos por Nivel de Uso
- **Bajo uso:** bajo consumo, candidatos a planes económicos.  
- **Uso medio:** consumo regular, base principal de clientes.  
- **Alto uso (~20%):** concentran más del 50% de ingresos, clientes más valiosos.  

### 🚨 Outliers
- Usuarios con llamadas y mensajes muy superiores al promedio.  
- No son errores de captura, sino clientes intensivos.  
- Implican oportunidad de planes premium y necesidad de monitoreo.  

---

## 📌 Implicaciones
- Los clientes **no son homogéneos**: edad y nivel de uso definen patrones claros.  
- El **Plan Básico (64,9%)** domina la base, pero no satisface plenamente a los segmentos de alto consumo.  
- Los **clientes de alto uso** son críticos para la rentabilidad y requieren estrategias de fidelización.  
- Los **outliers** son señales de oportunidad y de riesgo.  

---

## 💡 Recomendaciones
1. Diseñar **planes diferenciados por perfil de uso** (básicos, balanceados, premium).  
2. Implementar **estrategias de upselling** para migrar clientes de alto consumo hacia planes premium.  
3. Crear **ofertas específicas por edad**:  
   - Jóvenes → más beneficios en mensajería y servicios digitales.  
   - Adultos → planes balanceados.  
   - Adultos mayores → planes simplificados con minutos incluidos.  
4. Desarrollar **programas de fidelización** para clientes intensivos.  
5. Mejorar la **validación de datos** en el registro de clientes para reducir errores futuros.  

---

## 📂 Recursos
- 📌 [Repositorio en GitHub](https://github.com/lfgomez409/An-lisis-de-una-empresa-de-telecomunicaciones)  
- 📌 Notebook del análisis (`Proyecto6_ConnectaTel.ipynb`)  
- 📌 Carpeta de datasets (`/data/`)  

---

## ✅ Conclusión
ConnectaTel puede **maximizar ingresos y satisfacción** si ajusta su oferta a los segmentos detectados, fortalece la retención de clientes intensivos y controla los outliers con procesos de validación más robustos.
