# Programacion_web


<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Granja Porcícola El Olivo: Crianza responsable de cerdos con productos de alta calidad." />
  <title>Granja Porcícola El Olivo</title>
  <!-- Fuente elegante -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap" rel="stylesheet" />
  <!-- Favicon -->
  <link rel="icon" href="logo-cerdo.png" type="image/png" />
  <style>
    :root {
      --olive-dark: #556b2f;
      --olive-medium: #6b8e23;
      --gold: #d4af37;
      --gold-dark: #b8860b;
      --beige: #f5f5dc;
      --beige-light: #faf9f0;
      --text-dark: #3b3a30;
      --text-light: #f0e68c;
    }

    /* Reset y base */
    * {
      box-sizing: border-box;
    }

    body {
      font-family: 'Playfair Display', serif;
      margin: 0;
      padding: 0;
      background: var(--beige);
      color: var(--text-dark);
      line-height: 1.6;
    }

    /* HEADER */
    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 20px 40px;
      background: linear-gradient(135deg, var(--olive-dark) 0%, var(--olive-medium) 100%);
      box-shadow: 0 4px 15px rgba(85, 107, 47, 0.7);
    }

    .logo-container {
      display: flex;
      align-items: center;
      gap: 20px;
    }

    .logo-container img {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      border: 3px solid var(--gold);
      box-shadow: 0 0 8px var(--gold);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      background: #f5f5dc;
    }

    .logo-container img:hover {
      transform: scale(1.1) rotate(5deg);
      box-shadow: 0 0 14px var(--gold);
      cursor: pointer;
    }

    .site-title {
      color: var(--text-light);
      text-shadow: 1.5px 1.5px 3px rgba(0,0,0,0.6);
    }

    .site-title h1 {
      margin: 0;
      font-size: 2.8rem;
      font-weight: 900;
      letter-spacing: 3px;
    }
    .site-title p {
      margin: 4px 0 0;
      font-style: italic;
      font-size: 1.3rem;
      color: var(--gold);
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.4);
      font-weight: 600;
    }

    header .btn {
      background: var(--gold);
      color: var(--text-dark);
      font-weight: 900;
      border-radius: 30px;
      padding: 12px 30px;
      box-shadow: 0 6px 12px rgba(212, 175, 55, 0.9);
      font-size: 1.15rem;
      text-shadow: none;
      transition: background 0.4s ease, color 0.4s ease;
      border: none;
      cursor: pointer;
      font-family: 'Playfair Display', serif;
      box-shadow: 0 4px 12px rgba(212, 175, 55, 0.9);
      user-select: none;
    }

    header .btn:hover {
      background: var(--gold-dark);
      color: var(--beige-light);
      box-shadow: 0 8px 20px rgba(184, 134, 11, 1);
    }

    /* NAV */
    nav {
      background: var(--olive-medium);
      display: flex;
      justify-content: center;
      padding: 16px 0;
      box-shadow: inset 0 -3px 7px rgba(212, 175, 55, 0.5);
      letter-spacing: 0.8px;
      font-weight: 600;
      font-size: 1.15rem;
    }

    nav a {
      color: var(--text-light);
      text-decoration: none;
      margin: 0 25px;
      letter-spacing: 1.2px;
      transition: color 0.4s ease, text-shadow 0.4s ease;
      padding: 3px 0;
      border-bottom: 2px solid transparent;
    }

    nav a:hover,
    nav a:focus {
      color: var(--gold);
      text-shadow: 0 0 6px var(--gold);
      border-bottom: 2px solid var(--gold);
      outline: none;
    }

    main {
      padding: 60px 40px;
      max-width: 960px;
      margin: auto;
      background: var(--beige-light);
      border-radius: 16px;
      box-shadow: 0 6px 20px rgba(85, 107, 47, 0.2);
      min-height: 75vh;
    }

    section {
      margin-bottom: 50px;
    }

    h2 {
      color: var(--olive-dark);
      border-bottom: 4px solid var(--gold);
      padding-bottom: 14px;
      font-size: 2.25rem;
      margin-bottom: 30px;
      letter-spacing: 2px;
      font-weight: 800;
      text-transform: uppercase;
      font-family: 'Playfair Display', serif;
    }

    p, ul {
      font-size: 1.25rem;
      color: #4b5320;
      line-height: 1.7;
    }
    ul {
      list-style-type: square;
      margin-left: 1.6rem;
    }

    .btn {
      display: inline-block;
      background: var(--gold);
      color: var(--text-dark);
      padding: 14px 34px;
      margin-top: 25px;
      text-decoration: none;
      border-radius: 40px;
      font-weight: 900;
      font-size: 1.2rem;
      box-shadow: 0 6px 14px rgba(212, 175, 55, 0.8);
      transition: background 0.3s ease, color 0.3s ease;
      cursor: pointer;
      border: none;
      font-family: 'Playfair Display', serif;
      user-select: none;
      letter-spacing: 1.2px;
    }

    .btn:hover {
      background: var(--gold-dark);
      color: var(--beige-light);
      box-shadow: 0 8px 18px rgba(184, 134, 11, 1);
    }

    form {
      max-width: 420px;
      margin: 25px auto 0;
      background: var(--beige);
      padding: 30px 35px;
      border-radius: 15px;
      box-shadow: 0 0 25px rgba(85, 107, 47, 0.25);
      font-size: 1.15rem;
      color: var(--text-dark);
      letter-spacing: 0.03em;
    }

    form label {
      display: block;
      margin-bottom: 10px;
      font-weight: 700;
      color: var(--olive-dark);
      letter-spacing: 0.6px;
    }

    form input {
      width: 100%;
      padding: 12px 18px;
      margin-bottom: 25px;
      border: 2px solid var(--olive-medium);
      border-radius: 10px;
      font-size: 1.05rem;
      font-family: 'Playfair Display', serif;
      transition: border-color 0.3s ease, box-shadow 0.3s ease;
    }

    form input:focus {
      border-color: var(--gold);
      outline: 2px solid var(--gold);
      box-shadow: 0 0 10px var(--gold);
      background-color: #fffef0;
    }

    form input[type="submit"] {
      background: var(--olive-dark);
      color: var(--beige-light);
      border: none;
      cursor: pointer;
      font-weight: 900;
      font-size: 1.2rem;
      transition: background 0.4s ease, box-shadow 0.4s ease;
      box-shadow: 0 6px 15px rgba(85, 107, 47, 0.8);
      user-select: none;
    }

    form input[type="submit"]:hover {
      background: var(--olive-medium);
      box-shadow: 0 9px 20px rgba(107, 142, 35, 1);
    }

    .success-message {
      text-align: center;
      color: var(--olive-dark);
      font-weight: 900;
      margin-top: 20px;
      font-size: 1.2rem;
      user-select: none;
      text-shadow: 1px 1px 2px #a1a242;
    }

    #contacto a {
      color: var(--olive-dark);
      font-weight: 700;
      text-decoration: none;
      transition: color 0.3s ease;
    }

    #contacto a:hover,
    #contacto a:focus {
      color: var(--gold);
      text-shadow: 0 0 6px var(--gold);
      outline: none;
    }

    footer {
      background: var(--olive-dark);
      color: var(--text-light);
      text-align: center;
      padding: 22px;
      font-size: 1.1rem;
      letter-spacing: 1.2px;
      box-shadow: inset 0 3px 7px rgba(212, 175, 55, 0.4);
      user-select: none;
      font-weight: 600;
    }

    @media (max-width: 768px) {
      header {
        flex-direction: column;
        gap: 15px;
        text-align: center;
        padding: 25px 20px;
      }
      nav {
        flex-direction: column;
        padding: 15px 0;
      }
      nav a {
        margin: 10px 0;
        font-size: 1.25rem;
      }
      main {
        padding: 40px 20px;
        max-width: 100%;
      }
      .logo-container img {
        width: 70px;
        height: 70px;
      }
      header .btn {
        padding: 12px 28px;
        font-size: 1.1rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="logo-container" aria-label="Logo Granja Porcícola El Olivo">
      <img src="logo-cerdo.png" alt="Logo Granja Porcícola El Olivo - cabeza de cerdo con estilo tradicional en tonos oliva y beige" />
      <div class="site-title">
        <h1>Granja Porcícola El Olivo</h1>
        <p>Calidad y confianza, bajo la sombra del olivo.</p>
      </div>
    </div>
    <a href="#registro" class="btn" aria-label="Ir a la sección de registro de usuario">Registro</a>
  </header>

  <nav>
    <a href="#nosotros" tabindex="0">Nosotros</a>
    <a href="#productos" tabindex="0">Productos</a>
    <a href="#contacto" tabindex="0">Contacto</a>
  </nav>

  <main>
    <section id="nosotros">
      <h2>Sobre Nosotros</h2>
      <p>
        En la Granja Porcícola El Olivo nos dedicamos a la crianza responsable de cerdos, 
        garantizando productos de alta calidad para nuestros clientes. 
        Nuestro compromiso está en la innovación, el bienestar animal y el respeto por el medio ambiente.
      </p>
    </section>

    <section id="productos">
      <h2>Nuestros Productos</h2>
      <ul>
        <li>Asesorías</li>
        <li>Cerdas de cría</li>
        <li>Venta de semen</li>
      </ul>
      <a href="#contacto" class="btn" aria-label="Solicitar más información en contacto">Solicita más información</a>
    </section>

    <section id="registro">
      <h2>Crear Usuario</h2>
      <form id="registroForm" aria-label="Formulario para crear usuario nuevo">
        <label for="usuario">Nombre de usuario:</label>
        <input type="text" id="usuario" name="usuario" required aria-required="true" />

        <label for="password">Contraseña:</label>
        <input type="password" id="password" name="password" required minlength="8" aria-required="true" />

        <input type="submit" value="Registrar" aria-label="Botón para registrar usuario" />
      </form>
      <p id="mensajeRegistro" class="success-message" role="alert" aria-live="polite" style="display:none;">¡Registro exitoso!</p>
    </section>

    <section id="contacto">
      <h2>Contacto</h2>
      <p>📍 Dirección: Vereda Sartenejal, Guadalupe, Huila</p>
      <p>📞 Teléfono: <a href="tel:3104746472">3104746472</a></p>
      <p>📧 Email: <a href="mailto:porcicolaelolivo@gmail.com">porcicolaelolivo@gmail.com</a></p>
      <p>🌍 <a href="https://www.google.com/maps/search/?api=1&query=Vereda+Sartenejal,+Guadalupe,+Huila,+Colombia" target="_blank" rel="noopener noreferrer">Ver en Google Maps</a></p>
    </section>
  </main>

  <footer>
    <p>&copy; 2024 Granja Porcícola El Olivo | Todos los derechos reservados</p>
  </footer>

  <script>
    // Scroll suave para todos los enlaces internos
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();

        const targetID = this.getAttribute('href').substring(1);
        const target = document.getElementById(targetID);
        if (target) {
          target.scrollIntoView({
            behavior: 'smooth',
            block: 'start'
          });
        }
      });
    });

    // Manejo registro formulario
    const form = document.getElementById('registroForm');
    const mensaje = document.getElementById('mensajeRegistro');

    form.addEventListener('submit', function(event) {
      event.preventDefault();

      const usuario = document.getElementById('usuario').value.trim();
      const password = document.getElementById('password').value;

      if (!usuario) {
        alert('Por favor, ingresa un nombre de usuario.');
        return;
      }

      if (password.length < 8) {
        alert('La contraseña debe tener al menos 8 caracteres.');
        return;
      }

      // Aquí podrías conectar con API real más adelante
      console.log('Usuario registrado:', usuario);

      form.reset();
      mensaje.style.display = 'block';

      setTimeout(() => {
        mensaje.style.display = 'none';
      }, 3000);
    });
  </script>
</body>
</html>