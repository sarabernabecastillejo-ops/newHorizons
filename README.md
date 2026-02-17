# newHorizons
 <!DOCTYPE html>
<html>

<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>SPA app</title>

  <style>
    /* style.css */
body {
  font-family:
Georgia, 'Times New Roman', Times, serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f0;
}
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
header {
  background-color: #5ab1a5;
  color: beige;
  text-align: center;
  padding: 1em;
}
nav {
  background-color: #4b968c;
}
nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
}
nav li {
  margin: 0;
}
nav a {
  text-decoration: none;
  color: #fff;
  padding: 1em;
  display: block;
  transition: background-color 0.3s ease;
}
nav a:hover {
  background-color: #0f002c;
}
main {
  flex: 1;
  padding: 1em;
}
#content {
  max-width: 1000px;
  margin: 0 auto;
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow:
0 0 10px rgba(0, 0, 0, 0.1);
}
#content h2 {
  color: #2f8d46;
}
#content img {
  width: 400px;
  height: auto;
  margin: 0 auto;
  display: block;
  border-radius: 10px;
  box-shadow:
2px 2px 5px rgba(0, 0, 0, 0.2);
  border: 3px solid #2F8D46;
}
form {
  max-width: 400px;
  margin: 20px auto;
  padding: 20px;
  background-color: #f0f0f0;
  border-radius: 8px;
  box-shadow:
0 0 10px rgba(0, 0, 0, 0.1);
}
form label {
  display: block;
  margin-bottom: 8px;
}
form input,
form textarea {
  width: 100%;
  padding: 8px;
  margin-bottom: 16px;
  box-sizing: border-box;
  border: 1px solid #ccc;
  border-radius: 4px;
}
form button {
  background-color: #4caf50;
  color: #fff;
  padding: 10px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition:
background-color 0.3s ease;
}
form button:hover {
  background-color: #45a049;
}


  </style>

  
</head>
<body>
  <link rel="stylesheet" href="style.css">

  <div id="app">
    <header>
      <h1>
       NEW HORIZONS
      </h1>
      <h2>
       Nous viatges per descobrir i a bon preu!!!!
      </h2>
    </header>
    <nav>
      <ul>
        <li>
          <a href="#" onclick=
          "changeContent('home')">
            Inici
          </a>
        </li>
        <li>
          <a href="#" onclick=
          "changeContent('about')">
            Sobre
          </a>
        </li>
        <li>
          <a href="#" onclick=
          "changeContent('contact')">
            Contacto
          </a>
        </li>
      </ul>
    </nav>
    <main>
      <div id="content">
        <img src=
"https://www.vipealo.com/blog/wp-content/uploads/2022/02/AdobeStock_83358985-1.jpeg">
        <h3>Les vacances del teu somni AQUI!</h3>
        <p>
          En aquest enllaç aniras a una altre WEB per consular els preus de les habitacions i els llocs on vols anar.
        </p>
        <p>
          Visita la pàgina WEB per consultar els preus
          <a href="https://www.tripadvisor.es/" target="_blank">
            aquí
          </a>.
        </p>
      </div>
    </main>
  </div>
  <script src="script.js"></script>

  <script>
    function changeContent(page) {
  var contentDiv = document.getElementById('content');
  switch (page) {
    case 'home':
      contentDiv.innerHTML = `
        <img src=
"https://www.vipealo.com/blog/wp-content/uploads/2022/02/AdobeStock_83358985-1.jpeg">
        <h2>
          Benvingut a la pàgina principal!
        </h2>
        <p>
          Aquesta és la pàgina principal.
        </p>
        <p>
          Explora les diferent seccions fent servir
          el menu.
        </p>
      `;
      break;
    case 'about':
      contentDiv.innerHTML = `
        <h2>Sobre </h2>
        <p>
          One life. One world. Explore it. Una vida  un món. Explora'l.
        </p>
        <p>
          La nostra intenció és donar-te unes vacances que mai no puguis oblidar
        </p>
      `;
      break;
    case 'contact':
      contentDiv.innerHTML =
        `<h2>Contacte</h2>
        <p>
          Escriu-nos si tens dubtes !
        </p>
        <form>
        <label for="name">Name:</label>
        <input type="text" id="name" name="name"
            placeholder="Your Name" required>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email"
            placeholder="Your Email" required>
        <label for="message">Message:</label>
        <textarea id="message" name="message"
              placeholder="Your Message"
              rows="4" required>
          </textarea>
        <button type="submit">Send Message</button>
        </form>`;
      break;


    default:
      contentDiv.innerHTML = '<h2>Page not found!</h2>';
  }
}

  </script>
</body>
</html>
