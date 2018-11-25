##EXPLICACIÓN DEL DIAGRAMA DE CLASES

En el diagrama de clases entregado mostramos las relaciones que se establecen entre las clases de nuestro problema, junto a sus atributos y métodos. A continuación voy a explicar dichas relaciones y añadir reseñas importantes para entenderlas.

Para comenzar establecemos una clase **Alumno**, en la cual cabe destacar la inclusión de los atributos *es_líder* y *ID_grupo*, ya que nos ahorra la existencia de una clase **Grupo** que no es necesaria puesto que podemos acceder a esa información directamente en la clase **Alumnos** de manera sencilla y de forma que satisface nuestro sistema.

Por otro lado, la clase **Alumno** está relacionada con **Base de datos** con una relación de composición, donde la clase **Alumno** representa el compuesto y la clase **Base de datos** el componente, ya que si no existen alumnos o no los introducimos al sistema no existiría base de datos que los recogiese. La cardinalidad de la clase **Alumnos** en esta relación sería "1..*" porque una base de datos puede estar formada por 1 o muchos alumnos, y la cardinalidad de **Base de datos** sería "0..1" ya que un alumno puede no estar en la base de datos pero si lo está, es de forma única.

Además existe una relación de asociación entre la clase **Base de datos** y la clase **Profesor** puesto que el profesor inserta, modifica, borra o extrae información de esta. En este caso la cardinalidad de la clase **Base de datos** en la relación es "0..1" puesto que e profesor puede acceder o no a la clase de datos, y la clase **Base de datos** tiene cardinalidad "0..*" ya a la base de datos pueden acceder cero o muchos profesores.

Por último existe una relación de generalización entre la clase **Profesor** y las especializaciones **Coordinador** y **Ayudante**, puesto que ambos pueden usar los métodos establecidos en la clase **Profesor**, pero individualmente son diferentes.