## <a name="_t4d9uhe70tf8"></a>**Terminal y línea de comandos**

🧸 Manejo de la línea de Comandos de Linux, apuntes y resumen. Es una herramienta esencial para todo desarrollador de Software.


## <a name="_28tlo46n6ef1"></a>**Instalación de Ubuntu en win10 virtual**
Dentro de Windows PowerShell escribe la siguiente instrucción y presiona la tecla Enter:
wsl --list --online

wsl --install -d ubuntu

wsl --install -d

Definición comando:

Un comando es una acción escrita, generalmente, a través de una terminal y emulada por una shell para ser ejecutada por nuestro sistema operativo.


Comandos de la clase

- **pwd** o print working directory. Comando para encontrar el ruta actual de trabajo de manera absoluta o desde el directorio /
- **cd** o change directory. Comando para navegar entre directorios requiriendo, dependiendo, del directorio o ruta a navegar.
  Hay varios shortcuts para navegar rápidamente:
  - cd .. para mover a un directorio inmediato anterior
  - cd para ir al directorio home
  - cd - para mover a un directorio previo
- **ls**. Comando para ver el contenido de un directorio. Por defecto, se mostrará el contenido del directorio actual.
  Algunas opciones son:
  - ls -R listar archivos de sub-directorios
  - ls -al listar archivos ocultos y de manera detallada
- **file** . Comando para reconocer el tipo descriptivo del archivo
  - file file.txt
  - resp. es un tipo de archivo de texto
## <a name="_9up1m9t0t1td"></a>**Aprendiendo a caminar en la terminal.**
- El sistema de archivos 📁 inicia en un slash **/** y desciende a otras carpetas. De todas las carpetas, nos interesa **home** ya que dentro se encuentran las carpetas de cada usuario, donde están todos los documentos.
- Cuando entramos, la terminal nos coloca en **~**, que es donde están nuestros documentos **/home/usuario.**
- **cd** Para acceder una carpeta, usa **cd** **<carpeta>**, para regresar a la carpeta anterior cd ... Para regresar a home, solo haz cd.
- **clear** Para limpiar la pantalla, o bien, el comando **ctrl+l**.
- En cada comando, hay varias especificaciones que podemos poner, después de **-**.
- **ls** para listar archivos. Agrega **-l** o **-lh** para agregar detalles.
- **pwd** print working directory 🖨️.
- **file <archivo>** sirve para describir un tipo de archivo y sus características 🥴.
##
## <a name="_d447tqwfpyv4"></a><a name="_nj8c7bspu0sa"></a>**Manipular archivos**
- **mkdir <nombre\_directorio>**: crea un directorio también puedes añadir la ruta
- **touch**: crea un archivo, si no indicas la extension por defecto sera **.txt**
- **cp <archivo> <ruta>**: nos permite duplicar archivos, para duplicar directorios con su contenido añadir el modificador **-r** que indica recursividad
- **mv <archivo> <ruta>** : mover un archivo hacia un directorio. También se usa para renombrar archivos **mv <archivo> <nuevo nombre>** no olvidar la extensión del archivo
  Para mover directorios añadir el modificador **-r**
- **rm**: elimina archivos, con **-i** indica un mensaje de confirmación en consola para tener mas control sobre la elección de que archivos queremos eliminar. Para eliminar un directorio añadir **-r** y **-ri** para usar el mensaje de confirmación

## <a name="_uyehxt3zxzca"></a>¨**q¨ para salir del editor de texto en ubuntu**

## <a name="_6m5c44wm4la"></a>**Head, tail, less, Explorando el contenido de nuestro archivos.**
- Podemos explorar el contenido de archivos sin la necesidad de abrirlos, desde la terminal 🧐. Esto para archivos de texto.
- **head <documento de texto>**: Nos muestra las primeras 10 líneas de un archivo de texto. Para especificar el número de líneas: 

**head -n** **<numero de lineas> <archivo>**

- **tail <documento>**: Nos muestra las últimas 10 líneas.
- **less <archivo>**: Este es muy cool, es muy interactivo, nos permite hacer scroll, y nos permite hacer búsquedas haciendo **/<palabra a buscar>**. Para salir presionamos q 🔍.
- **xdg-open** <**archivo>**: Para abrir un archivo desde la terminal. Usa las aplicaciones predeterminadas. Esto para linux, para mac, es **open**. Esto crea un proceso en la terminal que no nos dejará hacer nada mas. Para terminar el proceso **ctrl+c**.
- **nautilus** nos permite abrir el explorador de archivos en una posición dada (en linux) 📁.

