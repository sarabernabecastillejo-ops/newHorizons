# newHorizons
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
   
  </div>
  <script src="script.js"></script>
