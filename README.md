# Proyecto 4. Modulación 16-QAM. 

Nombre: Miguel Andrés Salazar Alvarado. 

Carné: B97118.

En el siguiente proyecto se hizo uso de la modulación de tipo 16-QAM, la misma se conoce como QAM cuatizada ya que se basa en los principios de su similar analógica, debido a que 
posee una entrada con datos binarios (0, 1), los mismos son obtenidos mediante una función divididos en grupos de tantos bits como se requieran para generar N estados de modulación.
En este caso se hizo uso de N = 16 usando la expresión k = 4. El problema, lo que supone es por medio de la señal transmitida de manera binaria, al pasarlo a una sección de modulación
bajo las descripciones teóricas de 16-QAM, se logre transmitir la imagen y verificar su comportamiento al graficar los resultados. Además, busca verificar que la señal transmitida resulte ser un proceso
estacionario y ergódico conciendo las relaciones entre los valores del promedio temporales y de los datos. Finalmente, obtener gráficamente la densidad espectral de potencia, por 
medio de la formulación descrita. 

![alt text](https://github.com/MiguelS1501/Proyecto4/blob/main/arenal.png)

Separando la funcionalidad de las secciones modificadas se tiene que: 

1- ) En la parte de modulación la señal le ingresa un vector unitario que luego se le cambia la forma por medio de la función de Numpy "reshape", dejandolo como matriz de Nx4. 
La misma igual que en la BPSK, presenta una función portadora s(t), la cual está compuesta por los componentes seno y coseno quienes son ortogonales. Los mismos se suman en una
sola variable. Estos presentan diversos valores para las amplitudes ([-3,-1,1,3]) dependiendo como indica el enunciado de los bits de la matriz los cuales están separados en b1, 
b2, b3 y b4. De esta manera y por medio de un for iterativo es posible encontrar los valores de ambos componentes. 

2- ) Ahora bien, en la parte de demodulación, se toma los valores de la parte anterior recostruyendo el seno y el coseno de la señal demodulada. Además se establece un criterio de
decisión por detección de energía en ambas portadoras, los cuales se encontraron através de variaciones con distintos números. En este caso se demodula la función para posteriormente
obtener la traducción de la misma por medio de una imagen. Los resultados indicaron que se hizo el proceso de manera correcta, debido a que tenía 0 errores y además se recuperaba 
la misma imagen. En las graficas se observaba la señal moduladora y el comportamiento acorde a la transmitida. 

Cabe destacar que las demás funciones se dejaron como estaban inicialmente y lo que se modificó, fueron estas dos para la primera parte. Lo anterior, debido a que cumplian con la 
misma funcionalidad. Depués, en la parte de ergodicidad y de estacionaridad, se hizo la comprobación mediante un porcentaje de error que el promedio de los datos corresponde 
al promedio en el tiempo, lo cual es el criterio de la ergodicidad. Como esta primera, es más restrictiva en su significado que la estacionaridad, una implica la otra. Sin embargo, 
se realizó la comprobación de que una de sus propiedades estadísticas (media) es igual a un valor constante para un intervalo de tiempo. Finalmente, mediante la densidad espectral de
potencia se visualizó un máximo de más de 140000 en su magnitud y se observa un comportamiento adecuado a los resultados obtenidos en las secciones anteriores. 

# Resultados obtenidos:

La siguiente muestra la imagen transmitida y recibida después del proceso de modulación:

![alt text](https://github.com/MiguelS1501/Proyecto4/blob/main/Recibida-Transmitida.JPG)

Además, se señalan las gráficas de las diferentes señales de especial relevancia que forman parte de las distintas secciones de transformación.

![alt text](https://github.com/MiguelS1501/Proyecto4/blob/main/grafica.png)

Seguidamente, se muestra un ejemplo de diferentes patrones de funciones en el tiempo. 

![alt text](https://github.com/MiguelS1501/Proyecto4/blob/main/ergodicidad.png)

Por último, es posible visualizar la gráfica que indica la magnitud espectral de potencia.

![alt text](https://github.com/MiguelS1501/Proyecto4/blob/main/potencia.png)