## <a name="_6cuznbmlckh2"></a>**Help, man, info, alias - comandos**
- Un comando puede ser 4 cosas 4️⃣:
  - Un programa ejecutable.
  - Un comando de utilidad de la shell. Esto es un programa en si mismo, que puede tener funciones. Ejemplo cd
  - Una función de shell. Son funciones de shell externas al comando de utilidad. Ejemplo **mkdir**
  - Un alias. Un ejemplo es **ls**
- **type <comando>**: Nos permite conocer que tipo de comando es 🤔.
- **alias l="<secuencia de comandos>"**: Nos permite crear comandos. Son temporales, se borran al cerrar la terminal 👶🏼.
- **help <comando>**: Nos permite consultar un poco de documentación de un comando 📄.
- **man <comando>**: De *manual*, nos permite conocer mucha mas información de un comando.
- **info <comando>**: Similar al anterior, pero un poco resumido y con otro formato.
- **whatis <comando>**: Describe un comando en una sola línea ☺ ️. No funciona con todos.
## <a name="_xodc0dtu5f1k"></a>**Wildcards**
Son una serie de caracteres especiales que nos permiten realizar búsquedas muy avanzadas utilizando **ls** 🔍. Puedes utilizar wildcards con otros comandos que realizan manipulación de archivos como **mv**, **cp** o **rm** 💫. También se conocen como *comodines.*

- **ls \*<texto>**: Nos muestra todos los archivos que tengan en su nombre dicho texto al final. Si haces ls **<texto>\*** lo busca al final. El asterisco significa *cualquier string.*
- **ls <text>?** El signo de interrogación sustituye a cualquier carácter, por ejemplo, buscamos todos los archivos que tengan una palabra y un número dado de caracteres después. El signo de interrogación significa *cualquier carácter*.
- **ls [[:upper:]]\*** Para filtrar cosas que inicien que una mayúscula; esto busca también dentro de los directorios.
- **ls [[:lower:]]\*** Lo mismo pero con minúsculas.
- **ls -d** Se muestran solo directorios.
- **ls [ad]\*** Todo lo que inicie con **a** o con **b**

## <a name="_jw9235s3yrkx"></a>**Redirecciones: Cómo funciona la shell.**
- Normalmente, cuando pones un comando en la terminal, la salida se muestra ahí mismo, pero se puede redirigir la salida a un archivo 👀. Si la salida es correcta tiene __*file descriptor 1,* si no, *file descriptor 2*__*.*
- La entrada estándar es nuestro teclado que tiene ***file descriptor** 0*, pero también puede venir de otro lado 🧠.
- Para redirigir algo usamos **>**. Por ejemplo **ls > misarchivos.txt**, entonces la salida del comando se guarda en ese archivo de texto. Siempre crea este archivo (si ya existe, lo reescribe).✍🏽
- Para que se concatene la salida en un archivo preexistente usa **"comando" >> "archivo"**. Esto ambos solo redirigen los **stdout**.
- Para redirigir **stderr**, agregas su *file descriptor **"comando" 2> "archivo"**.* 👽
- Si quiere redirigir cualquiera de las dos opciones **"comando" >> "archivo" 2>&1**.
- Esto nos puede servir para, por ejemplo, guardar los mensajes de error que manda un servidor 🤯.
- Para redirigir **stdin** se usa **<** Esto te permite tener de entrada de comandos algún archivo.

## <a name="_wstvl5aa19tw"></a>**Redirecciones: pipe operator.**
Es uno de los operadores mas útiles que existen, ya que nos permite poner varios comandos, tales que la salida de uno es la entrada del siguiente 📤.

- **echo <texto>** genera un stdout con el texto que tenemos.
- **cat <archivo1> <archivo2>** muestra los dos archivos concatenados 💩.
- El pipe operator **|** hace que el ***stdout*** de un comando sea el ***stdin*** de otro comando. Por ejemplo **ls -lh | less**
- **tee** hace algo parecido a **>**, pero dentro de los pipe´s, por ejemplo: 

**ls -lh | tee** **output.txt |less** 

Se puede poner en medio, pero se ignora porque se sigue pasando.

- **cowsay "Texto"** es un comando que imprime una vaca que dice algo JAJAJAJAJ 🐮.

**\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_**

**< Nunca pares de aprender >**

` `**-------------------------**

`        `**\   ^\_\_^**

