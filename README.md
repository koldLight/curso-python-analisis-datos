[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/koldLight/curso-python-analisis-datos/master)

# Libro Python para análisis de datos

Este curso tiene como objetivo enseñar Python orientado al análisis de datos en aproximadamente 24 horas.

No hace falta tener conocimientos previos de Python.

## Contenido del curso

* 1: Anaconda y notebooks
* 2: Pandas
* 3: Programación
* 4: APIs
* 5: Web scraping
* 6: Introducción a la visualización de datos
* 7: Gráficos
* 8: Gráficos con seaborn
* 9: Mapas
* 10: Numpy
* 11: Pivotación de tablas
* 12: Bases de datos
* 13: Producción
* 14: Entornos

_Nota:_ Hay gente que piensa que esta forma de ordenar el curso es _rara_. Los programadores estamos acostumbrados a empezar viendo sintaxis básica, tipos de datos, etc... para ir subiendo a librerías de más alto nivel más tarde.

Aquí, lo he hecho al revés. Lo primero que vemos son tablas de datos con pandas y de forma indirecta iremos utilizando números, cadenas de texto, listas, diccionarios, ... sin haberlos dado explícitamente. ¿Por qué? Para que el principiante pueda ver avance rápidamente y comprenda para qué sirve esa _parte aburrida_ de los tipos de datos y estructuras básicas antes de ponerse con ellas.

## Ejecutar los notebooks del curso

### Binder

La forma más fácil es utilizando Binder. Entra [aquí](https://mybinder.org/v2/gh/koldLight/curso-python-analisis-datos/master), espera a que se inicie, y tendrás los notebooks disponibles en un entorno funcional. De esta forma, puedes seguir el curso sin necesidad de que instales nada en tu ordenador.

En cambio, si quieres ir realizando los ejercicios y guardando los resultados, te recomiendo que instales Python localmente.

### Instalación local

Para lanzarlo desde tu máquina, tienes dos opciones:

* Instalar Anaconda para Python 3 (recomendado para usuarios principiantes)
* Utilizar `pipenv` (recomendado para usuarios avanzados).

#### Instalación local con Anaconda

Instala la última versión de Anaconda para Python 3.7 para tu sistema operativo desde [aquí](https://www.anaconda.com/download). Fíjate bien que instales la de Python 3.7 (y no la de Python 2.7).

Aquí tienes un tutorial paso a paso de cómo hacerlo:

* [Windows](https://www.datacamp.com/community/tutorials/installing-anaconda-windows). Fíjate bien en el paso en el que debes marcar que añada anaconda al PATH. Esa casilla debe quedar marcada.
* [Mac](https://www.datacamp.com/community/tutorials/installing-anaconda-mac-os-x).

Una vez instalado, nuestra terminal debería reconocer los comandos `conda` (el gestor de paquetes), `jupyter` (la herramienta de notebooks) y `python`, gracias a que hemos añadido anaconda a nuestro PATH. Esto quiere decir que, cuando escribamos uno de estos comandos, nuestro sistema lo buscará en la carpeta de anaconda. 

Para comprobarlo, abre una consola. Esto se puede hacer:

* En Windows, abriendo el menú inicio y escribiendo cmd.exe. Si necesitas ayuda, mira más opciones [aquí](https://www.lifewire.com/how-to-open-command-prompt-2618089).
* En Mac, abre una terminal. Si necesitas ayuda sobre cómo abrirla, mira [aquí](https://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line).
* En ubuntu / debian, abre una terminal. Si necesitas ayuda, mira [aquí](https://www.lifewire.com/ways-to-open-a-terminal-console-window-using-ubuntu-4075024).

Una vez abierto, nos debería funcionar bien los siguientes tres comandos:

```
python --version

conda --version

jupyter --version
```

Si nos dice que no reconoce el comando, es que no se ha añadido correctamente anaconda al PATH. Los tutoriales referenciados tienen buenas soluciones a este problema habitual.

Ahora, vamos a instalar las dependencias necesarias para nuestras sesiones con `conda`. Para ello, abre una terminal en tu ordenador y lanza lo siguiente:

```
conda install -c conda-forge seaborn
conda install -c conda-forge folium
```

Los comandos anteriores deberán instalar sin error las librerías.

Y finalmente, para abrir los notebooks en Windows, puedes hacer, desde la consola (cmd.exe):

```
jupyter notebook --notebook-dir='C:\mi\ruta\con\notebooks\'
```

En mac o linux, con la terminal:

```
jupyter notebook --notebook-dir='/mi/ruta/con/notebooks'
```

Modificando la ruta dependiendo de dónde los hayas descargado.

#### Instalación local con pipenv

Necesitarás:

  * Python 3.7 o superior
  * pipenv
  * jupyter

Si no tienes `pipenv`, puedes instalarlo como comando así:

```
sudo -H pip install -U pipenv
```

Si no tienes `jupyter`, puedes instalarlo como comando así:

```
sudo -H pip install -U jupyter
```

Para instalar las dependencias, ejecuta:

```
pipenv install --dev
```

La primera vez que lo lances, creará el entorno virtual con las dependencias del proyecto.

Y para crear el kernel sobre el que correrán los notebooks, lanza lo siguiente:

```
# Activate the virtual environment
pipenv shell

# Create the kernel
python -m ipykernel install --user --name='libropython'

# Exit the virtual environment shell
exit
```

A partir de ahora, en `jupyter`, tendrás un nuevo kernel disponible llamado `libropython`. Tendrás que seleccionarlo para ejecutar correctamente los notebooks de este curso.

Finalmente, para lanzar los notebooks:

```
pipenv run jupyter notebook .
```

## Contribuye

Si ves algo incorrecto, que no se entiende bien, crees que falta alguna explicación o tienes alguna idea que compartir, puedes crear una `issue` en el repositorio.

## Licencia

[![Binder](http://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

## TODO

* Revisar links rotos
* Añadir ejemplo paleta cut en sns
* Ejercicio OVNIs quitar hist o sugerir agregar por año
* Cambiar orden de ejercicio APIs después de mapas
