# Marketing web

## HTML semántico

No sólo afecta a la accesibilidad, sino también a la usabilidad y el SEO.

HTML5 nos ofrece una serie de elementos que nos ayudan a estructurar correctamente el contenido. Estos elementos son: header, nav, main, section, article, aside, footer. También se incluyen y son extremadamente importantes los h1-h6, que indican la jerarquía del contenido.

<https://developer.mozilla.org/en-US/docs/Web/HTML>

Tanto los crawlers de los buscadores como los lectores de pantalla interpretan estos elementos, por lo que es importante usarlos correctamente.

Es muy importante añadir alt en las imágenes, para que los lectores de pantalla puedan interpretarlas. Si la imagen es decorativa, se añade alt="".

## Accesibilidad

### ARIA: Accessible Rich Internet Applications

Principalmente se trata de indicar que un elemento es un botón, una lista, un menú, etc. para que los lectores de pantalla puedan interpretar correctamente el contenido. Siempre que estos elementos no sean establecidos por un elemento nativo de HTML.

- aria-expanded: true/false  
  Se usa en los elementos que se expanden o colapsan, como los acordeones.

- aria-label: "texto"  
  Se usa para darle un nombre a un elemento que no tiene un texto visible. Por ejemplo en iconos svg, para indicar que hace el icono con "Síguenos en instagram". Otro buen ejemplo es un botón con una X para cerrar un modal, en este caso, le indicamos su función con aria-label="Cerrar".  
  En caso de tener varios elementos iguales, como nav, por ejemplo, se indica su función con aria-label, ej: aria-label="Main"

- aria-labelledby: "id"  
  Si un elemento no tiene un texto visible, pero existe un elemento relacionado que contiene texto, como un caption, se puede usar este atributo para relacionarlos.

- role: "nombre"  
  Para indicar que hace un elemento que no es semánticamente correcto, por ejemplo, una imagen que se enlaza mediante javascript, le indicamos que es un botón con role="button".  
  En el ejemplo anterior, además, añadiríamos tabindex="0" para que el elemento sea accesible mediante teclado.  
  Otro ejemplo muy utilizado, es un link con href="#" que se comporta como un botón, en este caso, le indicamos que es un botón con role="button".  
  Semánticamente hablando, el elemento a es un enlace y el elemento button es un botón, por lo que es importante usar el elemento correcto.

- aria-hidden: true/false  
  Si necesitamos que un elemento no sea accesible para lectores de pantalla, usamos este atributo. Se utiliza mucho en enlaces que contienen texto e icono, para no leer el icono o elementos con opacidad 0.

### Landmarks

Los lectores de pantalla pueden navegar la página por secciones, llamadas landmarks. Estas secciones son: banner, navigation, main, complementary, contentinfo, form. Para que un elemento sea reconocido como landmark, se le añade el atributo role="nombre", ej: role="banner". Estos elementos coinciden en HTML5 con elementos semánticos, por lo que no es necesario añadir el atributo role. Banner es el header, navigation es el nav, main es el main, complementary es el aside y contentinfo es el footer.

También tenemos las regiones, que son secciones que se pueden navegar con el teclado. Se usan para indicar que una sección es importante, como un formulario, un menú, etc. se usan con role="region" y aria-label="nombre". Un ejemplo habitual es usarlos dentro de main para indicar las diferentes categorías del contenido. Si usamos el elemento section, no es necesario añadir role="region".

### Contraste

Es importante que el contraste entre el texto y el fondo sea suficiente para que el texto sea legible. Ésto es especialmente importante para personas con problemas de visión. De todas formas, los navegadores y sistemas operativos pueden usar el modo de alto contraste, pero es importante que la web sea semánticamente correcta y accesible para que no haya problemas al usar este modo.

## Usabilidad

Usabilidad es la facilidad de uso de una web. Se trata de que el usuario encuentre lo que busca de forma rápida y sencilla. Hay que considerar siempre que los usuarios son vagos y están muy ocupados, quieren resultados rápidos y fácilmente accesibles. Como empresa, también nos interesa que podamos convertir rápida y fácilmente la visita en una compra, un lead, una suscripción, o cualquier objetivo que nos hayamos marcado. Si la web es difícil de usar, los usuarios se irán a la competencia y perderemos dinero. Debemos diseñar las páginas pensando en el usuario, no en la empresa.

### Velocidad

