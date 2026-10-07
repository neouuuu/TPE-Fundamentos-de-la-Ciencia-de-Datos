# TPE – Fundamentos de la Ciencia de Datos (2026)

Trabajo Práctico Especial: análisis del conjunto de datos **CKF-NHANES** sobre enfermedad renal crónica (CKD/CKF), a partir de datos de la encuesta poblacional de salud y nutrición NHANES de Estados Unidos (2021-2023).

## Integrantes (Grupo XX)

- Allende, Neo
- Maiarú, Francisco
- Lara Lambrecht, Manuel

## Contenido del repositorio

```
.
├── README.md                 # Este archivo
├── requirements.txt          # Dependencias de Python (pip)
├── Informe_TPE_Grupo_XX.docx # Informe con hallazgos y conclusiones (agregar también el PDF si corresponde)
├── TPE_Grupo_XX.ipynb        # Notebook de Jupyter con todo el análisis
└── data/
    └── <archivo_de_datos>.csv  # Conjunto de datos CKF-NHANES
```

> **Pendiente:** ajustar los nombres de archivo de esta sección a los definitivos.

## Qué hace el trabajo

La notebook implementa, organizada en secciones, los requerimientos del enunciado:

1. Análisis exploratorio inicial de los datos (origen, atributos, distribuciones, outliers y valores nulos).
2. Limpieza de la base, con la justificación de cada acción.
3. Planteo de tres hipótesis propias (univariada, bivariada y multivariada).
4. Validación de las tres hipótesis propias y de las tres provistas por la cátedra.

El informe referencia explícitamente las secciones de la notebook en las que se realiza cada cálculo.

## Requisitos previos

- **Python 3.X** (completar con la versión usada, por ejemplo 3.11).
- `pip` y `venv` (incluidos en las instalaciones estándar de Python).
- Jupyter (se instala con `requirements.txt`).

## Instrucciones de ejecución

### 1. Clonar el repositorio

```bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_REPOSITORIO>
```

### 2. Crear y activar un entorno virtual

Linux / macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Windows (PowerShell):

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

Windows (cmd):

```bat
python -m venv .venv
.venv\Scripts\activate.bat
```

### 3. Instalar las dependencias

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Verificar que el archivo de datos esté en su lugar

El archivo de datos se incluye en el repositorio, en la carpeta `data/`. La notebook lo lee mediante una ruta **relativa** (`data/<archivo_de_datos>.csv`), por lo que debe ejecutarse desde la raíz del repositorio y no hace falta modificar ninguna ruta.

### 5. Abrir y ejecutar la notebook

```bash
jupyter notebook TPE_Grupo_XX.ipynb
```

(o `jupyter lab TPE_Grupo_XX.ipynb`). Una vez abierta, ejecutar todas las celdas en orden con **Kernel → Restart & Run All**. La notebook debe correr de principio a fin sin errores ni intervención manual.

Alternativa por línea de comandos, sin abrir la interfaz:

```bash
jupyter nbconvert --to notebook --execute TPE_Grupo_XX.ipynb --output TPE_Grupo_XX_ejecutada.ipynb
```

## Estructura de la notebook

> **Pendiente:** completar con las secciones reales cuando esté terminada la notebook y mantenerlas sincronizadas con las referencias del informe.

| Sección | Contenido |
| --- | --- |
| 1 | Carga de datos y análisis exploratorio |
| 2 | Limpieza de la base |
| 3 | Hipótesis 1 (univariada) |
| 4 | Hipótesis 2 (bivariada) |
| 5 | Hipótesis 3 (multivariada) |
| 6 | Hipótesis 4: casos de CKF según grupo étnico |
| 7 | Hipótesis 5: presión arterial como factor de riesgo |
| 8 | Hipótesis 6: vínculo de edad, sexo, BMI, presión arterial, diabetes, tabaquismo y nivel socioeconómico con CKD |
| 9 | Conclusiones |

## Sobre los datos

Cada fila corresponde a una persona examinada en la encuesta NHANES 2021-2023. Las columnas combinan datos demográficos, medidas corporales, presión arterial, análisis de sangre y orina, antecedentes declarados y variables derivadas de función renal (eGFR con la ecuación CKD-EPI 2021, `ckd_stage` y `ckd_present`). El diccionario completo de variables se encuentra en el informe y en la documentación provista por la cátedra.

## Notas

- Una asociación observada en estos datos no demuestra causalidad.
- Fuente de los datos: NHANES, Centers for Disease Control and Prevention (CDC) / National Center for Health Statistics (NCHS). https://www.cdc.gov/nchs/nhanes/
