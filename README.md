# Programacion_web
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Granja Porcícola El Olivo</title>

  <!-- Fuente elegante desde Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap" rel="stylesheet" />

  <style>
    /* Tipografía elegante */
    body {
      font-family: 'Playfair Display', serif;
      margin: 0;
      padding: 0;
      background: #f5f5dc; 
      color: #3b3a30; 
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 40px;
      background: #556b2f; 
      color: #f0e68c; 
      box-shadow: 0 4px 8px rgba(85, 107, 47, 0.5);
    }

    header h1 {
      margin: 0;
      font-size: 2.8rem;
      font-weight: 700;
      letter-spacing: 2px;
      text-shadow: 1px 1px 2px #3b3a30;
    }

    header p {
      margin: 0;
      font-size: 1.2rem;
      font-style: italic;
      color: #d4af37; 
      text-shadow: 1px 1px 1px #3b3a30;
    }

    nav {
      background: #6b8e23; 
      display: flex;
      justify-content: center;
      padding: 12px 0;
      box-shadow: inset 0 -3px 5px rgba(212, 175, 55, 0.3);
    }

    nav a {
      color: #f0e68c; 
      text-decoration: none;
      margin: 0 20px;
      font-weight: 600;
      font-size: 1.1rem;
      transition: color 0.3s ease;
      letter-spacing: 1px;
    }

    nav a:hover {
      color: #d4af37; 
      text-shadow: 0 0 5px #d4af37;
    }

    section {
      padding: 50px 40px;
      max-width: 900px;
      margin: auto;
      background: #faf9f0; 
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(85, 107, 47, 0.15);
      margin-bottom: 40px;
    }

    h2 {
      color: #556b2f; 
      border-bottom: 3px solid #d4af37; 
      padding-bottom: 12px;
      font-size: 2rem;
      margin-bottom: 25px;
      letter-spacing: 1.5px;
    }

    ul {
      list-style-type: square;
      padding-left: 20px;
      font-size: 1.2rem;
      color: #4b5320; 
    }

    footer {
      background: #556b2f;
      color: #f0e68c;
      text-align: center;
      padding: 20px;
      font-size: 1rem;
      letter-spacing: 1px;
      box-shadow: inset 0 3px 5px rgba(212, 175, 55, 0.3);
    }

    /* Botones */
    .btn {
      display: inline-block;
      background: #d4af37; 
      color: #3b3a30; 
      padding: 12px 28px;
      margin-top: 20px;
      text-decoration: none;
      border-radius: 30px;
      font-weight: 700;
      font-size: 1.1rem;
      box-shadow: 0 4px 8px rgba(212, 175, 55, 0.6);
      transition: background 0.3s ease, color 0.3s ease;
      cursor: pointer;
      border: none;
      font-family: 'Playfair Display', serif;
    }

    .btn:hover {
      background: #b8860b; 
      color: #faf9f0;
      box-shadow: 0 6px 12px rgba(184, 134, 11, 0.8);
    }

    /* Botón registro */
    header .btn {
      background: #d4af37;
      color: #3b3a30;
      margin-top: 0;
      height: fit-content;
      font-weight: 700;
      border-radius: 30px;
      padding: 10px 25px;
      box-shadow: 0 4px 8px rgba(212, 175, 55, 0.8);
      text-shadow: none;
    }

    header .btn:hover {
      background: #b8860b;
      color: #faf9f0;
      box-shadow: 0 6px 12px rgba(184, 134, 11, 1);
    }

    /* Formularios */
    form {
      max-width: 400px;
      margin: 20px auto 0;
      background: #faf9f0;
      padding: 25px 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(85, 107, 47, 0.2);
      font-size: 1.1rem;
      color: #3b3a30;
    }

    form label {
      display: block;
      margin-bottom: 8px;
      font-weight: 700;
      color: #556b2f;
      letter-spacing: 0.5px;
    }

    form input {
      width: 100%;
      padding: 10px 12px;
      margin-bottom: 20px;
      border: 2px solid #6b8e23;
      border-radius: 8px;
      font-size: 1rem;
      font-family: 'Playfair Display', serif;
      transition: border-color 0.3s ease;
    }

    form input:focus {
      border-color: #d4af37;
      outline: none;
      box-shadow: 0 0 8px #d4af37;
    }

    form input[type="submit"] {
      background: #556b2f;
      color: #faf9f0;
      border: none;
      cursor: pointer;
      font-weight: 700;
      font-size: 1.1rem;
      transition: background 0.3s ease;
      box-shadow: 0 4px 8px rgba(85, 107, 47, 0.7);
    }

    form input[type="submit"]:hover {
      background: #6b8e23;
      box-shadow: 0 6px 12px rgba(107, 142, 35, 0.9);
    }

    .success-message {
      text-align: center;
      color: #556b2f;
      font-weight: 700;
      margin-top: 15px;
      font-size: 1.1rem;
    }
  </style>
</head>
<body>

  <!-- Encabezado con botón Registro -->
  <header>
    <div>
      <h1>Granja Porcícola El Olivo</h1>
      <p>Calidad y confianza, bajo la sombra del olivo.</p>
    </div>
    <a href="#registro" class="btn">Registro</a>
  </header>

  <!-- Menú de navegación -->
  <nav>
    <a href="#nosotros">Nosotros</a>
    <a href="#productos">Productos</a>
    <a href="#contacto">Contacto</a>
  </nav>

  <!-- Sección Nosotros -->
  <section id="nosotros">
    <h2>Sobre Nosotros</h2>
    <p>
      En la Granja Porcícola El Olivo nos dedicamos a la crianza responsable de cerdos, 
      garantizando productos de alta calidad para nuestros clientes. 
      Nuestro compromiso está en la innovación, el bienestar animal y el respeto por el medio ambiente.
    </p>
  </section>

  <!-- Sección Productos -->
  <section id="productos">
    <h2>Nuestros Productos</h2>
    <ul>
      <li>Asesorías</li>
      <li>Cerdas de cría</li>
      <li>Venta de semen</li>
    </ul>
    <a href="#contacto" class="btn">Solicita más información</a>
  </section>

  <!-- Sección Registro de Usuario -->
  <section id="registro">
    <h2>Crear Usuario</h2>
    <form id="registroForm">
      <label for="usuario">Nombre de usuario:</label>
      <input type="text" id="usuario" name="usuario" required />

      <label for="password">Contraseña:</label>
      <input type="password" id="password" name="password" required />

      <input type="submit" value="Registrar" />
    </form>
    <p id="mensajeRegistro" class="success-message" style="display:none;">¡Registro exitoso!</p>
  </section>

  <!-- Sección Contacto -->
  <section id="contacto">
    <h2>Contacto</h2>
    <p>📍 Dirección: Vereda Sartenejal, Guadalupe, Huila</p>
    <p>📞 Teléfono: 3104746472</p>
    <p>📧 Email: porcicolaelolivo@gmail.com</p>
  </section>

  <!-- Pie de página -->
  <footer>
    <p>&copy; 2025 Granja Porcícola El Olivo | Todos los derechos reservados</p>
  </footer>

  <script>
    const form = document.getElementById('registroForm');
    const mensaje = document.getElementById('mensajeRegistro');

    form.addEventListener('submit', function(event) {
      event.preventDefault();

      

      form.reset();
      mensaje.style.display = 'block';

      setTimeout(() => {
        mensaje.style.display = 'none';
      }, 3000);
    });
  </script>

</body>
</html>