El primer factor importante a tener en cuenta es la velocidad de carga de la web, que debe ser lo más rápida posible. Google tiene en cuenta la velocidad de carga para el posicionamiento, por lo que es importante tenerla en cuenta. Además, los usuarios no esperan más de 3 segundos para que una web cargue, por lo que si tarda más, se irán a la competencia. Un buen hosting es clave en este sentido, no solo por la velocidad, sino también por la seguridad. Podemos medir la velocidad de carga con herramientas como Pagespeed Insights, Gtmetrix o Pingdom.

### Claridad y simplicidad

El diseño debe ser claro y sencillo, con un menú de navegación simple y fácil de usar. No debemos sobrecargar la web con elementos innecesarios, ya que distraen al usuario y dificultan su manejo. Debe haber un equilibrio entre la cantidad de información y la claridad. Los espacios en blanco son una parte muy importante del diseño, ya que ayudan a separar los elementos y a que la web sea más fácil de leer.

Categoriza bien la información y la estructura y navegación de tu web para que sea fácil llegar donde se quiere llegar.

#### Texto claro y conciso

Evita el texto largo y farragoso. Los usuarios no leen, escanean. Utiliza listas, negritas, títulos, etc. para que el usuario pueda encontrar lo que busca rápidamente. No uses lenguaje técnico, utiliza un lenguaje sencillo y directo. No uses jerga, a no ser que estés seguro de que tu público la entiende. Resaltar la importancia de la ortografía y gramática correcta, hará que la web sea más profesional y confiable.

Usa tamaño de letra legible, no uses tamaños muy pequeños. Intenta no centrar o justificar los párrafos, pierden legibilidad, asegúrate de que los párrafos no son muy largos.

### Familiaridad

Los usuarios están acostumbrados a ciertos patrones de diseño, por lo que es importante seguirlos. Por ejemplo, el logotipo en la esquina superior izquierda, el menú de navegación en la parte superior, el botón de llamada a la acción en la parte inferior, etc. si cambiamos estos patrones, el usuario se sentirá desorientado y abandonará la web.

### Diseño responsivo

Más del 50% de las visitas a las webs se hacen desde dispositivos móviles, por lo que es importante que la web esté adaptada a estos dispositivos. Google también tiene en cuenta la adaptación a dispositivos móviles para el posicionamiento. Pagespeed Insights nos muestra si la web está adaptada a dispositivos móviles.

### 404

Revisar periódicamente los enlaces de la web para asegurarnos de que no hay enlaces rotos. Si un usuario llega a una página 404, es muy probable que abandone la web. Podemos usar herramientas como google console para ver los enlaces rotos.

Ésta herramienta no solo nos muestra los enlaces rotos, sino que también nos muestra los errores de rastreo, que pueden ser causados por enlaces rotos, redirecciones mal configuradas, etc.

### Imágenes y vídeos

Utiliza las imágenes y los vídeos con prudencia. Pueden ayudar a separar el texto y hacer que tu sitio web sea más atractivo visualmente. Sin embargo, un número excesivo puede hacer que el sitio parezca recargado.

### Actualizaciones

Mantén el sitio actualizado, tanto en contenido como en diseño. Un sitio web desactualizado da una mala impresión y puede hacer que los usuarios piensen que la empresa no está en activo. Un caso habitual es incluir un blog y no actualizarlo. Es mejor no tenerlo que tenerlo desactualizado.

### Formularios

Presta especial atención al diseño de los formularios, ya que son una de las partes más importantes de la web. Deben ser fáciles de rellenar y no pedir más información de la necesaria. Si el formulario es muy largo, es probable que el usuario abandone la web. Si el formulario es para una compra, es importante que el usuario pueda ver el resumen de la compra antes de finalizarla.

Usa siempre labels para identificar los campos del formulario, no uses placeholders como sustitutos de los labels. Los placeholders no son accesibles y no se ven si el campo se ha rellenado. Intenta que los labels estén encima de los inputs, para que el usuario pueda verlos mientras rellena el formulario.

Intenta validar el formulario en línea, es muy frustrante rellenar un formulario y que al enviarlo, te haga retroceder y volver a rellenar los datos.

### Test de usabilidad

Es muy útil hacer tests de usabilidad con personas que no pertenezcan al equipo y no estén familiarizadas con la web. Podemos hacer tests de usabilidad con herramientas como Hotjar, que nos permite grabar la sesión de los usuarios, ver heatmaps, encuestas, etc.

## Seo

Si hemos seguido todos los pasos anteriores, el seo de nuestra web estará prácticamente hecho. Pero vamos a tomar en cuenta ciertas consideraciones.

### Keywords y metadatos

