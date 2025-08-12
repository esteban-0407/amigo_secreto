# 🎁 Amigo Secreto

Este es un proyecto simple en JavaScript que permite:
- Ingresar una lista de nombres de amigos.
- Mostrar la lista en la página.
- Sortear aleatoriamente un amigo secreto.

## 📂 Estructura del proyecto

- index.html # Página principal
- style.css # Estilos del proyecto
- app.js # Lógica en JavaScript
- assets/ # Imágenes e íconos

## 🚀 Características

- **Agregar amigos**: Los nombres ingresados se almacenan en un arreglo `amigos`.
- **Mostrar lista**: Los amigos se muestran en un `<ul>` de forma dinámica.
- **Sortear amigo secreto**: Selecciona aleatoriamente un nombre de la lista usando `Math.random()`.

## 🛠️ Tecnologías usadas

- **HTML5**
- **CSS3**
- **JavaScript**

## 📋 Uso

1. Abre el archivo `index.html` en tu navegador.
2. Escribe el nombre de un amigo en el campo de texto y haz clic en **"Añadir"**.
3. Repite el paso anterior para agregar más nombres.
4. Haz clic en **"Sortear amigo"** para seleccionar un nombre al azar.


## 📜 Código principal

Ejemplo de función para agregar amigos:

```javascript
let amigos = [];

function agregarAmigo() {
    let input = document.getElementById("amigo");
    let nombre = input.value.trim();

    if (nombre === "") {
        alert("Por favor, escribe un nombre válido.");
        return;
    }

    amigos.push(nombre);
    mostrarLista();
    input.value = "";
}
