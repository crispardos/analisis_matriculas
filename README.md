# Análisis de Matrículas — Educación Superior (Arica y Parinacota, 2021)

Proyecto de estadística descriptiva (MAT4141). Análisis exploratorio de la matrícula
en educación superior de la región de Arica y Parinacota.

## Requisitos

Para que todos trabajemos con las **mismas versiones de Python y librerías**, el
proyecto usa [uv](https://docs.astral.sh/uv/) como gestor de dependencias.

### 1. Instalar uv

**Linux / macOS** (terminal):

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows** (PowerShell):

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Después de instalar, cierra y vuelve a abrir la terminal para que `uv` esté
disponible en el PATH.

> No necesitas instalar Python aparte: uv descarga automáticamente la versión
> correcta (definida en `.python-version`).

### 2. Instalar las dependencias

Clona el repositorio y dentro de la carpeta del proyecto:

```bash
uv sync
```

Este comando crea el entorno virtual `.venv` e instala exactamente las
dependencias fijadas en `uv.lock`. No instales paquetes con `pip` directamente;
si necesitas agregar una librería, avisa al grupo y se agrega con:

```bash
uv add <paquete>
```

## Trabajo con notebooks

Los notebooks están en `notebooks/`. Para abrirlos:

```bash
uv run jupyter lab
# o solo jupyter:
uv run jupyter notebook
```

Ejecuta los comandos siempre con `uv run` para que usen el entorno del proyecto
y no un Python global.

## Estructura del repositorio

```
├── docs/         # Diccionario de variables (PDF)
├── notebooks/    # Análisis en Jupyter y datos
├── src/          # Código del paquete
└── pyproject.toml / uv.lock   # Definición del entorno
```

## Datos

- `raw/01_MATRICULAS_ED_SUPERIOR_ARICA_Y_PARINACOTA_2021.xlsx` — matrículas de
  educación superior 2021, incluido en el repositorio (no requiere descarga).
- `docs/diccionario_variables.pdf` — descripción de cada columna.
