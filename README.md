# WORKSHOP 5 - PÁGINA DE NOTICIAS

Objetivo: Creación de una aplicación de noticias utilizando React Router, Chakra y que realice llamadas a un API ficticio alojado en Github y que nos devolverá 5 páginas de contenido para estas 3 categorías:

**Deportes:**

<https://raw.githubusercontent.com/The-Valley-School/react-w5-newspaper/main/api/sport/1.json>

...

<https://raw.githubusercontent.com/The-Valley-School/react-w5-newspaper/main/api/sport/5.json>

**Economía:**

<https://raw.githubusercontent.com/The-Valley-School/react-w5-newspaper/main/api/economics/1.json>

...

<https://raw.githubusercontent.com/The-Valley-School/react-w5-newspaper/main/api/economics/5.json>

**Tecnología:**

<https://raw.githubusercontent.com/The-Valley-School/react-w5-newspaper/main/api/tech/1.json>

...

<https://raw.githubusercontent.com/The-Valley-School/react-w5-newspaper/main/api/tech/5.json>

**PASO 1:**

Crea un proyecto nuevo con Create React App e instalar React Router y Chakra como dependencias.

Revisa todos los pasos de la instalación de Chakra y no te olvides de nada, por ejemplo el ChakraProvider

Deshabilita el modo estricto de React, ya que en desarrollo te causará lanzar dos peticiones en cada pintado y esto puede provocar que te bloqueen el API:

```jsx
root.render(
  // <React.StrictMode>
    <App />
  // </React.StrictMode>
);
```

**PASO 2:**

Crear un componente principal "App" que actúe como contenedor de la aplicación y utilice React Router para gestionar la navegación entre diferentes páginas.

Deberás tener las siguientes rutas y componentes asociados:

- La raíz (/) pintará el componente Home
- /noticias pintará el componente NoticiasHome que tendrá un selector de categorías
- /noticias/:topic pintará el componente Noticias y recibirá por parámetros la categoría de las noticias a mostrar (así podremos buscarlas en el API)
- Añade una página 404 para todas las demás urls

**PASO 3:**

Realiza el componente Home. Este deberá tener contenido estático y todo estará maquetado haciendo uso de componentes de Chakra.

Haz uso de al menos estos componentes de chakra:

- Heading
- Text
- Image
- Link
- Box

Deberá verse de la siguiente manera:

![Untitled](/assets//Untitled.png)

**PASO 4:**

Crea el componente NoticiasHome, este mostrará nos botones para navegar a cada una de las categorias de noticias:

/noticias/sports

/noticias/tech

/noticias/economics

Deberás verse así:

![Untitled](/assets//Untitled%201.png)

Deberás usar todos los siguientes componentes de Chakra que puedas.

**PASO 5:**

Crea el componente Noticias. Este será el encargado de realizar las llamadas al API.

Fíjate que en la URL podemos poner el tema y la página:

<https://raw.githubusercontent.com/The-Valley-School/react-w5-newspaper/main/api/economics/3.json>

Al final de este componente deberás incluir unos botones para paginar, debes controlar que solo puedan verse las páginas de la 1 a la 5.

La página debe estar maquetada con componentes de Chakra y debe quedar así:

INICIO:

![Untitled](/assets//Untitled%202.png)

FINAL:

![Untitled](/assets//Untitled%203.png)

**PASO 6:**

Implementa el buscador que ves en la parte superior de la página de manera que se filtren los artículos mostrados en pantalla solo si el título contiene el texto buscado, por ejemplo:

![Untitled](/assets//Untitled%204.png)
