# Material docente de la asignatura Programación (PRG)

Este repositorio contiene material docente de la asignatura Programación (PRG) del [Grado en Ingeniería de Datos e Inteligencia Artificial (GIA)](https://www.upv.es/titulaciones/GIAR-A/index-es.html) de [l'Escola Politècnica Superior d'Alcoi (EPSA)](https://www.upv.es/entidades/epsa/) de la [Universitat Politècnica de València (UPV)](https://www.upv.es/).

Este material docente se proporciona en forma de [cuadernos Jupyter](https://jupyter.org/), que combinan texto formateado (markdown) explicativo con código Python modificable y ejecutable. 

Desde GitHub podéis visualizar los cuadernos Jupyter en formato HTML, pero no podréis modificar ni ejecutar los bloques de código. Para más información sobre cómo modificarlos y/o ejecutarlos, véase la sección ["Cómo usar los cuadernos"](#cómo-usar-los-cuadernos).

Como complemento a los contenidos de esta asignatura, para profundizar en el lenguaje Python, podéis consultar el **[Seminario de Python3](https://dsic.gitbook.io/python3)** de Joan Albert Silvestre.

## Índice de contenidos

### Teoría

1. Tipos de datos y librerías avanzados de Python

    1. [Tipos de datos estándar](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.1%20Tipos%20de%20datos%20estándar.ipynb)
    2. [Tuplas](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.2a%20Tuplas.ipynb)
        - [Ejercicios](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.2b%20Ejercicios.ipynb)
        - [Ejercicios resueltos](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.2c%20Ejercicios%20resueltos.ipynb)
    3. [Conjuntos](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.3a%20Conjuntos.ipynb)
        - [Ejercicios](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.3b%20Ejercicios.ipynb)
        - [Ejercicios resueltos](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.3c%20Ejercicios%20resueltos.ipynb)
    4. [Iteradores y Generadores](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.4a%20Iteradores%20y%20Generadores.ipynb)
        - [Ejercicios](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.4b%20Ejercicios.ipynb)
        - [Ejercicios resueltos](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.4c%20Ejercicios%20resueltos.ipynb)
    5. [NumPy](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.5a%20NumPy.ipynb)
    6. [Pandas](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.6%20Pandas.ipynb)
    7. [Matplotlib](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.7%20Matplotlib.ipynb)
    8. [Ejemplo de aplicación en IA](./T1:%20Tipos%20de%20datos%20avanzados%20en%20Python/T1.8%20Ejemplo%20de%20aplicación%20en%20IA.ipynb)

## Cómo usar los cuadernos

Existen varias opciones para trabajar con los cuadernos de la asignatura:

### Opción a): Google Colab
La opción más sencilla y rápida pasa por usar Google Colab. Necesitaréis una cuenta de Google y acceso a internet permanente (lo cual puede ser un inconveniente; ver opción c).

Para abrir los cuadernos de esta práctica:

1. Accede a [Google Colab](https://colab.research.google.com/).
1. Ve a *"Archivo" > "Abrir cuaderno" > "GitHub"*.
1. Escribe el usuario *jsilvestreUPV* y selecciona el repositorio *prg-gia-epsa*, o bien introduce directamente la URL de este repositorio.
1. Haz click sobre el cuaderno que quieras abrir en Colab.

Una vez abierto, podrás realizar modificaciones sobre el cuaderno, pero no podrás guardarlas. Si deseas guardar dichas modificaciones, deberás crear una copia local en tu cuenta de Google Drive. Para ello, ve a *"Archivo" > "Guardar una copia en Drive"*. Dicho notebook se almacenará en la carpeta *"Colab Notebooks"* de tu unidad de Google Drive.

### Opción b): Jupyter Notebook en Polilabs
Debéis acceder al escritorio LINUX de los PCs del laboratorio del DSIC, o bien al escritorio DSIC-LINUX de [Polilabs](https://polilabs.upv.es/) si os conectáis desde casa.

Una vez estéis dentro del escritorio de Ubuntu Mate:

1. Abrir una terminal:
    + *"Menú" > "Herramientas del Sistema" > "Terminal de Mate"*.
1. Situarse en el directorio W:
    + `cd $HOME/W`
1. Clonar el repositorio git de la asignatura:
    + `git clone https://github.com/jsilvestreUPV/prg-gia-epsa.git`
1. Ir al directorio del repositorio:
    + `cd prg-gia-epsa`
1. Ejecutar Jupyter:
    + `jupyter notebook`

### Opción c): Instalación local de Jupyter en vuestros PCs con kernel Python propio
La tercera opción es realizar una instalación local de Jupyter Notebook y de un kernel Python3 propio.

Instrucciones para GNU/Linux (Debian/Ubuntu):

1.  **Instalar Python3 y pip**: `sudo apt update && sudo apt install python3 python3-pip -y`
2.  **Instalar virtualenv**: `pip3 install virtualenv`
3.  **Crear un entorno virtual**: `python3 -m virtualenv prg-venv`
    - Activar: `source prg-venv/bin/activate`
    - Desactivar: `deactivate`
4.  **Instalar Jupyter y dependencias**:
    `pip3 install notebook ipykernel scikit-learn pandas numpy matplotlib`
5.  **Registrar kernel**:
    `python3 -m ipykernel install --user --name prg-venv`
6.  **Lanzar Jupyter**: `jupyter notebook` y seleccionar el kernel `prg-venv`.

### Opción d): Instalación local de Visual Studio Code / Antigravity
Si utilizas un entorno de desarrollo como Visual Studio Code (o Antigravity), puedes ejecutar los cuadernos directamente.

Recomendamos usar un entorno virtual para aislar las dependencias del proyecto. En Ubuntu Linux:

1.  **Abrir el repositorio** en VS Code.
2.  **Abrir una terminal** en VS Code (Terminal > New Terminal).
3.  **Crear el entorno virtual**:
    ```bash
    python3 -m venv .venv
    ```
    VS Code detectará el nuevo entorno y te preguntará si quieres usarlo para el workspace. Acepta.
4.  **Instalar dependencias**:
    Si existe un fichero `requirements.txt`, VS Code puede ofrecer instalarlo. Si no, o para instalar manualmente:
    ```bash
    source .venv/bin/activate
    pip install notebook ipykernel scikit-learn pandas seaborn openml numpy matplotlib
    ```
5.  **Seleccionar el kernel**:
    Abre cualquier cuaderno (`.ipynb`). Arriba a la derecha, haz clic en "Select Kernel" -> "Python Environments" -> selecciona el entorno `.venv` que acabas de crear.
