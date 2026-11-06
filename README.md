# ETL_PandasNumpy

🛠️ ETL Pipeline & Data Quality (Arquitectura Medallón - Capa Silver)

## 📌 Descripción
Pipeline de Extracción, Transformación y Carga (ETL) desarrollado en Python (**Pandas y NumPy**) enfocado en la limpieza, estandarización y gobernanza 

El proyecto toma un dataset crudo (Bronze) con inconsistencias de codificación, tipos de datos ambiguos y registros duplicados, transformándolo en un dataset limpio, tipado e íntegro (**Capa Silver**).

---

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3.14
* **Entorno:** Jupyter Notebook
* **Librerías:** Pandas, NumPy
* **Estándar:** DAMA-DMBOK & Medallion Architecture Enfoque en silver


## 📐 Reglas de Transformación Aplicadas

1. **Tipado Estricto (`dtype`):** Asignación explícita de tipos de datos en la carga inicial.
2. **Higiene de Cadenas & Encoding:** Corrección de *mojibake* (`Ã³`) e incorporación de `utf-8-sig` para la correcta visualización de acentos y eñes (`Ana Gómez`, `Ciudad Obregón`).
3. **Estandarización de Fechas:** Parseo estricto a objetos `datetime64`.
4. **Precisión Financiera:** Redondeo del `Monto` a **2 decimales**.
5. **Deduplicación:** Control de calidad sobre la PK (`Id_Transaccion`) consolidando **12,430 registros limpios**.

---

## 📁 Archivos en el Repositorio
* `ETL.ipynb`: Cuaderno principal con la ejecución paso a paso del proceso de limpieza.
* `Capa_Silver_Transacciones.csv`: Dataset resultante procesado y listo para consumo analítico.
