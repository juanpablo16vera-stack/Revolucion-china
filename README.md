```html
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Museo Virtual - Revolución China</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family: Georgia, "Times New Roman", serif;
    background:#171411;
    color:#eee;
    overflow-x:hidden;
}

/* =========================
   MENÚ
========================= */

nav{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:65px;
    background:rgba(15,12,10,.94);
    border-bottom:1px solid #6f5b42;
    display:flex;
    align-items:center;
    justify-content:center;
    gap:35px;
    z-index:1000;
}

nav a{
    color:#ddd;
    text-decoration:none;
    font-size:15px;
    transition:.3s;
}

nav a:hover{
    color:#d9a441;
}

/* =========================
   PORTADA
========================= */

.portada{
    height:100vh;
    min-height:650px;

    background:
        linear-gradient(rgba(0,0,0,.65),rgba(0,0,0,.82)),
        url("https://images.unsplash.com/photo-1547981609-4b6bfe67ca0b?auto=format&fit=crop&w=2000&q=80");

    background-size:cover;
    background-position:center;

    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:30px;
}

.portada-contenido{
    max-width:900px;
}

.pequeno{
    color:#d9a441;
    letter-spacing:5px;
    font-size:14px;
    margin-bottom:25px;
}

.portada h1{
    font-size:64px;
    line-height:1.05;
    margin-bottom:20px;
}

.portada h2{
    font-size:28px;
    font-weight:normal;
    color:#ddd;
    margin-bottom:40px;
}

.entrar{
    display:inline-block;
    padding:15px 35px;
    border:1px solid #d9a441;
    color:#fff;
    text-decoration:none;
    transition:.3s;
}

.entrar:hover{
    background:#d9a441;
    color:#171411;
}

/* =========================
   SECCIONES
========================= */

.sala{
    min-height:100vh;
    padding:120px 8% 100px;
    position:relative;
}

.sala:nth-child(even){
    background:#211c17;
}

.contenedor{
    max-width:1150px;
    margin:auto;
}

.titulo-sala{
    text-align:center;
    margin-bottom:60px;
}

.numero{
    color:#d9a441;
    font-size:14px;
    letter-spacing:4px;
}

.titulo-sala h2{
    font-size:45px;
    margin-top:10px;
}

.linea{
    width:80px;
    height:2px;
    background:#d9a441;
    margin:20px auto;
}

/* =========================
   CUADROS
========================= */

.exposicion{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:50px;
    align-items:center;
}

.cuadro{
    background:#0e0d0c;
    padding:15px;
    border:1px solid #675640;
    box-shadow:0 20px 50px rgba(0,0,0,.4);
}

.cuadro img{
    width:100%;
    height:480px;
    object-fit:cover;
    display:block;
}

.descripcion{
    padding:10px;
}

.descripcion h3{
    font-size:30px;
    margin-bottom:20px;
}

.descripcion p{
    font-family:Arial,sans-serif;
    color:#ccc;
    line-height:1.8;
    font-size:17px;
}

/* =========================
   PROPAGANDA VS REALIDAD
========================= */

.comparacion{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:30px;
}

.panel{
    padding:40px;
    background:#171411;
    border:1px solid #514333;
}

.panel h3{
    color:#d9a441;
    font-size:28px;
    margin-bottom:20px;
}

.panel p{
    font-family:Arial,sans-serif;
    color:#ccc;
    line-height:1.8;
}

/* =========================
   OBJETO
========================= */

.objeto{
    max-width:700px;
    margin:auto;
    text-align:center;
}

.objeto-marco{
    background:#0d0c0b;
    padding:25px;
    border:1px solid #705d43;
    box-shadow:0 20px 50px rgba(0,0,0,.5);
}

.objeto img{
    width:100%;
    height:400px;
    object-fit:cover;
}

.objeto h3{
    font-size:35px;
    margin:25px 0 15px;
}

.objeto p{
    font-family:Arial,sans-serif;
    color:#ccc;
    line-height:1.8;
}

/* =========================
   AUDIO
========================= */

.audio{
    max-width:750px;
    margin:auto;
    background:#0f0e0c;
    border:1px solid #62523d;
    padding:40px;
    text-align:center;
}

.audio-icon{
    font-size:50px;
    margin-bottom:20px;
}

.audio h3{
    font-size:30px;
    margin-bottom:20px;
}

.audio p{
    font-family:Arial,sans-serif;
    line-height:1.8;
    color:#ccc;
}

audio{
    width:100%;
    margin-top:30px;
}

/* =========================
   REFLEXIÓN
========================= */

.reflexion{
    min-height:70vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;

    background:
        linear-gradient(rgba(0,0,0,.7),rgba(0,0,0,.8)),
        url("https://images.unsplash.com/photo-1578321272176-b7bbc0679853?auto=format&fit=crop&w=2000&q=80");

    background-size:cover;
    background-position:center;
}

.reflexion-contenido{
    max-width:900px;
    padding:40px;
}

.reflexion h2{
    font-size:48px;
    margin-bottom:30px;
}

.reflexion p{
    font-size:27px;
    line-height:1.5;
    color:#eee;
}

/* =========================
   PIE
========================= */

footer{
    background:#0b0a09;
    text-align:center;
    padding:35px;
    color:#888;
    font-family:Arial,sans-serif;
}

footer strong{
    color:#d9a441;
}

/* =========================
   RESPONSIVE
========================= */

@media(max-width:800px){

    nav{
        gap:12px;
        height:55px;
    }

    nav a{
        font-size:11px;
    }

    .portada h1{
        font-size:42px;
    }

    .portada h2{
        font-size:21px;
    }

    .exposicion,
    .comparacion{
        grid-template-columns:1fr;
    }

    .titulo-sala h2{
        font-size:34px;
    }

    .cuadro img{
        height:350px;
    }

}

</style>
</head>

<body>

<!-- =========================
     MENÚ DEL MUSEO
========================= -->

<nav>

<a href="#inicio">Entrada</a>
<a href="#propaganda">Propaganda</a>
<a href="#realidad">Realidad</a>
<a href="#objeto">Objeto</a>
<a href="#audio">Audioguía</a>
<a href="#final">Reflexión</a>

</nav>


<!-- =========================
     ENTRADA
========================= -->

<header class="portada" id="inicio">

<div class="portada-contenido">

<div class="pequeno">
MUSEO VIRTUAL
</div>

<h1>
Revolución China
</h1>

<h2>
El pueblo trabajador
</h2>

<p style="color:#aaa; font-family:Arial;">
Grupo 5 · Propaganda, poder y vida cotidiana
</p>

<a class="entrar" href="#propaganda">
ENTRAR A LA SALA
</a>

</div>

</header>


<!-- =========================
     SALA 1
========================= -->

<section class="sala" id="propaganda">

<div class="contenedor">

<div class="titulo-sala">

<div class="numero">
SALA 01
</div>

<h2>
El pueblo trabajador
</h2>

<div class="linea"></div>

</div>


<div class="exposicion">

<div class="cuadro">

<img
src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Long_Live_the_Great_Unity_of_the_People_of_the_World.jpg/800px-Long_Live_the_Great_Uni
```
