# Proyecto Rick and Morty

Este es un proyecto sencillo que consume la **API de Rick and Morty** y muestra los personajes en formato de cartas con estilos personalizados.

## 🚀 Tecnologías utilizadas

* **HTML5**
* **CSS3**
* **JavaScript** (Fetch API)
* **Rick and Morty API**: [https://rickandmortyapi.com/](https://rickandmortyapi.com/)

---

## 📁 Estructura del proyecto

```
📂 proyecto-rick-and-morty
 ┣ 📂 assets
 ┃ ┗ 📂 img
 ┣ 📄 index.html
 ┣ 📄 styles.css
 ┣ 📄 app.js
 ┗ 📄 README.md
```

## 📌 Funcionalidades

* Consumo de API externa.
* Renderizado dinámico de personajes.
* Diseño visual basado en la estética de Rick and Morty.
* Hover animations en tarjetas.

---

## 📜 Código principal para consumir la API

```js
function getCharacters(done) {
    fetch('https://rickandmortyapi.com/api/character')
        .then(response => response.json())
        .then(data => done(data));
}

getCharacters(data => {
    data.results.forEach(personaje => {
        const article = document.createRange().createContextualFragment(`
            <article class="card">
                <div class="image-container">
                    <img src="${personaje.image}" alt="${personaje.name}">
                </div>
                <h2>${personaje.name}</h2>
                <span>${personaje.status}</span>
            </article>
        `);

        const main = document.querySelector('main');
        main.append(article);
    });
});
```

---

## 🎨 Estilos recomendados (ejemplo)

```css
header h1 {
    text-align: center;
    font-size: 3rem;
    font-weight: 900;
    padding: 20px;
    background: linear-gradient(90deg, #00d0ff, #00ff88);
    border-radius: 15px;
    color: #0a0a0a;
    text-shadow: 0 0 10px #fff;
    box-shadow: 0 0 20px #00ffcc;
}

## 📄 Licencia

Este proyecto es de uso libre para prácticas educativas.

---

¡Disfruta creando tu proyecto inspirado en **Rick and Morty**! 💚🛸


## 👨‍💻 Autor
Danius E. Fuentes Solano
