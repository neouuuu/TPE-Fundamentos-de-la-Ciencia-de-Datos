# TPE – Fundamentos de la Ciencia de Datos (2026)

Trabajo Práctico Especial: análisis del conjunto de datos **CKF-NHANES** sobre enfermedad renal crónica (CKD/CKF), a partir de datos de la encuesta poblacional de salud y nutrición NHANES de Estados Unidos (2021-2023).

## Integrantes (Grupo XX)

- Allende, Neo
- Maiarú, Francisco
- Lara Lambrecht, Manuel

## Contenido del repositorio

```
.
├── README.md                    # Este archivo
├── requirements.txt             # Dependencias de Python (pip)
├── TPE_Ciencia_de_Datos.ipynb   # Notebook de Jupyter con todo el análisis
├── Informe.docx                 # Informe con hallazgos y conclusiones
├── dataset.csv                  # Conjunto de datos CKF-NHANES
├── metadata.docx                # Guía de contexto y diccionario de variables (material de la cátedra)
└── .gitignore
```

## Qué hace el trabajo

La notebook implementa, organizada en secciones, los requerimientos del enunciado:

1. Análisis exploratorio inicial de los datos (origen, atributos, distribuciones, outliers y valores nulos).
2. Limpieza de la base, con la justificación de cada acción.
3. Planteo de tres hipótesis propias (univariada, bivariada y multivariada).
4. Validación de las tres hipótesis propias y de las tres provistas por la cátedra.

El informe (`Informe.docx`) referencia explícitamente las secciones de la notebook en las que se realiza cada cálculo.

## Requisitos previos

- **Python 3.X** (completar con la versión usada, por ejemplo 3.11).
- `pip` y `venv` (incluidos en las instalaciones estándar de Python).
- Git, para clonar el repositorio.

Jupyter y el resto de las librerías se instalan con `requirements.txt`.

## Instrucciones de ejecución

### 1. Clonar el repositorio

```bash
git clone https://github.com/neouuuu/TPE-Fundamentos-de-la-Ciencia-de-Datos.git
cd TPE-Fundamentos-de-la-Ciencia-de-Datos
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

### 4. Verificar el archivo de datos

El archivo de datos (`dataset.csv`) está incluido en la raíz del repositorio. La notebook lo lee con una ruta **relativa** (`dataset.csv`), por lo que debe abrirse y ejecutarse desde la raíz del repositorio. No hace falta modificar ninguna ruta.

### 5. Abrir y ejecutar la notebook

```bash
jupyter notebook TPE_Ciencia_de_Datos.ipynb
```

(o `jupyter lab TPE_Ciencia_de_Datos.ipynb`). Una vez abierta, ejecutar todas las celdas en orden con **Kernel → Restart & Run All**. La notebook corre de principio a fin sin errores ni intervención manual.

Alternativa por línea de comandos, sin abrir la interfaz:

```bash
jupyter nbconvert --to notebook --execute TPE_Ciencia_de_Datos.ipynb --output TPE_Ciencia_de_Datos_ejecutada.ipynb
```

## Estructura de la notebook

> **Pendiente:** reemplazar esta tabla por las secciones reales de la notebook y mantenerlas sincronizadas con las referencias del informe.

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

Cada fila corresponde a una persona examinada en la encuesta NHANES 2021-2023. Las columnas combinan datos demográficos, medidas corporales, presión arterial, análisis de sangre y orina, antecedentes declarados y variables derivadas de función renal (eGFR con la ecuación CKD-EPI 2021, `ckd_stage` y `ckd_present`). El diccionario completo de variables se encuentra en `metadata.docx`.

## Notas

- Una asociación observada en estos datos no demuestra causalidad.
- Fuente de los datos: NHANES, Centers for Disease Control and Prevention (CDC) / National Center for Health Statistics (NCHS). https://www.cdc.gov/nchs/nhanes/
