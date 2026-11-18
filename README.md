# 🖼️ Buscador de Imágenes Pixabay

Aplicación web desarrollada con **HTML5, CSS3 y JavaScript** que permite buscar imágenes utilizando la API de Pixabay.

Los usuarios pueden ingresar un término de búsqueda, visualizar imágenes relacionadas y navegar entre diferentes páginas de resultados.

Este proyecto forma parte de mi aprendizaje de JavaScript y está enfocado en la práctica del consumo de APIs externas, manipulación dinámica del DOM y uso de generadores para implementar paginación.

## 🚀 Demo

🔗 [Ver aplicación en GitHub Pages](https://cristhianychr.github.io/buscador-imagenes-pixabay-js/)

> La búsqueda requiere una clave válida de Pixabay.

## 📸 Vista previa

![Vista previa del Buscador de Recetas](./img/preview.png)

## ✨ Funcionalidades

- **Buscar imágenes:** permite realizar búsquedas mediante palabras clave.
- **Validar búsqueda:** comprueba que el usuario haya ingresado un término antes de realizar la consulta.
- **Mostrar resultados dinámicos:** presenta las imágenes obtenidas desde Pixabay.
- **Visualizar estadísticas:** muestra la cantidad de likes y visualizaciones de cada imagen.
- **Ver imagen original:** permite abrir la imagen en su tamaño disponible mediante un enlace externo.
- **Paginación dinámica:** genera los botones de navegación según la cantidad de resultados disponibles.
- **Resultados por página:** muestra hasta 40 imágenes por consulta.
- **Actualización de resultados:** permite cambiar de página sin recargar el documento.
- **Mensajes de validación:** muestra alertas cuando el usuario intenta realizar una búsqueda sin ingresar un término.

## 🛠️ Tecnologías utilizadas

- **HTML5:** estructura de la aplicación y formulario de búsqueda.
- **CSS3:** estilos personalizados.
- **Tailwind CSS:** diseño de la interfaz mediante clases utilitarias.
- **JavaScript (ES6+):** lógica de la aplicación y manipulación del DOM.
- **Fetch API:** comunicación con servicios externos.
- **Pixabay API:** obtención de imágenes y estadísticas.
- **Git y GitHub:** control de versiones y publicación del proyecto.

## 🧠 Conceptos de JavaScript aplicados

- Manipulación del DOM con `querySelector`, `createElement` y `appendChild`.
- Gestión de eventos con `addEventListener` y `onclick`.
- Prevención del comportamiento predeterminado con `preventDefault()`.
- Consumo de APIs externas mediante `fetch()`.
- Programación asíncrona con promesas y `.then()`.
- Procesamiento de respuestas JSON.
- Desestructuración de objetos.
- Funciones flecha.
- Template literals.
- Métodos de arreglos como `forEach()`.
- Generadores mediante `function*` y `yield`.
- Iteración manual de generadores con `next()`.
- Manejo de atributos `data-*` en elementos HTML.
- Temporizadores con `setTimeout()`.
- Manipulación de clases CSS con `classList`.

## 🌐 API utilizada

El proyecto utiliza **Pixabay API**, un servicio que permite acceder a imágenes y otros recursos multimedia.

Se implementa el siguiente endpoint:

`https://pixabay.com/api/`

Los parámetros utilizados son:

| Parámetro | Descripción |
|---|---|
| `key` | Clave de autenticación de la API. |
| `q` | Término de búsqueda. |
| `per_page` | Cantidad de resultados por página (40). |
| `page` | Número de página solicitada. |

La respuesta proporciona información de las imágenes, incluyendo su URL de vista previa, imagen de mayor tamaño, likes y visualizaciones.

## 🔄 Paginación mediante generadores

Uno de los conceptos principales del proyecto es la implementación de un generador de JavaScript para construir dinámicamente la paginación.

```javascript
function* crearPaginador(total) {
    for (let i = 1; i <= total; i++) {
        yield i;
    }
}
```

El generador produce los números de página de manera secuencial mediante `yield`, permitiendo recorrerlos utilizando `next()` y crear los controles de navegación dinámicamente.

## 📂 Estructura del proyecto

```text
buscador-imagenes-pixabay-js/
├── css/
│   ├── custom.css
│   └── tailwind.min.css
├── img/
│   └── preview.png
├── js/
│   └── app.js
├── index.html
├── .gitignore
└── README.md
```

## ⚙️ Instalación y ejecución

1. Clona el repositorio:

   ```bash
   git clone https://github.com/cristhianychr/buscador-imagenes-pixabay-js.git
   ```

2. Accede a la carpeta:

   ```bash
   cd buscador-imagenes-pixabay-js
   ```

3. Configura una clave válida de Pixabay en `js/app.js`:

   ```javascript
   const key = 'YOUR_API_KEY';
   ```

4. Abre `index.html` en tu navegador.

No es necesario instalar dependencias adicionales ni configurar un servidor backend.

> Para publicar una versión funcional sin exponer la clave de API, se recomienda implementar un backend intermediario.

## 📌 Aprendizajes

Este proyecto me permitió reforzar el consumo de APIs externas mediante Fetch API y el procesamiento de respuestas JSON.

También profundicé en el uso de generadores de JavaScript para controlar la iteración y construir una paginación dinámica, además de practicar la manipulación del DOM y la actualización de resultados sin recargar la página.

## 👨‍💻 Autor

Proyecto desarrollado como parte de mi formación práctica en JavaScript y desarrollo web.

**Cristhian Chanamé**  
Estudiante de Ingeniería de Software.