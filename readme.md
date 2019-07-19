# 1. **AppEncuesta\_teamName:**

 ![Image1 de la aplicación](imagen1.jpg)

Cada equipo desarrollará una App con un escenario principal que incluya en un área central una imagen que sugiera encuestas. En el área superior, top, se incluya una barra de menú con un menú en la parte izquierda con diferentes menúitems uno por cada uno de los tipos de encuesta que se indicará  después. Otro menú en la parte derecha del top con los menuitem de ayuda y acerca de. Se supone un interfaz similar a:









Para el comportamiento del menú, se registrarán los manejadores de eventos correspondientes: Al hacer clic sobre el MenuItem Deporte se debe mostrar la escena para realizar la encuesta de Deporte, al hacer clic sobre el MenuItem Comidas se debe mostrar la escena para realizar la encuesta Comidas y así sucesivamente con cada encuesta. Al hacer clic sobre el MenuItem salir se cierra la aplicación.

Además se crearán por tanto varias UI (escenas gráficas) incorporando los controles necesarios para que un usuario pueda rellenar los distintos tipos de encuesta, al final quedará una interfaz similar a la de la imagen de uno de los tipos de encuesta (Deportes).  Las interfaces que se abrirán al seleccionar los menús serán cada unas pequeñas encuestas en la que se preguntará al usuario algunos datos personales, como la profesión, edad, o número de hermanos, y otros datos relacionados con los siguientes temas (un tema para cada escena):

1. **Deportes** , hábitos de ocio (ejemplo en la imagen adjunta)

2. **Comidas** , tipos de comidas, hábitos alimenticios.

3. **Animales** , mascotas, hábitos con las mascotas.

4. **Viajes** , medios de transporte, hábitos de viajar.

5. **Lectura** , tipo de lecturas, comics, novelas, ensayos, hábitos de lectura.

 ![Imagen2 de la aplicación](imagen2.jpg)











En este ejemplo necesitarás los siguientes componentes: etiquetas ( **Labels** ), un campo de texto para la profesión (TextField), para el número de hermanos incluirás una **ChoiceBox** que contendrán los valores: &quot;Ninguno&quot;, &quot;Uno&quot;, &quot;Dos&quot;, &quot;Más de dos&quot;, para la edad otra **ChoiceBox** en la que se deberá elegir entre: &quot;Menos de 15&quot;, &quot;Entre 15 y 18&quot;, &quot;Entre 19 y 35&quot;, &quot;Entre 36 y 60&quot;, &quot;Más de 60&quot;, un **RadioButtons** para el sexo, una **CheckBox** para preguntar al usuario si le gusta el deporte, una **ChoiceBox** para los deportes (Tenis, Fútbol, Balonmano, Atletismo y Natación), para las aficiones tres deslizadores, Sliders. Por último un Button para enviar la encuesta.

En cuanto al comportamiento de los **Sliders** deberá mostrar en la etiqueta de la derecha el valor correspondiente a la posición seleccionada entre 1 y 10 a medida que el usuario lo desliza. El manejador de selector de sexo, **Toggle** , que mostrará la imagen correspondiente al sexo seleccionado. El manejador de eventos del botón &quot;Enviar&quot; que validará que todos los campos estén rellenos, enviará el mensaje de error correspondiente si alguno de los campos no está relleno y por el contrario el mensaje &quot;Encuesta enviada con éxito&quot; cuando todo vaya bien. En este último caso **se grabará** la información de la encuesta en un **fichero** llamado **Enc\_Deporte.csv** , **Enc\_Comidas.csv** , etc., con la fecha y hora del sistema y todos los datos introducidos en una línea. Cada campo de la línea se separará por &quot;;&quot;.

Se deberá establecer una relación **modal** de aplicación en el que el Stage principal, el menú, abra el Stage de realizar encuesta (por ejemplo Deportes). Por lo que no se podrá realizar otra encuesta (por ejemplo Animales) ni cerrar la aplicación hasta realizada la primera encuesta a realizar o se cierre la ventana de la encuesta abierta inicialmente.

Para realizar este ejercicio, parte del código ejemplo proporcionado por Oracle o bien el que encuentres en Ensemble.jar y adáptalo a los requerimientos. Para la ubicación y alineamiento de los componentes usa los layouts (SplitPane, AnchorPane, BorderPane, HBox,…) que consideres oportuno.