`         `**\  (oo)\\_\_\_\_\_\_\_**

`            `**(\_\_)\       )\/\**

`                `**||----w |**

`                `**||     ||**

- **echo "Texto" | lolcat** esto lo imprime con colores bonitos 😂.

## <a name="_yobrkirba9y4"></a>**Encadenando comandos: operadores de control.**
Son símbolos reservados por la terminal que nos permiten ejecutar varios comandos seguidos, e incluso agregar condicionales ⛓️.

- Síncronos: Se corre uno detrás de otro, en orden. Se hace esto con ; , por ejemplo 

**ls; mkdir carpeta1; cal** 👁️

- Asíncrono: Por cada comando, se abre una nueva terminal, y cada comando se corre de manera paralela, esto es con **&**, por ejemplo 

**ls & date & cal** ⏲️

- Condicionales: Podemos agregar lógica a como se corren los comandos:
  - **AND**: Si se cumple un comando, entonces se ejecuta el siguiente, se usa &&, un ejemplo es 

**mkdir carpeta1 && cd carpeta1 && echo "Si se pudo"** 

Si no se puede ejecutar el primer comando, no se ejecuta el siguiente. 🚆

- **OR**: Se ejecuta el primer comando que se pueda ejecutar, y se usa ||, por ejemplo 

**cd carpeta || echo "No hay carpeta"** 🤩
## <a name="_ocuvcg3h9ver"></a>**Permisos**.
- Cuando listamos con **ls -l** se muestran varias cosas. Los tipos de archivos:
  - - archivo normal.
  - d directorio.
  - l link simbólico.
  - b archivo de bloque especial.
- Tipos de modos: rwx corresponde con *read, write y execute.* Se representan con 3 bits, y los podemos manejar a través de un modo octal, esto es, pasar de binario a número.
  - rwx (1,1,1) dueño. En modo octal es 7.
  - r-x (1,1,1) grupo. En modo octal es 5.
  - r-x (1,0,1) world. Octal 5.
- Modo simbólico: Esto es para asignar los permisos a los diferentes posibles usuarios.
  - u Solo para el usuario.
  - g Solo para el grupo.
  - o Solo para otros (world).
  - a Aplica para todos.

`	`Permisos 750 solo admin.
## <a name="_b29d8vp5zi89"></a>**Ubuntu como root:**
**Sudo su** (Enter)

**Password** (Enter)

\---

Volver al usuario anterior

**su alexjair** (enter)
## <a name="_76pd597ptr00"></a>**Modificando permisos en la terminal.**
- Existen diversos usuarios con permisos cada uno; el usuario **root** es especial y puede hacer de todo🚶🏽.
- Puedes crear archivos de texto también con **> archivo.txt** y también podemos editarlo con **cat > archivo.txt** 📜
- En un archivo, se muestran: 

**[tipo de archivo][rwx usuario][rwx grupo][rwx mundo]**

, por ejemplo, 

**-rw-r--r-- mitexto.txt** 👀.

- **chmod <permiso en octal para usuario><para grupo><para mundo> <archivo> change mode** 

nos sirve para cambiar los permisos de un archivo. Si hacemos por ejemplo **chmod 755 mitexto.txt** tendremos ahora **-rwxr-xr-x mitexto.txt**, esto no cambia para nada el contenido del archivo.

- Para quitarle los permisos a alguien en particular, usamos el modo simbólico y usando la resta, por ejemplo quitando el permiso de lectura al usuario chmod **u-r mitexto.txt**. Para agregar, se usa la suma. 🧮
- Podemos hacer configuraciones mas avanzadas, por ejemplo, podemos asignar varios permisos al mismo tiempo **chmod u-x,go=w mitexto.txt**.
- **whoami** Para saber que usuario somos, y también podemos obtener el ID del usuario con **id**.
- **su root** para cambiar de usuario hacía **root**, hay que tener cuidado al usar este usuario 😟. Su home es incluso distinto. Los archivos que crea **root** (o otro usuario) no se pueden eliminar por un usuario normal.
- **sudo <comando>** nos otorga temporalmente los permisos de root para ejecutar algún comando que ocupe permisos especiales. 🦸🏽 Nunca dejes el usuario root por defecto, y ponle una contraseña distinta!!
## <a name="_wj5qn3afbks3"></a>Editar Texto linux (nano)
1. **nano** *texto.txt* (enter)
1. *..--editar el archivo--*
1. **Ctrl+X** (enter)
1. **Y** (enter)
1. (enter)
<a name="_e8zvv4a8d8id"></a>**Banderas del comando (find)**
Banderas básicas:
-----------------------------------------------------------
- -**name**: Realiza una búsqueda por nombre de archivo.
- -**iname**: Realiza una búsqueda por nombre de archivo sin tomar en cuenta las mayúsculas o minúsculas.
- -**type**: Realiza una búsqueda por tipo de archivo, f(files) y d(directories) que son los más comunes.
- -**size**: Realiza una búsqueda por el tamaño de archivo y/o directorio.

