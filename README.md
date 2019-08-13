| Carrera: | INGENIERIA DE SISTEMAS | | 
| --- | :--- | :---|
| Materia: | TECNOLOGIAS EMERGENTES II | 
| Apellidos y nombres: | APAZA ANTONIO EVERT | A 
| C.I: | 9168864 L.P. | 
| Lugar y fecha: | EL ALTO 13 DE AGOSTO

**1)Explique que son los sistemas empresariales**

Los sistemas empresariales son sistemas que tienen un impacto muy importante en el funcionamiento de una organización o negocio, que normalmente ofrece una alta calidad de servicio, gestiona con grandes volúmenes de datos, disponible de forma continua y es capaz de soportar cualquier organización grande.


**2) Describa cuales son las características más importantes de una aplicación empresarial**

Las características más importantes que presenta una aplicación empresarial son:
- El acceso a base de datos
- Operaciones transaccionales
- Son escalables, tanto vertical como horizontal
- Disponibles para la prestación de servicios de forma continúa
- Seguras
- Permiten la integración con otras tecnologías
- Arquitectura multicapa


**4) Explique cuáles son las diferencias entre la escalabilidad horizontal y escalabilidad vertical**

La escalabilidad vertical es hacer las actualizaciones o modernizaciones de componentes existentes, mientras que la escalabilidad horizontal se refiere a aumentar el número de componentes

**5) Que es un servidor Web y que es un servidor de aplicaciones**

Un servidor web es un programa informático que procesa una aplicación del lado del servidor, realizando conexiones bidireccionales o unidireccionales y síncronas o asíncronas con el cliente y generando o cediendo una respuesta en cualquier lenguaje o aplicación del lado del cliente.

Un Servidor de aplicaciones es un dispositivo de software que proporcionan servicios de aplicación a las computadoras cliente, generalmente gestionan la mayor parte de las funciones de la lógica de negocio y acceso a los datos de la aplicación. 

**6) Con un gráfico explique cómo funciona el protocolo HTTP**

![](https://user.oc-static.com/upload/2017/05/26/14957903870158_Captura%20de%20pantalla%202017-05-26%20a%20las%2011.14.02.png)
 
El protocolo HTTP funciona a través de solicitudes y respuestas entre un cliente y un servidor. A una secuencia de estas solicitudes se le conoce como sesión de HTTP.

**7) Explique los elementos importantes de REQUEST en HTTP**

Los elementos importantes de request en http son:
- El método http (la acción a realizar)
- La página para acceder (una URL)
- Parámetros de formulario (como argumentos de un método)

**8) Explique los elementos importantes de RESPONSE en HTTP**

Los elementos importantes de response en http son:
- Un código de estado (para saber si la solicitud fue exitosa)
- Tipo de contenido (texto, imagen, HTML, etc.)
- El contenido (el HTML real, la imagen, etc.)

**9) Describa con un gráfico la arquitectura Java EE**

![](https://image.slidesharecdn.com/jatunandjavaee-110905104600-phpapp02/95/desarrollo-de-aplicaciones-empresariales-con-java-ee-4-728.jpg?cb=1316098712)

**10) Explique cuáles son los contenedores, componentes y servicios de Java EE**



En Java EE presenta los siguientes tipos de contenedores: contenedores web y los contenedores de negocio(o de EJBs).    

Entre sus componentes están los de tipo cliente (Cliente AWT, Swing, Applet y navegador Web), web (Servlet, JSP y JSF)  y de negocio (EJB) las cuales cubren necesidades concretas y se basan en APIs específicas.    

Los servicios de Java EE son los de directorio, de despliegue, de transaccionalidad, de seguridad y de acceso a la base de datos. 

**11) Investigue los métodos más utilizados de las clases HttpServlet, HttpServletRequest y 
HttpServletResponse, y para cada uno de los métodos muestre un ejemplo**

**HttpServlet**    
**Métodos**

El método service() de la clase HttpServlet lanza diferentes peticiones a distintos métodos Java para sistemas de peticiones diferentes. Reconoce los métodos estándar en formato HTTP/1.1 y no es conveniente sobrecargarlo en subclases, a no ser que se necesiten para implementar métodos adicionales.    

Los métodos de petición que reconoce son: GET, HEAD, PUT, POST, DELETE, OPTIONS y TRACE (cualquier otro método obtendrá como respuesta un error HTTP). Para cada uno de los métodos anteriores, Java lanza un método de tipo doXXX(). Por ejemplo, para GET lanza doGet(). Todos los métodos esperan dos parámetros.    

Los métodos doOptions() y doTrace() disponen de una implementación por defecto y no está permitido sobrecargarlos.    

El método HEAD, que se supone que devuelve las mismas líneas de cabecera que podría devolver el método GET, sin incluir el cuerpo. Así que todos los métodos que se pueden utilizar van a ser doGet(), doPut(), doPost(), doDelete(), cuyas implementaciones por defecto en la clase HttpServlet devuelven un error HTTP. Cualquier subclase de HttpServlet debe sobrecargar uno o más de estos métodos para proporcionar la adecuada implementación de las acciones que desea realizar.

**HttpServletRequest**    
**Métodos**

- El método getParameter devuelve el valor de un parámetro nombrado. Si nuestro parámetro pudiera tener más de un valor, deberíamos utilizar getParameterValues en su lugar. El método getParameterValues devuelve un array de valores del parámetro nombrado. (El método getParameterNames proporciona los nombres de los parámetros.
- Para peticiones GET de HTTP, el método getQueryString devuelve en un String una línea de datos desde el cliente. Debemos analizar estos datos nosotros mismos para obtener los parámetros y los valores.
- Para peticones POST, PUT, y DELETE de HTTP.       
Si esperamos los datos en formato texto, el método getReader devuelve un               BufferedReader   utilizado para leer la línea de datos.    
Si esperamos datos binarios, el método getInputStream devuelve un ServletInputStream utilizado para leer la línea de datos.

**HttpServletResponse**    
**Métodos**

- El método getWriter devuelve un Writer
- El método getOutputStream devuelve un ServletOutputStream

Se utiliza el método getWriter para devolver datos en formato texto al usuario y el método getOutputStream para devolver datos binarios.    

Si cerramos el Writer o el ServletOutputStream después de haber enviado la respuesta, permitimos al servidor saber cuando la respuesta se ha completado.
