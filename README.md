
<h1>Amigo Secreto</h1>

"Amigo Secreto" es una aplicación web simple e interactiva que permite organizar un sorteo para asignar amigos secretos entre un grupo de participantes. Esta herramienta es ideal para eventos sociales, como intercambios de regalos en celebraciones.

## Funcionalidades

1. **Agregar Nombres**: Permite a los usuarios ingresar los nombres de los participantes en el sorteo.
2. **Visualizar Lista de Participantes**: Muestra la lista actualizada de nombres ingresados.
3. **Sortear Amigo Secreto**: Realiza el sorteo de forma aleatoria y muestra el nombre del participante seleccionado.

## Estructura del Proyecto

El proyecto consta de tres archivos principales:
- `index.html`: Contiene el diseño de la estructura básica del sitio web.
- `style.css`: Define el estilo visual y los elementos gráficos del sitio.
- `app.js`: Implementa la lógica del programa en JavaScript.

## Requisitos Técnicos

- Navegador web moderno que soporte HTML5, CSS3 y JavaScript.
- Acceso a una conexión a internet para cargar las fuentes de Google Fonts utilizadas en el diseño.

## Cómo Utilizar el Proyecto

1. **Agregar Participantes**:
   - Escriba un nombre en el campo de entrada que dice "Escribe un nombre".
   - Presione el botón `Añadir` para incluirlo en la lista de participantes.

2. **Visualizar la Lista**:
   - Los nombres ingresados aparecerán listados automáticamente bajo la sección "Digite el nombre de sus amigos".

3. **Realizar el Sorteo**:
   - Cuando todos los nombres hayan sido ingresados, haga clic en el botón `Sortear amigo`.
   - El sistema seleccionará aleatoriamente a un amigo secreto y mostrará su nombre.

## Código Destacado

### Agregar Amigos
```javascript
function agregarAmigos() {
    const inputAmigo = document.getElementById("amigo");
    const nombreAmigo = inputAmigo.value.trim();

    if (nombreAmigo === "") {
        alert("Por favor, inserte un nombre valido");
        return;
    }

    amigos.push(nombreAmigo);
    actualizarLista();
    inputAmigo.value = "";
    inputAmigo.focus();
}
```
### Realizar el Sorteo
```javascript
function sortearAmigo() {
    if (amigos.length === 0) {
        alert("No hay amigos para sortear. Primero agrega nombres de amigos.");
        return;
    }

    const indiceAleatorio = Math.floor(Math.random() * amigos.length);
    const amigoSorteado = amigos[indiceAleatorio];
    const resultadoUl = document.getElementById("resultado");
    resultadoUl.innerHTML = `<li>${amigoSorteado}</li>`;
}
```
## Problemas Comunes y Soluciones
### No se muestran los nombres en la lista:

Asegúrese de que el campo de entrada no esté vacío antes de presionar el botón Añadir.

Verifique la conexión entre el archivo app.js y el HTML.

### El sorteo no funciona:

Confirme que hay al menos un nombre en la lista de amigos antes de realizar el sorteo.
