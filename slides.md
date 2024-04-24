# Usabilidad, accesibilidad, SEO y analíticas web

Rubén Silva

---

# Accesibilidad

La accesibilidad web permite a los usuarios con alguna discapacidad navegar por sus interfaces con la menor dificultad posible.

---

# HTML semántico

-   HTML5 nos ofrece una serie de elementos que nos ayudan a estructurar correctamente el contenido:  
    https://developer.mozilla.org/en-US/docs/Web/HTML
-   Estos elementos son: header, nav, main, section, article, aside, footer.
-   Otros elementos extremadamente importantes los h1-h6, que indican la jerarquía del contenido.

---

```html {1-10|12-21|24-28|36-38}{maxHeight:'500px'}
<header>
    <h1>Nombre de la empresa</h1>
    <nav>
        <ul>
            <li><a href="#">Inicio</a></li>
            <li><a href="#">Servicios</a></li>
            <li><a href="#">Contacto</a></li>
        </ul>
    </nav>
</header>
<main>
    <aside>
        <h2>Categorías</h2>
        <nav>
            <ul>
                <li><a href="#">Categoría 1</a></li>
                <li><a href="#">Categoría 2</a></li>
                <li><a href="#">Categoría 3</a></li>
            </ul>
        </nav>
    </aside>
    <section>
        <h2>Últimas entradas</h2>
        <article>
            <h3>Entrada 1</h3>
            <img src="imagen.jpg" alt="Descripción de la imagen" />
            <p>Contenido de la entrada 1</p>
        </article>
        <article>
            <h3>Entrada 2</h3>
            <img src="imagen.jpg" alt="Descripción de la imagen" />
            <p>Contenido de la entrada 2</p>
        </article>
    </section>
</main>
<footer>
    <p>© 2021 Nombre de la empresa</p>
</footer>
```

---

# ARIA: Accessible Rich Internet Applications

Indicar la función de un elemento para que los lectores de pantalla puedan interpretar correctamente el contenido, cuando no sea establecido por un elemento nativo de HTML.

---

-   aria-expanded: true/false. Se usa en los elementos que se expanden o colapsan, como los acordeones o menús.

```html
<nav aria-expanded="true">...</nav>
```

---

-   aria-label: "texto". Se usa para darle un nombre a un elemento que no tiene un texto visible.

```html
<button aria-label="Cerrar">X</button>
```

En caso de tener varios elementos iguales, como nav, se indica su función con aria-label

---

-   role: "nombre". Para indicar que hace un elemento que no es semánticamente correcto.

```html
<a href="#" role="button" aria-label="Cerrar">X</a>
```

---

-   aria-hidden: true/false. Si necesitamos que un elemento no sea accesible para lectores de pantalla, usamos este atributo.

```html
<a href="#">
    Texto visible
    <img src="imagen.jpg" aria-hidden="true" alt="Descripción de la imagen" />
</a>
```

---

# Landmarks

Los lectores de pantalla pueden navegar la página por secciones, llamadas landmarks.

-   banner = header
-   navigation = nav
-   main = main
-   complementary = aside
-   contentinfo = footer

```html
<div role="navigation">...</div>
```

---

También tenemos las regiones, que son secciones que se pueden navegar con el teclado.

```html
<div role="region" aria-label="Últimas Noticias">...</div>
<section aria-label="Noticias destacadas">...</section>
```

---

<div class="grid grid-cols-2 gap-2">
<div>

# Contraste

Es importante que el contraste entre el texto y el fondo sea suficiente para que el texto sea legible.

</div>
<div>

![Contraste](/contraste.webp)

</div>
</div>

---

# Usabilidad

-   Usabilidad es la facilidad de uso de una web.
-   Se trata de que el usuario encuentre lo que busca de forma rápida y sencilla.

---

# Velocidad

