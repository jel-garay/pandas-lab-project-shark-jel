# pandas-lab-project-shark-jel

Primeramente chequeo las columnas y filas que tengo en el dataframe con el data.shape.

Una vez visto lo que tengo(columnas y filas) me dispongo a observar los valores nulos de cada columna.

Dichos valores nulos los limpio rellenandolos con un 'unknown' para columnas no numéricas y con 0 para las numéricas ejemplo'AGE'

Siguiendo con los valores nulos hago una hipotesis con la las filas que tengan más del 50% de valores nulos sean eliminados ya que considero que son filas que poco o nada pueden aportarme.

Una vez hecho esto dibujo un grafico para comprobar visualmente que valores nulos que me quedarían

Después observo los nombres de las columnas por si hubiera algún espacio y me diese cualquier problema, una vez identifico que hay dos columnas exactamente 'case number' y 'sex' que tienen dichos espacios los renombro como 'Case_Number' y 'Sex1'

Hecho esto la primera columna que empiezo a limpiar sería la de Year. Observo que de las 6000 y poco filas que me quedan las últimas tienen 0s y además hay valores que no son consistentes como por ejemplo datos de fechas que son completamnete ínutiles como fechas antes de cristo, siguiendo en la columna year uso la formula pd numeric para pasar todos los elemntos a numericos y una vez hecho eso al tener la columna fechas en float 2018.0 hago la formula correspondiente para que pasen a integer.

En la columna country lo que hago es ver los valores únicos y comprobar que estén correctamente escritos. He hecho alguna modificación menor como cambios de nombres para que quedara todo uniforme.

En la columna de Name lo que he intentado que los nombres estuvieran linkados con su apellido mediante '-'.

Entre medias para aprender y probar he hecho una pivot table de country y tipo de ataque ya que opino que las actividades acuaticas son distintas en cada país. Me explico: por ejemplo  Hawai es la meca del surf pero puede que en otro país se practique más la pesca en barco.

Para la columna age lo que he realizado primeramente es quitar los numeros que pudieran tener alguna letra adherida y por tanto  los hacía strings y no integers.Después lo cambio todo a numerico por si hubiera floats y finalmente los paso a integer. 

Seguidamnete de esto en AGE intento obtener la media basicamnete para saber la edad más frecuente en la que se producen dichos ataques. Era obvio que que los ataques más frecuentes ocurran a la población más joven ya que es la que hace actividades acuaticas más frecuentemente.

En Fatal lo que he intenatdo es hacer un bucle con un lambda para que me dejara solo los ataques que NO  mortales es decir los más habituales. De esa manera tenemos una muestra más completa ya que rara vez los ataques son mortales.

Y finalmente en la columna de species lo he hecho ha sido intentar que las especias tuvieran el indicativo de 'm' y una vez hecho eso coger las especies que miden entre 2 y 7 metros ya que son las más habituales para tener una muestar más exacta.

El objetivo era correlacionar las especies de tiburones con los tipos de ataque que hacian pero no me ha salido. Sorry