Usa siempre las propiedades title y meta description. Usa links internos. Asegúrate de que todas tus keywords están en el contenido y añade variaciones de las keywords. Evita que más de una página de su sitio utilicen la misma palabra clave e intención.

#### Identifica tu competencia

Una de las formas más eficaces de comenzar con la investigación de palabras clave es identificar las palabras clave de la competencia. Podemos hacerlo con herramientas como Ahrefs, SEMrush, Moz, etc.

#### Generar keywords y metadatos

Basándonos en la investigación de palabras clave, generamos las keywords y metadatos. Es importante que las keywords estén en el título, la descripción, el contenido, las imágenes, etc. No abuses de las keywords, ya que Google penaliza el keyword stuffing. Podemos usar herramientas de IA para facilitarnos la labor, ChatGPT o Ahrefs son dos ejemplos.

#### RRSS

Es importante que la web incluya metadatos para redes sociales, como Open Graph y Twitter Cards. Esto facilitará que los usuarios compartan el contenido en sus redes sociales. Me gusta mucho esta herramienta para generarlos de forma fácil: <https://autonome.github.io/silobuster/>

### Jerarquía de títulos

Usa un solo h1 en cada página, que sea el título principal de la página. Los títulos deben seguir una jerarquía, h1, h2, h3, etc. no uses títulos solo por el tamaño de la letra, sino por la jerarquía del contenido.

### Duplicidad de contenido

No dupliques tu contenido y revisa que no estés sirviendo la web en varios dominios, www.misitio.com y misitio.com son dos dominios diferentes, elige cual es tu dominio principal y redirige todos los demás a él.

### Urls amigables

Las estructuras de url compatibles con seo facilitan que los motores de búsqueda rastreen las páginas, evita usar query strings, por ejemplo:

```
/category.php?id=54
```

### Backlinks

Se trata de uno de los mejores métodos para aumentar el ranking de la web. Básicamente tenemos dos opciones:

1. Crear páginas de alta calidad que atraigan backlinks de forma natural.
2. Promocionarlos en publicaciones relevantes.

### Sitemap

Crea un sitemap de la web y envíalo a google console. Esto le facilitará a google el rastreo de la web. Puedes usar herramientas como Xml Sitemap Generator para crear el sitemap.

### robots.txt

robots.txt es un archivo que indica a los motores de búsqueda qué páginas y archivos deben o no rastrear. Hay cientos de guías disponibles en línea para crear un archivo robots.txt.

### HTTPS

Utiliza siempre https, ya que google tiene en cuenta la seguridad para el posicionamiento. Además, los usuarios confiarán más en tu web si ven que es segura.

### schema.org

Los buscadores usan datos estructurados para entender el contenido de la web. Puedes usar Schema.org para añadir estos datos a tu web. Si has usado html semántico, parte del trabajo está hecho con etiquetas como addresss, time, etc. Para identificar los elementos se usan propiedades itemtype="" e itemprop="" según las indicaciones de Schema.org.

## Analytics

Más que explicar de que se trata o como hacerlo, me gustaría abordar una situación incómoda. Cómo cada día es mas difícil obtener analíticas y cómo ha empeorado la calidad de las mismas. Actualmente se calcula que se pierden entre 20% y 35% de las estadísticas totales de la web. Esto es debido a los bloqueadores de publicidad y a las leyes de consentimiento de la UE. Ambas causas son beneficiosas para el usuario, pero bastante perjudiciales para la empresa, dado que esos datos son de vital importancia a la hora de generar campañas de marketing o evaluar el funcionamiento de la web. Por suerte hay alguna solución, pero no son fáciles ni simples de implementar y son totalmente incompatibles con Google Adsense y herramientas similares.

Tened esto en cuenta en todo momento, las analíticas son muy útiles, pero no podéis fiaros de ellas al 100%. Por eso considero que son tan importantes los pasos previos que hemos mencionado, así tendremos un producto de calidad y no dependeremos tanto del feedback del usuario o de las analíticas para mejorar nuestras conversiones.

De todas formas, se pueden usar sistemas de analítica orientados a la privacidad como Plausible Analytics o sistemas ejecutados en el propio servidor. A la vez, se pueden implementar proxies que ejecuten las llamadas a Google Analytics desde el servidor, para así evitar los bloqueadores de publicidad. Pero en ningún caso podremos evitar que un usuario rechace las cookies de nuestro sitio web. Sin las cookies la trazabilidad del usuario se vuelve muy difícil y la fiabilidad de los datos obtenidos se reduce drásticamente.