-   El primer factor importante a tener en cuenta es la velocidad de carga de la web.
-   Google tiene en cuenta la velocidad de carga para el posicionamiento.
-   Muchos usuarios no esperan más de 3 segundos para que una web cargue.
-   Pagespeed Insights.

---

<div class="grid grid-cols-2 gap-2">
<div>

# Claridad y simplicidad

-   El diseño debe ser claro y sencillo, con un menú de navegación simple y fácil de usar.
-   No debemos sobrecargar la web con elementos innecesarios, distraen al usuario.
-   Categoriza bien la información, la estructura y navegación de tu web para que sea fácil llegar donde se quiere llegar.

</div>
<div>

![Claridad](/claridad.webp)

</div>
</div>

---

<div class="grid grid-cols-2 gap-2">
<div>

# Texto claro y conciso

-   Evita el texto largo y farragoso.
-   Utiliza listas, negritas, títulos, etc. para que el usuario pueda encontrar lo que busca rápidamente.
-   No uses lenguaje técnico, utiliza un lenguaje sencillo y directo.
-   Muy importante la ortografía y gramática correcta.
-   Usa tamaño de letra legible.

</div>
<div>

![Conciso](/texto.webp)

</div>
</div>

---

<div class="grid grid-cols-2 gap-2">
<div>

# Familiaridad

-   Los usuarios están acostumbrados a ciertos patrones de diseño:
    -   Logotipo en la esquina superior izquierda.
    -   Menú de navegación en la parte superior.
    -   Botón de llamada a la acción en la parte inferior.
-   Si cambiamos estos patrones, el usuario se sentirá desorientado y abandonará la web.

</div>
<div>

![Familiaridad](/familiaridad.webp)

</div>
</div>

---

# Diseño responsivo

-   Más del 50% de las visitas a las webs se hacen desde dispositivos móviles.
-   Google también tiene en cuenta la adaptación a dispositivos móviles para el posicionamiento.
-   Pagespeed Insights nos muestra si la web está adaptada a dispositivos móviles.

---

# 404

-   Revisar periódicamente los enlaces de la web para asegurarnos de que no hay enlaces rotos.
-   Si un usuario llega a una página 404, es muy probable que abandone la web.
-   Podemos usar herramientas como Google Search Console para ver los enlaces rotos.

---

<div class="grid grid-cols-2 gap-2">
<div>

# Imágenes y vídeos

-   Utiliza las imágenes, los vídeos y las animaciones con prudencia.
-   Pueden ayudar a separar el texto y hacer que tu sitio web sea más atractivo visualmente.
-   Un número excesivo puede hacer que el sitio parezca recargado.

</div>
<div>

![Clutter](/clutter.webp)

</div>
</div>

---

# Actualizaciones

-   Mantén el sitio actualizado, tanto en contenido como en diseño.
-   Un sitio web desactualizado da una mala impresión y puede hacer que los usuarios piensen que la empresa no está en activo.

---

<div class="grid grid-cols-2 gap-2">
<div>

# Formularios

-   Presta especial atención al diseño de los formularios, ya que son una de las partes más importantes de la web.
-   Deben ser fáciles de rellenar y no pedir más información de la necesaria.
-   Usa siempre labels para identificar los campos del formulario, no uses placeholders como sustitutos de los labels.
-   Intenta validar el formulario en línea, es muy frustrante rellenar un formulario y que al enviarlo, te haga retroceder y volver a rellenar los datos.

</div>
<div>

![Formularios](/form.webp)

</div>
</div>

---

# Test de usabilidad

-   Es muy útil hacer tests de usabilidad con personas que no pertenezcan al equipo y no estén familiarizadas con la web.
-   Podemos hacer tests de usabilidad con herramientas como Hotjar.

---

# Seo

Si hemos seguido todos los pasos anteriores, el seo de nuestra web estará prácticamente hecho. Pero vamos a tomar en cuenta ciertas consideraciones.

---

# Identifica tu competencia