Banderas de tiempo⏰

- **mmin**: Búsqueda por tiempo en minutos.
- **mtime**: Búsqueda por tiempo en días.

Más banderas👀

- -**maxdepth**: Después de está bandera se pone el número de niveles de profundidad en los que queremos realizar la búsqueda
- -**empty**: Realiza una búsqueda de archivos y/o directorios vacíos.
- -**perm**: Búsqueda de archivos por permisos.
- -**not**: Retorna los resultados que no coinciden con la búsqueda.
- -**delete**: Está bandera se coloca al final del comando, eliminara los resultados de la búsqueda(⚠ ️Hay que tener mucho cuidado al usarla).

Hay muchas más banderas, pero esas son las que me parecieron más útiles.
.
**Ejemplos**:
A continuación pondré unos cuantos ejemplos de las banderas mencionadas anteriormente.

Búsqueda de todos los archivos con el permiso 644 a partir del directorio actual con una profundidad de 2 niveles.

**find . -perm 644 -maxdepth 2**


Búsqueda de archivos vacíos a partir del directorio actual.

**find** . -type **f** -empty


Búsqueda de todos los archivos .log, todos los resultados serán eliminados.

**find** . -type d -iname "\*.log" -**delete**   
## <a name="_4zwcvgpi4mtt"></a>Su majestad: grep
Veamos los comandos de clase, recordar que **grep** usa expresiones regulares (**regex**):

1. **grep -i the movies.csv** : Lo que busca este comando es cualquier línea que contenga la palabra “the”, asi sea mayúscula o minúscula.
1. **grep -ci the movies.csv** : Lo que hace este comando es encontrar el numero de veces que aparece la palabra “the” dentro del archivo, así sea mayúscula o minúscula.
1. **grep -vi towers movies.csv > sintowers.txt** : Lo que hace este comando es buscar todas las lineas que no tienen la palabra towers, y el output ponerlo en un archivo de texto llamado “**sintowers**”.
1. **wc**: Cuenta la cantidad de palabras de un archivo.
1. **wc -l**: Cuenta la cantidad de lineas de un archivo.

**grep** es un comando con muchas utilidades, la verdad es que tiene muchos casos de uso, aquí te dejo algunos que a mí me han sido de utilidad 👀👇:

1. Buscar algún paquete en específico que tengas instalado:

dpkg --get-selections | grep nombreDelPaquete

\# dpkg --get-selections te dirá todos tus paquetes instalados

\# grep filtrará esa lista con el paquete que te interesa

1. Filtrar algún archivo en específico después de un ls:

ls -al | grep myFile.txt

\# ls te dará la lista de todos tus archivos

\# grep filtrará todos y te mostrará únicamente el que deseas

1. Buscar algún contenido en específico dentro de algún archivo:

cat unArchivoLargo.txt | grep "La línea que busco"

\# cat Te listará todo el contenido de ese archivo

\# grep te filtrará únicamente lo que quieres ver


1. Buscar una línea en específico en diferentes archivos por medio de un patrón:

grep "string" archivo\_\*

\# grep buscará la palabra "string" en todos los archivos que comienzen por "archivo\_" y te los mostrará.

1. Buscar usando expresiones regulares (te recomiendo aprender expresiones regulares, son MUY poderosas 👀):

Imagina que tienes un archivo llamado test.txt y adentro contiene la siguiente frase:

*Imagina que quieres buscar algo*

Entonces, podemos usar grep así:

grep "Imagina .\* algo" test.txt

\# grep buscará alguna coincidencia, la expresion .\* indica que ahí dentro puede haber una o más letras, cualquier que sea, así que podrías leerla como: Imagina (cualquier cosa) algo.

Esto encontrará justo la frase que quieres:

Imagina que quieres buscar algo

## <a name="_qezzaxiawuhd"></a>Utilidades de red.
Existen comandos que nos dan información sobre la red 🥅:

- **ifconfig**: Nos da información general sobre nuestra red 🔍.
- **ping <url>**: Nos dice si una página está activa a no 🏃🏽. Lo revisa continuamente, y podemos usarla para ver la velocidad de nuestra conexión.
- **curl <url>**: Nos trae un archivo de texto a través de la red 🌎. (El index.html).
- **wget <url>**: *Web get,* trae un archivo de la web, descarga el archivo directamente a nuestra computadora 💻. (El index.html con mejor formato).
- **traceroute <url>**: Nos da la lista de todas las computadoras (direcciones IP) por la que nuestra conexión pasa para llegar a un sitio web 🚰.
- **netstat -i**: Nos muestra los dispositivos de red. Similar a **ifconfig** pero más resumido 👀.

## <a name="_r5m5twx6alu3"></a>Comprimiendo archivos.
- Podemos crear archivos comprimidos **.zip** o **.tar** desde la terminal. 🤖
- **.tar** se usa mucho en repositorios. Para comprimir** 

**tar -cvf <nombre>.tar** **<archivos>**, donde c → compress, v → verbose, f→ file. 📁

- **.gz** es un poco mejor, se usa el mismo comando pero con la bandera z→zip 

**tar -cvzf <nombre>.gz <archivos>**. Usa el algoritmo *gzip* que es muy eficiente para comprimir. 📄

- Para descomprimirlo, usamos el mismo comando pero con la bandera x → decompress en lugar de c → compress. Para que funcione, debemos descomprimir debemos usar el mismo tipo de compresión (*tar* o *zip*). 📖
- .zip es uno muy común. Es necesario instalarlo en linux. 

**zip -r <nombre>.zip <directorio>**. Para descomprimir usamos 

**unzip <nombre>.zip.** 📃

- .rar funciona igual que .zip, pero con rar y unrar de comandos 👁️‍🗨️.


## <a name="_q4svybi4133p"></a>Manejo de procesos.
- Cuando se traba nuestro OS, normalmente terminamos procesos con el administrador de tareas 😆, en la terminal se puede hacer, pero es un poco diferente.
- **ps** nos muestra los procesos que están corriendo actualmente. Cada proceso tiene un *PID.* Podemos ver los procesos que estén en el background (por ejemplo, CAT).
- **kill <PID>** nos ayuda a terminar procesos fuera de nuestra terminal. 🛑
- **top <PID>** nos muestra los procesos que están usando más recursos de nuestra computadora. Podemos filtrar los procesos (para ver como, usamos bandera h → help). 🆘
- La terminal, sabiéndola usar bien, es más eficiente que el administrador de tareas.
- **htop** es como **top** pero con esteroides. Debemos instalarlo. Tiene muchas más opciones

es recomiendo htop tiene una interfaz mucho más amigable, lo pueden descargar con: sudo apt install htop y para entrar al programa solo utilizan el comando htop
## <a name="_poyabi8qowjr"></a>Procesos de foreground y background.
- Los procesos que están corriendo pero no se muestran en terminal se dice que están en *background*. Los que si se muestran están en *foregroung*. 🏘️
- Para mover un proceso al background, usamos *Ctrl+z.* Esto lo suspende, pero sigue corriendo (como con Cat). Para matar un proceso se usa *Ctrl+c*
- **fg <numero de trabajo>** nos permite traer un proceso al *foreground*. Es importante notar que el número de trabajo no es lo mismo que el *PID.*
- **bg <numero de trabajo>** nos permite llevar un proceso al *background,* pero sin suspender el proceso.⭐
## <a name="_cksffcmvt9u0"></a>Editores de texto en la terminal.
- Una de las utilidades más importantes de la terminal es el editor de texto.
- Hay diferentes opciones, pero Vim es uno de los mas sencillos y populares. También está Emacs y Nano 🤔.
- **vi <archivo>** es la versión vieja. 👴🏽
- **vim <archivo>**: ***Vi modern***. Tenemos dos modos, el normal o de inserción, para instertar presionamos la tecla *i* y para salir presionamos *Esc.* Para salir del editor y guardar ***:wq**.* 🔒
- Este editor tiene un resaltador de sintaxis 😄 depende del tipo de archivo.
- Al igual que con less para buscar una palabra, podemos hacerlo en Vim con **/<palabra>**. Te lleva a la primera coincidencia.
- Para eliminar una línea, desde el modo normal, nos ponemos al inicio de la línea y presionamos *dd.*

Fin.

