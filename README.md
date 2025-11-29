<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>IronGym — Premium Fitness Experience</title>

  <style>
    body{margin:0;font-family:'Inter',sans-serif;background:#0b0b12;color:white;overflow-x:hidden}

    /* HERO */
    .hero{background:url('https://images.unsplash.com/photo-1517836357463-d25dfeac3438') center/cover no-repeat;height:55vh;display:flex;align-items:center;justify-content:center;text-shadow:0 4px 20px rgba(0,0,0,0.8)}
    .hero h1{font-size:50px;font-weight:900}

    .section{padding:40px 20px;max-width:1100px;margin:auto}
    .section h2{text-align:center;font-size:32px;margin-bottom:20px;font-weight:800}

    /* MERCH GRID */
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:20px}
    .item{background:rgba(255,255,255,0.08);border-radius:16px;overflow:hidden;backdrop-filter:blur(10px);box-shadow:0 8px 30px rgba(0,0,0,0.3)}
    .item img{width:100%;height:180px;object-fit:cover}
    .item-info{padding:14px;text-align:center}
    .price{color:#84f3c0;font-size:18px;font-weight:700}

    /* INSTALLATIONS */
    .install-img{width:100%;border-radius:18px;box-shadow:0 8px 30px rgba(0,0,0,0.4);margin-bottom:20px}

    /* VIDEO */
    video{width:100%;border-radius:18px;box-shadow:0 8px 30px rgba(0,0,0,0.4)}

    /* FORM */
    .card{background:rgba(255,255,255,0.08);backdrop-filter:blur(14px);padding:26px;border-radius:20px;width:90%;max-width:500px;margin:40px auto;box-shadow:0 8px 30px rgba(0,0,0,0.45)}
    input{width:100%;padding:14px;margin-top:6px;border-radius:12px;border:0;font-size:16px;background:rgba(255,255,255,0.12);color:white}
    button{width:100%;padding:16px;margin-top:22px;border:0;border-radius:14px;background:#e11d48;color:white;font-weight:700;font-size:18px;cursor:pointer;transition:0.2s}
    button:hover{transform:scale(1.03);background:#f22058}
    #msg{text-align:center;margin-top:14px;color:#84f3c0;font-weight:600}
  </style>
</head>
<body>

  <!-- HERO -->
  <section class="hero"><h1>IronGym</h1></section>

  <!-- INSTALLATIONS -->
  <section class="section">
    <h2>Instalaciones</h2>
    <img class="install-img" src="https://images.unsplash.com/photo-1518611012118-696072aa579a" />
    <img class="install-img" src="https://images.unsplash.com/photo-1554284126-aa88f22d8b74" />
    <img class="install-img" src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b" />
  </section>

  

  <!-- FORM -->
  <div class="card">
    <h2>Regístrate</h2>
    <label>Correo</label>
    <input id="email" type="email" placeholder="tucorreo@ejemplo.com" />

    <label>Teléfono</label>
    <input id="phone" type="tel" placeholder="600 000 000" />

    <button onclick="guardar()">Guardar registro</button>
    <div id="msg"></div>
  </div>

  <script>
    function guardar(){
      const email=document.getElementById('email').value.trim();
      const phone=document.getElementById('phone').value.trim();
      if(!email||!phone){msg.textContent='Rellena todo';return;}
      localStorage.setItem('irongym_user',JSON.stringify({email,phone}));
      msg.textContent='✔ Registro guardado correctamente';
    }
  </script>

  

</body>
</html>