Una de las formas más eficaces de comenzar con la investigación de palabras clave es identificar las palabras clave de la competencia. Podemos hacerlo con herramientas como Ahrefs, SEMrush, Moz, etc.

---

# Keywords y metadatos

-   Basándonos en la investigación de palabras clave, generamos las keywords y metadatos.
-   Usa siempre las propiedades title y meta description.
-   Asegúrate de que todas tus keywords están en el contenido y añade variaciones de las keywords.
-   No abuses de las keywords, ya que Google penaliza el keyword stuffing.
-   Podemos usar herramientas de IA para facilitarnos la labor, ChatGPT o Ahrefs.
-   Evita que más de una página de su sitio utilicen la misma palabra clave e intención.
-   Usa links internos.

---

# RRSS

-   Es importante que la web incluya metadatos para redes sociales, como Open Graph y Twitter Cards.
-   Esto facilitará que los usuarios compartan el contenido en sus redes sociales:  
    <https://autonome.github.io/silobuster/>

---

# Jerarquía de títulos

-   Usa un solo h1 en cada página.
-   Los títulos deben seguir una jerarquía, h1, h2, h3, etc.
-   No uses títulos solo por el tamaño de la letra.

---

# Duplicidad de contenido

No dupliques tu contenido y revisa que no estés sirviendo la web en varios dominios, www.misitio.com y misitio.com son dos dominios diferentes, elige cual es tu dominio principal y redirige todos los demás a él.

---

# Urls amigables

Las estructuras de url compatibles con seo facilitan que los motores de búsqueda rastreen las páginas.

-   Evita usar query strings, por ejemplo: /category.php?id=54

---

# Backlinks

Se trata de uno de los mejores métodos para aumentar el ranking de la web. Básicamente tenemos dos opciones:

1. Crear páginas de alta calidad que atraigan backlinks de forma natural.
2. Promocionarlos en publicaciones relevantes.

---

# Sitemap

-   Crea un sitemap de la web y envíalo a google search console.
-   Puedes usar herramientas online, busca xml sitemap generator para encontrarlas.

---

# robots.txt

robots.txt es un archivo que indica a los motores de búsqueda qué páginas y archivos deben o no rastrear.
Hay cientos de guías disponibles en línea para crear un archivo robots.txt.

```txt
User-agent: Googlebot
User-agent: *
Disallow: /wp-admin/
```

---

# HTTPS

Utiliza siempre https, ya que google tiene en cuenta la seguridad para el posicionamiento. Además, los usuarios confiarán más en tu web si ven que es segura.

---

# schema.org

-   Los buscadores usan datos estructurados para entender el contenido de la web.
-   Puedes usar Schema.org para añadir estos datos a tu web.
-   Si has usado html semántico, parte del trabajo está hecho con etiquetas como addresss, time, etc.
-   Para identificar los elementos se usan propiedades itemtype="" e itemprop="" según las indicaciones de Schema.org.

```html
<div itemscope itemtype="http://schema.org/Movie">
    <h1 itemprop="name">Pirates of the Caribbean: On Stranger Tides (2011)</h1>
</div>
```

---

# Analytics

-   Cada día es mas difícil obtener analíticas y ha empeorado la calidad de las mismas.
-   Actualmente se calcula que se pierden entre 20% y 35% de las estadísticas totales de la web.

Esto es debido a los bloqueadores de publicidad y a las leyes de consentimiento de la UE.  
Ambas causas son beneficiosas para el usuario, pero bastante perjudiciales para la empresa, dado que esos datos son de vital importancia a la hora de generar campañas de marketing o evaluar el funcionamiento de la web.

---

Por eso considero que son tan importantes los pasos previos que hemos mencionado, así tendremos un producto de calidad y no dependeremos tanto del feedback del usuario o de las analíticas para mejorar nuestras conversiones.

Se pueden usar sistemas de analítica orientados a la privacidad como Plausible Analytics o sistemas ejecutados en el propio servidor.
