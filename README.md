#  TelecomX LATAM — Análisis de Evasión de Clientes (Churn)

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=flat-square&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7-orange?style=flat-square)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-4c72b0?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completado-success?style=flat-square)

---

##  Descripción del Proyecto

Este proyecto forma parte del **Challenge de Data Science — LATAM** y tiene como objetivo analizar el comportamiento de evasión de clientes (**churn**) de la empresa de telecomunicaciones **TelecomX**.

A través de un proceso completo de **ETL (Extracción, Transformación y Carga)** y **Análisis Exploratorio de Datos (EDA)**, se identificaron los principales factores que llevan a los clientes a cancelar sus servicios, generando insights accionables para reducir la tasa de evasión.

---

##  Objetivos

- Extraer y procesar datos de clientes desde una API en formato JSON
- Limpiar y transformar el dataset para garantizar calidad en el análisis
- Identificar patrones y factores asociados a la evasión de clientes
- Proponer recomendaciones estratégicas basadas en los hallazgos

---

##  Estructura del Repositorio

```
TelecomX_LATAM/
│
├──  TelecomX_LATAM.ipynb       # Notebook principal con todo el análisis
├──  TelecomX_Data.json         # Dataset de clientes (fuente: API)
├──  TelecomX_diccionario.md    # Diccionario de datos
└──  README.md                  # Este archivo
```

---

##  Diccionario de Datos

| Columna | Descripción |
|---|---|
| `customerID` | ID único del cliente |
| `Churn` | Si el cliente dejó o no la empresa |
| `gender` | Género del cliente |
| `SeniorCitizen` | Si el cliente tiene 65 años o más |
| `Partner` | Si tiene pareja |
| `Dependents` | Si tiene dependientes |
| `tenure` | Meses de contrato |
| `PhoneService` | Suscripción al servicio telefónico |
| `InternetService` | Tipo de servicio de internet |
| `Contract` | Tipo de contrato (mes a mes, anual, bianual) |
| `PaymentMethod` | Método de pago |
| `Charges.Monthly` | Cargo mensual total |
| `Charges.Total` | Total gastado por el cliente |

>  Ver diccionario completo en [`TelecomX_diccionario.md`](TelecomX_diccionario.md)

---

##  Pipeline del Proyecto

```
 EXTRACCIÓN            TRANSFORMACIÓN              ANÁLISIS
──────────────         ──────────────────         ──────────────────
API JSON         →     Aplanar JSON         →     Estadísticas
requests               Limpiar nulos              descriptivas
pd.json_normalize      Eliminar duplicados        Visualizaciones
                       Convertir tipos            Análisis Churn
                       Crear Cuentas_Diarias      Insights
                       Estandarizar/Traducir      Recomendaciones
```

---

##  Principales Hallazgos

###  Tasa de Evasión General
> Aproximadamente el **26% de los clientes** cancelaron el servicio.

###  Factores más relevantes detectados:

| Factor | Hallazgo | Impacto |
|---|---|---|
| **Tipo de Contrato** | Clientes mes a mes tienen ~43% de evasión |  Alto |
| **Servicio de Internet** | Fibra óptica presenta mayor tasa de churn |  Alto |
| **Método de Pago** | Cheque electrónico asociado a ~45% de evasión |  Alto |
| **Tiempo de Contrato** | Los primeros 12 meses son el período crítico |  Medio |
| **Cargo Mensual** | Clientes que se van pagan cargos más altos |  Medio |

---

##  Recomendaciones Estratégicas

1. **Incentivar contratos anuales o bianuales** con descuentos y beneficios exclusivos
2. **Programa de fidelización en los primeros 12 meses** (soporte prioritario, descuentos)
3. **Revisar la calidad del servicio de Fibra Óptica** ante su alta tasa de evasión
4. **Migrar clientes a métodos de pago automático** con incentivos (mes gratis, cashback)
5. **Segmentar campañas de retención** enfocadas en perfiles de alto riesgo

---

##  Tecnologías Utilizadas

| Herramienta | Uso |
|---|---|
| `Python 3.10+` | Lenguaje principal |
| `Pandas` | Manipulación y limpieza de datos |
| `Matplotlib` | Visualizaciones |
| `Seaborn` | Gráficos estadísticos |
| `Requests` | Extracción de datos desde la API |
| `Jupyter Notebook` | Entorno de desarrollo |

---

##  Cómo Ejecutar el Proyecto

**1. Clonar el repositorio**
```bash
git clone https://github.com/tu-usuario/TelecomX_LATAM.git
cd TelecomX_LATAM
```

**2. Instalar dependencias**
```bash
pip install pandas matplotlib seaborn requests jupyter
```

**3. Abrir el notebook**
```bash
jupyter notebook TelecomX_LATAM.ipynb
```

**4. Ejecutar todas las celdas en orden**
> `Kernel` → `Restart & Run All`

---

##  Juan Camilo Mantilla Ramirez

Hecho con cariño como parte del **Challenge de Data Science — Alura LATAM + Oracle ONE**

---
