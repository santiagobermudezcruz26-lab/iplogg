

<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Buzón de Sugerencias | I.E Carlos Ramírez París</title>

<style>
body{
  margin:0;
  font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background:linear-gradient(135deg,#0a3d62,#1e90ff);
  min-height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
}

.container{
  background:white;
  width:100%;
  max-width:520px;
  padding:30px;
  border-radius:18px;
  box-shadow:0 12px 35px rgba(0,0,0,0.3);
}

h1{
  text-align:center;
  margin-bottom:10px;
}

p{
  text-align:center;
  color:#444;
  font-size:14px;
  margin-bottom:25px;
}

button{
  width:100%;
  background:#1e90ff;
  color:white;
  border:none;
  padding:15px;
  border-radius:10px;
  font-size:18px;
  cursor:pointer;
  transition:background 0.3s;
}

button:hover{
  background:#0a3d62;
}

.hidden{display:none;}

label{
  font-weight:600;
  display:block;
  margin-bottom:6px;
}

select, textarea{
  width:100%;
  padding:12px;
  margin-bottom:18px;
  border-radius:10px;
  border:1px solid #ccc;
  font-size:16px;
}

textarea{
  resize:none;
  height:120px;
}

/* SEMÁFORO */
.colors{
  display:flex;
  justify-content:space-around;
  margin-bottom:22px;
}

.color-option{
  display:flex;
  flex-direction:column;
  align-items:center;
  cursor:pointer;
}

.circle{
  width:28px;
  height:28px;
  border-radius:50%;
  border:2px solid #555;
  margin-bottom:6px;
  transition:transform 0.2s, box-shadow 0.2s;
}

.green{background:#2ecc71;}
.yellow{background:#f1c40f;}
.red{background:#e74c3c;}

input[type="radio"]{display:none;}

input[type="radio"]:checked + .circle{
  box-shadow:0 0 0 4px rgba(30,144,255,0.4);
  transform:scale(1.15);
}

.footer{
  text-align:center;
  font-size:12px;
  color:#777;
  margin-top:18px;
}
</style>
</head>

<body>

<div class="container">

<div id="inicio">
  <h1>📩 Buzón de sugerencias<br>Contraloría 2026</h1>
  <p>
    Hola querido estudiante 😁<br>
    Haz clic en continuar para enviar tu sugerencia.
  </p>
  <button onclick="mostrarFormulario()">Continuar</button>
</div>

<div id="formulario" class="hidden">
<form action="https://formsubmit.co/contralorsantiago2026@gmail.com" method="POST">

<input type="hidden" name="_captcha" value="false">
<input type="hidden" name="_subject" value="Nueva sugerencia - Contraloría 2026">
<input type="hidden" name="_template" value="table">

<label>Grado</label>
<select name="Grado" required>
  <option value="">Selecciona tu grado</option>
  <option>Sexto</option>
  <option>Séptimo</option>
  <option>Octavo</option>
  <option>Noveno</option>
  <option>Décimo</option>
  <option>Once</option>
</select>

<label>Tipo de mensaje</label>
<div class="colors">
  <label class="color-option">
    <input type="radio" name="Nivel" value="Cosas buenas" required>
    <span class="circle green"></span>
    <span>Bueno</span>
  </label>

  <label class="color-option">
    <input type="radio" name="Nivel" value="Puede mejorar">
    <span class="circle yellow"></span>
    <span>Mejorar</span>
  </label>

  <label class="color-option">
    <input type="radio" name="Nivel" value="Situación delicada">
    <span class="circle red"></span>
    <span>Delicado</span>
  </label>
</div>

<label>Motivo</label>
<select name="Motivo" required>
  <option value="">Selecciona una opción</option>
  <option>Bullying</option>
  <option>Comedor</option>
  <option>Convivencia</option>
  <option>Ideas o mejoras</option>
</select>

<label>Mensaje</label>
<textarea name="Mensaje" placeholder="Escribe aquí tu mensaje..." required></textarea>

<button type="submit">Enviar sugerencia</button>
</form>
</div>

<div class="footer">
  I.E. Carlos Ramírez París – Cúcuta, Colombia © 2026
</div>

</div>

<script>
function mostrarFormulario(){
  document.getElementById("inicio").classList.add("hidden");
  document.getElementById("formulario").classList.remove("hidden");
}
</script>

</body>
</html>
