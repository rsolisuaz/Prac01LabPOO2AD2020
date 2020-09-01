#PRACTICA 1. FORMATEO DE FECHAS Y REVISIÓN DE COMO SUBIR LAS PRÁCTICAS Y PROGRAMAS DE POO2.

## COPIA DEL REPOSITORIO REMOTO EN SU COMPUTADORA LOCAL
Como primer paso, será necesario crear una copia local del repositorio remoto creado en Github al aceptar la tarea. Para ello, es necesario hacer los siguientes pasos:
1)	Entrar a la página cuyo URL les fue proporcionado al aceptar la tarea, en tal página dé click en el botón Code y copie el URL que aparece en el cuadro de texto de nombre **Clone with HTTPS** (comienza con https://)
2)	En una consola de Git Bash en Windows (o en una terminal en Linux o Mac), cree una carpeta donde quiera que se contengan sus prácticas del semestre (si es que aun no la creado) y colóquese en tal carpeta. La carpeta la puede crear desde el Git Bash o terminal Linux/Macusando el comando mkdir (o con el explorador de archivos de su sistema operativo) y en la consola de Git Bash o terminal de Linux/Mac se puede cambiar a la carpeta mencionada usando el comando cd
3)	Clone el repositorio privado dando el comando **git clone URL practica01**
 (donde **URL** es el URL que copió en el paso 1)
 Este comando creará dentro de la carpeta creada en el paso 2) una subcarpeta de nombre practica01 donde estará una copia local del repositorio remoto


## MODIFICACIÓN DEL CÓDIGO PROPORCIONADO
Una vez que tenga el repositorio local, su trabajo consiste en completar el método **formateaFechaEn** de la clase **AnalizadorFechas**, proporcionada en el repositorio privado que se creó al aceptar esta tarea.

Tal método tendrá como trabajo recibir un String que representa una línea de texto leída del teclado y que pudiera contener una fecha en formato corto. Si de hecho la línea contiene una fecha válida (de acuerdo a la región que se especifica inicialmente en la entrada) el método deberá regresar un String con la fecha correspondiente en formato largo para la región especificada inicialmente, de otra manera deberá generar una excepción *ParseException*.

En el código que se les proporciona como base, ya se encuentra implementada toda la lógica para leer las líneas de la entrada e imprimir el resultado que devuelve el método *formateaFechaEn*.

La entrada se asume tendrá siempre la siguiente estructura, y por tanto no es necesario validarla:
a)	La primera línea contiene dos cadenas separadas por espacio, la primera representa un código de idioma y la segunda representa un código de país. Estos datos son los que se usan para crear un objeto Locale que representa a la región indicada por esos dos datos, así como dos objetos DateFormat, uno para procesar fechas en formato corto y otro para procesar fechas en formato largo
b)	De la segunda línea en adelante, pudiera haber líneas vacías, líneas que contienen SOLO una fecha valida y líneas que contienen texto que no representan una fecha valida

En el método *procesaEntrada* se hace todo el trabajo de leer las líneas de entrada, crear los objetos necesarios y llamar a formateaFechaEn por cada línea no vacía tomando en cuenta que el método *formateaFechaEn* pudiera genera una *ParseException*.


##NOTAS IMPORTANTES
1)	Es necesario estar guardando los cambios realizados usando **git add** y **git commit**
2)	Una vez que esté seguro de que funciona correctamente suba su copia local al repositorio remoto usando el comando **git push**
3)	Cada vez que haga git push se realizaran automáticamente pruebas sobre su código para verificar si funciona correctamente. Verifique que en la página de su repositorio en la sección **Pull Requests**, se encuentra una subsección de nombre **Feedback**, ahí podrá encontrar los resultados de las pruebas en la sescción **Check** y cualquier comentario general que el profesor tenga sobre su código en la pestaña **Conversation**. También es posible que haya comentarios sobre líneas de código específicas en la pestaña **Files Changed**. **NO BORRE ESTA SUBSECCIÓN DE FEEDBACK NI CIERRE EL PULL REQUEST**. Si tiene preguntas sobre los comentarios que le haya dejado el profesor, escríbalas en la pestaña **Conversation** usando el área de texto que se encuentra hasta abajo asegurándose de dar click en **Comment** una vez tecleada la pregunta.
