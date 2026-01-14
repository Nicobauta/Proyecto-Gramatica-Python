# Sistema de Análisis y Evaluación de Expresiones usando Gramáticas en Python

Este proyecto implementa un **sistema de análisis sintáctico y evaluación de expresiones matemáticas** utilizando **gramáticas formales** y **ANTLR4** con generación de código en **Python**.

El sistema define una **gramática personalizada**, genera automáticamente el **lexer y parser**, y permite procesar archivos de entrada para **validar, interpretar y evaluar expresiones**, con fines académicos en el estudio de **lenguajes formales y compiladores**.

---

## Características principales

- Definición de una **gramática formal (.g4)**
- Generación automática de:
  - Lexer
  - Parser
  - Visitor
  - Listener
- Evaluación de expresiones matemáticas
- Procesamiento de archivos de entrada (`.txt`, `.csv`)
- Arquitectura basada en **ANTLR + Python**
- Separación clara entre:
  - Gramática
  - Lógica de ejecución
  - Datos de prueba

---

## Arquitectura del sistema

Archivo de entrada  
↓  
Lexer (tokenización)  
↓  
Parser (análisis sintáctico)  
↓  
Árbol de sintaxis (AST)  
↓  
Visitor / Evaluador  
↓  
Resultado de la expresión  

---

## Tecnologías utilizadas

- **Python 3**
- **ANTLR4**
- **Gramáticas formales (.g4)**
- **CSV / TXT**
- **ANTLR Runtime para Python**

---

## Estructura del proyecto

```
Proyecto-Gramatica-Python-main/
├── calculadora.g4
├── calculadoraLexer.py
├── calculadoraParser.py
├── calculadoraVisitor.py
├── calculadoraListener.py
├── calculadora.tokens
├── calculadoraLexer.tokens
├── calculadora.interp
├── calculadoraLexer.interp
│
├── main.py
│
├── datos.csv
├── prueba.csv
├── ejemplo.txt
├── quijote
│
├── requirements.txt
├── sustentacion.txt
└── README.md

```



---

## Descripción de los componentes principales

### `calculadora.g4`
Archivo que define la **gramática formal** del lenguaje de expresiones matemáticas, incluyendo:
- Reglas sintácticas
- Tokens
- Operadores
- Prioridad de operaciones

---

### Archivos generados por ANTLR

- `calculadoraLexer.py`: Tokeniza la entrada
- `calculadoraParser.py`: Analiza la estructura sintáctica
- `calculadoraVisitor.py`: Implementa la lógica de recorrido del árbol
- `calculadoraListener.py`: Manejo de eventos del parser

Estos archivos son generados automáticamente a partir de la gramática `.g4`.

---

### `main.py`
Archivo principal del proyecto.

Funciones principales:
- Lectura de archivos de entrada
- Ejecución del lexer y parser
- Evaluación de expresiones
- Manejo de errores sintácticos

---

### Archivos de datos

- `ejemplo.txt`: Ejemplos de expresiones a evaluar
- `datos.csv` / `prueba.csv`: Datos de prueba estructurados
- `quijote`: Archivo de texto usado como prueba adicional
- `sustentacion.txt`: Documento de apoyo académico

---

## Funcionalidades del sistema

### Análisis léxico

- Identifica tokens válidos
- Detecta errores léxicos

---

### Análisis sintáctico

- Valida la estructura de las expresiones
- Construye el árbol de sintaxis (AST)

---

### Evaluación de expresiones

- Ejecuta operaciones matemáticas
- Respeta precedencia de operadores
- Retorna resultados correctos o errores

---

## Ejecución del proyecto

```bash
# 1. Acceder al directorio del proyecto
cd Proyecto-Gramatica-Python-main

# 2. (Opcional) Crear un entorno virtual
python -m venv venv

# 3. Activar el entorno virtual
# Linux / macOS
source venv/bin/activate

# Windows
venv\Scripts\activate

# 4. Instalar dependencias
pip install -r requirements.txt

# 5. Ejecutar el programa principal
python main.py
