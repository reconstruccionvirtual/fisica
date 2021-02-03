
![](https://d7lju56vlbdri.cloudfront.net/var/ezwebin_site/storage/images/_aliases/img_1col/noticias/actualizada-la-estrategia-de-fisica-de-particulas-europea/8302208-1-esl-MX/Actualizada-la-estrategia-de-fisica-de-particulas-europea.jpg)
# Actividad 3 - Laboratorio de física de partículas.
## Antoni Oseni Triado / David Lasanta Ajona


## Objetivo

Simular la interacción básica de partículas con ciertos medios gracias al software [Geant4](https://geant4.web.cern.ch/geant4/), desarrollado por el [CERN](http://home.cern/).

En este laboratorio vamos a manejar una serie de [contenedores **Docker**](https://www.docker.com/) para _orquestar_ una serie de servicios sencillos _virtualizados_. En lugar de instalar Docker en nuestra computadora (que podríamos hacerlo perfectamente), vamos usar el servicio gratuito [Play with Docker](https://labs.play-with-docker.com/).

Este servicio no es más que un _playground_ para que, quien quiera pueda explorar la creación y gestión de contenedores virtuales basados en [Docker](https://www.docker.com/). Vamos a ver en qué consiste.


## Preguntas

### ¿Cuál es la diferencia entre una imagen y un contenedor? 

>Al discutir la diferencia entre imágenes y contenedores, no es justo contrastarlos como entidades opuestas. Ambos elementos están estrechamente **relacionados y forman parte de un sistema** definido por la plataforma Docker.

>Las imágenes pueden existir sin contenedores, mientras que un contenedor necesita ejecutar una imagen para existir. Por lo tanto, los contenedores dependen de las imágenes y las utilizan para construir un entorno de tiempo de ejecución y ejecutar una aplicación.

>Los dos conceptos existen como componentes esenciales (o más bien fases) en el proceso de ejecución de un contenedor Docker. Tener un contenedor en ejecución es la "fase" final de ese proceso, lo que indica que depende de los pasos y componentes anteriores. Es por eso que las imágenes de Docker esencialmente gobiernan y dan forma a los contenedores.
>`echo ip$(ifconfig eth1 | grep "inet " | awk -F'[: ]+' '{ 
    print $4 }' | sed 's/\./-/g')-$SESSION_ID`

    
### ¿qué hace el comando anterior? 

>Con el comando **echo**, se imprime en pantalla una lineal formada por parte del contendido de la información que arroja la consulta `ifconfig eth1`, percedido de la 
Concretamente la información relativa a la información `inet` que alberga la **ip**.
Ejemplo: `inet addr:172.18.0.56 Bcast:0.0.0.0 Mask: 255.255.0.0`
Las ordenes seguidas **awk** y **sed** extraen la ip y la muestran con '-': `172-18-0-56`
Por último **echo** captura la información de sesión de `$SESSION_ID`
La concatenación de todos los comandos imprimiría en consola, por ejemplo: `ip172-18-0-56-c0dfa8k34gag00ac6tj0`


### ¿De qué subcomandos se compone y qué papel juegan (`ifconfig`,`grep`, `awk`y `sed`)?

>**ifconfig** («configuración de interfaz») es un programa disponible en varias versiones del sistema operativo UNIX/Linux/OsX, que permite configurar o desplegar numerosos parámetros de las interfaces de red residentes en el núcleo, como la dirección IP (dinámica o estática), o la máscara de red. 

>**grep** es una utilidad de la línea de comandos escrita originalmente para ser usada con el sistema operativo Unix.
Usualmente, grep toma una expresión regular de la línea de comandos, lee la entrada estándar o una lista de archivos, e imprime las líneas que contengan coincidencias para la expresión regular.

>**awk** o GNU awk en específico proporciona un lenguaje de scripting para el procesamiento de texto. Con el lenguaje de scripting awk puedes:
>- Definir variables.
>- Utilizar cadenas y operadores aritméticos.
>- Utilizar control de flujo y ciclos.
>- Generar reportes con formato.
>
>Actualmente, puedes procesar archivos de registro que contengan tal vez millones de líneas de salida, a un reporte del cual te puedes beneficiar.

>**sed** es utilizado para trabajar con archivos de texto como archivos de registro, archivos de configuración y otros archivos de texto.
>Se utiliza para manipulación de texto, Los sistemas Linux proporcionan algunas herramientas para el procesamiento de texto, una de esas herramientas es **sed**.

### ¿Qué otros formatos estándar de representación 3D conoces (Collada, Stanford, Wavefront, X3D Extensible, Standard Tessellation Language, x3dom, etc.)?
>.3ds, .blend, .3mf, .dxf, .vrlm, .stl, .obj

### ¿Quién desarrolla Instant Player qué contribuciones ha hecho al mundo de la tecnología?
> Se ha desarrollado en Fraunhofer IGD y ZGDV en estrecha colaboración con otros socios industriales.

### ¿En qué proyectos está involucrada la fundación Kitware y cómo han cambiado el mundo de la informática, la tecnología, la ciencia y la medicina?
>**Kitware, Inc.** es una compañía de tecnología ubicada en [Clifton Park](https://es.wikipedia.org/wiki/Clifton_Park "Clifton Park"), [Nueva York](https://es.wikipedia.org/wiki/Nueva_York "Nueva York"), especializada en la investigación y desarrollo de [software de código abierto](https://es.wikipedia.org/wiki/Software_de_c%C3%B3digo_abierto "Software de código abierto") en las áreas de [visión por computador](https://es.wikipedia.org/wiki/Visi%C3%B3n_por_computador "Visión por computador"), [imágenes médicas](https://es.wikipedia.org/wiki/Im%C3%A1genes_m%C3%A9dicas "Imágenes médicas"), [visualización científica](https://es.wikipedia.org/wiki/Visualizaci%C3%B3n_cient%C3%ADfica "Visualización científica") y análisis de información multidimensional. Además del desarrollo de software, la compañía ofrece otros productos y servicios como libros, manuales, soporte técnico, consultoría y cursos de entrenamiento personalizado, que han contribuido a cambios en la informática, la tecnología, la ciencia y la medicina.

### ¿Qué es Docker? 
>Docker es un proyecto de código abierto que automatiza el despliegue de aplicaciones dentro de contenedores de software, proporcionando una capa adicional de abstracción y automatización de virtualización de aplicaciones en múltiples sistemas operativos. Docker utiliza características de aislamiento de recursos del kernel Linux, tales como cgroups y espacios de nombres (namespaces) para permitir que "contenedores" independientes se ejecuten dentro de una sola instancia de Linux, evitando la sobrecarga de iniciar y mantener máquinas virtuales. 
El soporte del kernel Linux para los espacios de nombres aísla la vista que tiene una aplicación de su entorno operativo, incluyendo árboles de proceso, red, ID de usuario y sistemas de archivos montados, mientras que los cgroups del kernel proporcionan aislamiento de recursos, incluyendo la CPU, la memoria, el bloque de E/S y de la red. Desde la versión 0.9, Docker incluye la biblioteca libcontainer como su propia manera de utilizar directamente las facilidades de virtualización que ofrece el kernel Linux, además de utilizar las interfaces abstraídas de virtualización mediante libvirt, LXC (Linux Containers) y systemd-nspawn.
De acuerdo con la firma analista de la industria Research, *"Docker es una herramienta que puede empaquetar una aplicación y sus dependencias en un contenedor virtual que se puede ejecutar en cualquier servidor Linux".* Esto ayuda a permitir la flexibilidad y portabilidad en donde la aplicación se puede ejecutar, ya sea en las instalaciones físicas, la nube pública, nube privada, etc

### ¿Qué son los contenedores virtuales?
>Un **contenedor Docker** es un entorno de tiempo de ejecución virtualizado donde los usuarios pueden aislar aplicaciones del sistema subyacente. Estos contenedores son unidades compactas y portátiles en las que puede iniciar una aplicación de forma rápida y sencilla.

### ¿Qué alternativas a Docker existen (OpenVZ, LXC, Vagrant, rkt, Singularity, etc.)? 
>Jira, Bitbucket, Azure, Appy Pie, Anypoint Platform, GitLab, Heroku...

### Resume brevemente la historia de Docker.
>Solomon Hykes comenzó Docker como un proyecto interno dentro dotCloud,​ empresa enfocado a una plataforma como un servicio (PaaS),​ con las contribuciones iniciales de otros ingenieros de dotCloud, incluyendo Andrea Luzzardi y Francois-Xavier Bourlet. Jeff Lindsay también participó como colaborador independiente. Docker representa una evolución de la tecnología patentada de dotCloud, que es a su vez construida sobre proyectos de código abierto anteriores como Cloudlets.

>Docker fue liberado como código abierto en marzo de 2013. El 13 de marzo de 2014, con el lanzamiento de la versión 0.9, Docker dejó de utilizar LXC como el entorno de ejecución por defecto y lo reemplazó con su propia biblioteca, libcontainer, escrito en [_Go_](https://es.wikipedia.org/wiki/Go_(lenguaje_de_programaci%C3%B3n) "Go (lenguaje de programación)"). El 13 de abril de 2015, el proyecto tenía más de 20 700 estrellas de [GitHub](https://es.wikipedia.org/wiki/GitHub "GitHub") (haciéndolo uno de los proyectos con más estrellas de GitHub, en 20ª posición), más de 4 700 [bifurcaciones (_forks_)](https://es.wikipedia.org/wiki/Bifurcaci%C3%B3n_(desarrollo_de_software) "Bifurcación (desarrollo de software)"), y casi 900 colaboradores.

>Un análisis en 2018 mostró las siguientes organizaciones como las principales contribuyentes de Docker: [Red Hat](https://es.wikipedia.org/wiki/Red_Hat "Red Hat") (mayores contribuyentes, aún más que el equipo de Docker en sí), el equipo de Docker, [Microsoft](https://es.wikipedia.org/wiki/Microsoft "Microsoft"), [IBM](https://es.wikipedia.org/wiki/IBM "IBM"), [Google](https://es.wikipedia.org/wiki/Google "Google"), [Cisco Systems](https://es.wikipedia.org/wiki/Cisco_Systems "Cisco Systems") y [Amadeus IT Group](https://es.wikipedia.org/wiki/Amadeus_IT_Group "Amadeus IT Group").

>El 29 de julio de 2020 se dio a conocer la existencia de Doki, un malware que corre en el sistema operativo Linux que tiene por finalidad infectar la API de los contenedores Docker mal configurados. Algunas de sus acciones son las siguientes:

>Crea URL única con vidas cortas para descargar payloads durante el ataque.
>Ha sido creado para ejecutar comandos recibidos desde sus operadores.
>Usa la biblioteca TLS para funciones criptografica.

### ¿Por qué Docker se ha convertido en un software tan popular?
>Con los avances tecnológicos, han aparecido soluciones cada vez más eficientes que garantizan el mejor desempeño de las plataformas. Después de la virtualización, la tecnología de contenedores (containers) ha llegado a ganar espacio y popularidad y ahí es donde encontramos **Docker**.

### ¿Qué es un fichero ppk?
>Son archivos clave y sirven como almacenamiento para las claves privadas. Estos archivos se utilizan para permitir la comunicación segura con otra parte que tenga la clave pública correspondiente.

### ¿Qué es una clave RSA público/privada (fichero key)?
>**RSA**  _(**[Rivest](https://es.wikipedia.org/wiki/Ronald_Rivest "Ronald Rivest"),  [Shamir](https://es.wikipedia.org/wiki/Adi_Shamir "Adi Shamir")  y  [Adleman](https://es.wikipedia.org/wiki/Leonard_Adleman "Leonard Adleman")**)_ es un [sistema criptográfico de clave pública](https://es.wikipedia.org/wiki/Criptograf%C3%ADa_asim%C3%A9trica "Criptografía asimétrica") desarrollado en [1979](https://es.wikipedia.org/wiki/1979 "1979"), que utiliza [factorización](https://es.wikipedia.org/wiki/Factorizaci%C3%B3n "Factorización") de números enteros. Es el primer y más utilizado [algoritmo](https://es.wikipedia.org/wiki/Algoritmo "Algoritmo") de este tipo y es válido tanto para cifrar como para [firmar digitalmente](https://es.wikipedia.org/wiki/Firma_digital).

### ¿Qué es el [Hub](https://hub.docker.com/) de Docker?
>Docker Hub es un servicio proporcionado por Docker para encontrar y compartir imágenes de contenedores en nuestros ordenadores.
>![](https://pbs.twimg.com/media/CYbab8dWAAA4CCi.png)
### ¿Cómo se llama a este [tipo de haz](https://htmlpreview.github.io/?https://github.com/pammacdotnet/FFRepo/blob/master/geant4lab2021.html#search=%22pencil%20beam%22) de partículas?
>RayosX

### ¿Qué son los archivos `wrl`? 
>Mundo virtual creado en VRML: el lenguaje de modelado de realidad virtual; Se puede navegar en tres dimensiones; Contiene coordenadas y colores que definen cada objeto y forma; También incluye las coordenadas del punto de vista para la vista inicial de la escena 3D.

### ¿De qué estándar internacional se trata?
> Actualmente, el soporte de VRML sigue siendo parte de las características estándar de exportación/importación en muchos títulos de software de CAD y modelado. Un archivo del mundo VRML (.wrl) puede ser importado en una aplicación de modelado CAD/3D o abierto y visualizado con un navegador web habilitado para VRML.

### ¿Cómo es posible que veamos figuras 3D en una página web? 
>Los tipos de archivo VRML permiten que los complementos del navegador muestren entornos de realidad virtual. El término VRML a menudo se conoce como "mundos" o archivo mundial vrml, que es también lo que realmente significa WRL.
>Los archivos WRL ayudan a los navegadores a renderizar polígonos 3D con detalles como vértices, bordes, colores de superficie, texturas mapeadas, mapas de luz y reflejos. 

### ¿Qué estándares, alternativas, consorcios e instituciones están implicados? 
>Un breve comentario sobre su historia: el principal impulso de VRML se remonta a las  sesiones de aves de las características  sobre  Lenguajes de marcado de realidad virtual  en la Primera Conferencia Internacional sobre la World-Wide-Web , mayo 25-27 de 1994 en el CERN de Ginebra. Sus orígenes conceptuales son más antiguos, por ejemplo, (a) literatura de ciencia ficción (por ejemplo, [ Gibson, 1994 ], [ Stephenson, 1992 ]),  el sistema  Labyrinth  de Mark Pesce, P. Kennard y Toni Parisi ([ Pesce et al., 1994 ]) y una propuesta para un esquema de navegación y representación en 3-D y más generalmente gráficos por computadora en 3-D (incluida la realidad virtual). Basado en el formato Open Inventor  de SGI, se presentó un borrador casi final de VRML 1.0 en la segunda conferencia de la WWW. en el otoño del 94 en Chicago. El 3 de abril de 1995 SGI presentó WebSpace, el primer navegador VRML disponible públicamente. Entonces, en general, tomó alrededor de un año establecer estándares y hacer que el primer navegador estuviera disponible. Dado que VRML es un formato relativamente simple que se basa en un estándar bien definido, muy rápidamente también estuvieron disponibles varias herramientas de modelado y convertidores.

### ¿Qué alternativa estamos usando en este ejercicio (pista) y qué gran centro de investigación en matemáticas estuvo implicado?
>Un "Mundo Virtual" creado en VRML, en un fichero `simulation.wrl`
>Association for Computing Machinery, ha estado implicado.

### ¿Cuánto tiempo puede estar serpenteando un fotón que nace en el centro del Sol hasta llegar a la retina de cualquiera de tus ojos?
>Los fotones van «rebotando» de carga en carga, dando pasos en direcciones que podemos suponer aleatorias, de manera que no todos los pasos les permiten avanzar en su salida del Sol. El hecho de que reboten, en lugar de poder ser absorbidos y reemitidos por los electrones, es porque las cargas libres no pueden absorber fotones, ya que se violaría la conservación simultánea de energía y momento lineal. Por tanto asumimos que los fotones rebotan sobre las cargas libres del Sol, saliendo despedidas en ángulos aleatorios. A este tipo de movimiento se le conoce en física como «paseo del borracho» o, si queremos ser políticamente correctos, caminata al azar.
>Pueden tardar **miles de años**.

### ¿Qué es un positrón? 
>El positrón o antielectrón es una partícula elemental, antipartícula del electrón. Posee la misma cantidad de masa y espín que el electrón

### ¿Quién postuló su existencia teórica y cuándo y cómo se descubrió experimentalmente?
>Esta partícula fue predicha por Paul Dirac en 1928, para luego ser descubierta en 1932 por el físico estadounidense Carl David Anderson al fotografiar las huellas de los rayos cósmicos en una cámara de niebla. 

### ¿Qué relación tiene la modalidad radiológica PET con la aniquilación de pares electrón-positrón? 
>La reacción e+ + e- → γ + γ se conoce como aniquilación positrón-electrón. Consiste en la conversión total de la masa de un [electrón](https://es.wikipedia.org/wiki/Electr%C3%B3n "Electrón") y un [positrón](https://es.wikipedia.org/wiki/Positr%C3%B3n "Positrón") en energía, es la forma más observada de aniquilación partícula-antipartícula.

>Puesto que la aniquilación de pares es un proceso fruto de la [interacción electromagnética](https://es.wikipedia.org/wiki/Interacci%C3%B3n_electromagn%C3%A9tica "Interacción electromagnética") la energía siempre se emitirá en forma de [rayos gamma](https://es.wikipedia.org/wiki/Rayos_gamma "Rayos gamma"). Si las partículas se mueven a velocidades mucho menores que la de la luz o se encuentran en reposo, se producirán 2 [fotones](https://es.wikipedia.org/wiki/Fot%C3%B3n "Fotón") emitidos en la misma dirección pero con sentidos opuestos, cada uno con una energía de 0.511 [MeV](https://es.wikipedia.org/wiki/MeV "MeV"), lo que coincide con las masas en reposo del electrón y del positrón. Normalmente ambas partículas formarán previamente un [estado ligado](https://es.wikipedia.org/w/index.php?title=Estado_ligado&action=edit&redlink=1 "Estado ligado (aún no redactado)") conocido como [positronio](https://es.wikipedia.org/wiki/Positronio "Positronio") el cual es inestable y termina siempre con la aniquilación.

>![](https://pammachome.files.wordpress.com/2018/12/aniquilacion.jpg)
### ¿Cómo se trasladan positrones hasta el interior de las células cancerígenas?
>Las unidades de emisión única de fotones de tomografía computarizada/tomografía computarizada (SPECT/TC) y tomografía/tomografía computarizada por emisión de positrones (PET/TC) pueden realizar ambos exámenes por imágenes al mismo tiempo. La PET/MRI es una tecnología emergente de toma de imágenes. Sin embargo, hoy en día, no se encuentra universalmente disponible.
La exploración por PET mide funciones importantes del cuerpo tales como el metabolismo. Ayuda a los médicos a evaluar cuán bien están funcionando los órganos y tejidos.
Las imágenes por TC utilizan un equipo especial de rayos X, y en algunos casos un material de contraste, para producir múltiples imágenes del interior del cuerpo. Un radiólogo observa e interpreta estas imágenes en el monitor de una computadora. Las imágenes por TC proporcionan excelente información anatómica.
Hoy en día, casi todas las exploraciones por PET se hacen con los exploradores combinados PET/TC. Estas exploraciones combinadas ayudan a identificar actividad metabólica anormal y pueden proporcionar diagnósticos más precisos que cuando se realizan las dos exploraciones en forma separada.

## Laboratorio

### Preparativos previos.

- Solicitud de instancia:
![](https://i.imgur.com/C9S9exH.png)

- Generar variable **usuariopwd**:
![](https://i.imgur.com/1FZhlFx.png)
- Adjudicar permisos a geant4lab.key:
![](https://i.imgur.com/Oxc227b.png)
- Conectar a la instancia **docker** por **ssh**:
![](https://i.imgur.com/akAV02A.png)
- Ordenamos a la instancia de **docker** descargar la imagen del laboratorio, con el comando **ssh**: `ssh -l $usuariopwd direct.labs.play-with-docker.com -i geant4lab.key "/usr/local/bin/docker pull pammacdotnet/g4lpwd"`
![enter image description here](https://i.imgur.com/TNXEY5R.png)

- En la instancia de **docker** y a traves de la interfaz web, descargammos el fichero `simulation.py` con el comando `curl https://raw.githubusercontent.com/pammacdotnet/FFRepo/master/simulation.py -o simulation.py -s`
![enter image description here](https://i.imgur.com/kHaJgJC.png)
- De igual manera, descarga el fichero `wrl2html.py`, que servirá más tarde para generar versiones WebGL de las simulaciones: `curl https://raw.githubusercontent.com/pammacdotnet/FFRepo/master/wrl2html.py -o wrl2html.py -s`

![enter image description here](https://i.imgur.com/N1gb7Xv.png)
Tamben asignamos permisos de ejecución al archivo con `chmod +x wrl2html.py`

### Ejecución de las simulaciones

- Ordenamos desde nuestra máquina local por **ssh**, la ejecución de la simulación: `ssh -l $usuariopwd direct.labs.play-with-docker.com -i geant4lab.key "/usr/local/bin/docker run -v \${PWD}:/root pammacdotnet/g4lpwd"` y que arroja un *log* de resultados con este final:
![enter image description here](https://i.imgur.com/onX3WVO.png)
* La ejecución de la simulación, ha generado un fichero `simulation.wrl` que se puede ver en la *interfaz web* con el comando `ls`:
* ![enter image description here](https://i.imgur.com/JCt9htI.png)

### Visualización de la simulación
* Descargamos de la *instancia docker* el archivo simulation.wrl a nuestra máquina local con `scp -i geant4lab.key -o User=$usuariopwd direct.labs.play-with-docker.com:/root/simulacion.wrl simulacion.wrl` y comprobamos que se ha descargado con el comando `ls`:
![enter image description here](https://i.imgur.com/HjHwSo2.png)
* Aunque ya se pueden ver los resultados con *Instant Player* o similar, aprovechamos el interface web de docker para generar un archivo *html* desde el *wrl*: `ssh -l $usuariopwd direct.labs.play-with-docker.com -i geant4lab.key "/usr/bin/python3 /root/wrl2html.py"`, desde nuestra máquina local por **ssh** y comprobamos que se ha creado correctamente en la interface web de **docker**:
![enter image description here](https://i.imgur.com/kR3NWyc.png)
* Descargamos el archivo *html* en nuestra máquina local con `scp -i geant4lab.key -o User=$usuariopwd direct.labs.play-with-docker.com:/root/simul
ation.html simulation.html
` y comprobamos su descarga con **ls**:
![enter image description here](https://i.imgur.com/f7TDuFl.png)

### Resultados:
![enter image description here](https://i.imgur.com/SqcvUCA.png)

#### Nueva simulación con baja energía, que provoca que los fotones no traspasen la barrera
- Código: `ssh -l $usuariopwd direct.labs.play-with-docker.com -i geant4lab.key "/usr/local/bin/
docker run -v \${PWD}:/root pammacdotnet/g4lpwd" --energy=0.01
`
- Resultado:
![enter image description here](https://i.imgur.com/NDgOPiC.png)

#### Nueva simulación con aumentando energía, que provoca el efecto *Compton*:
- Código: `ssh -l $usuariopwd direct.labs.play-with-docker.com -i geant4lab.key "/usr/local/bin
docker run -v \${PWD}:/root pammacdotnet/g4lpwd" --energy=0.1
`
- Resultado:
![enter image description here](https://i.imgur.com/JXSWUOM.png)

La simulación está disponible hasta fin de curso en la *url*:
http://apps.stpservicom.com:81/fisica/simulation.html
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY3NTMzMzQ4Miw3NzIzMTMwMzUsLTEyOT
k2OTc3NDEsLTE1MjQ0NDcxMDUsLTMxNTI3MDkxMywtODc2NzI1
NDA3LC01OTkzNjk5NzYsLTEwNDE3NTQyOTMsLTE0MzE4MTAwNT
YsLTg4MzA4OTIzNCwxNTQ1Njk1NzE4LC0xNDEwODg0OTUyLDU3
MTA2Mjg0MCwxMTgwODc3NDc2LC0yMTQwODAxNzkxLC0xNzQ1ND
k5MTUsOTk4NTY0MzkwLDEzNDkyNjIwNjBdfQ==
-->