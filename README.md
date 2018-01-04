# Discursos presidenciales

Datos originales de discursos presidenciales obtenidos desde la Web, y scripts para procesarlos (extraer texto, limpiarlo y eliminar duplicados). Actualmente contiene:

- 575 discursos de Sebastián Piñera desde 2010 hasta 2014, obtenidos desde el sitio http://2010-2014.gob.cl/discursos/ (descargados en diciembre 2017). Todos los discursos se encuentran en páginas en formato .htm. Aproximadamente 565 son discursos únicos.
- 1581 discursos de Michelle Bachelet desde 2014 hasta 2017, obtenidos desde el sitio https://prensa.presidencia.cl/discursos.aspx (descargados en diciembre 2017). Todos los discursos se encuentran en páginas en formato .html. Aproximadamente 1544 son discursos únicos.

Para procesarlos simplemente se debe ejecutar el script `data_processing.sh` en la raiz (requiere python 3, un par de librerías estandar y [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/)). Este script genera archivos de texto con el contenido de cada discurso eliminando algunos duplicados o discursos que son realmente extractos de otros. 

Importante: la extracción de texto desde los archivos más el chequeo de duplicados puede tardar un par de minutos pues el chequeo implica encontrar el traslape máximo entre pares de discursos y eliminar el discurso de menor tamaño cuando el string comun más largo pase cierto umbral (ver los códigos para los umbrales seteados en cada caso así como la cantidad pares a chequear y la forma de los chequeos).