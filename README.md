let numeroSecreto =  0;
let intentos =  0;
let listaNumerosSorteados = [];

function asignarTextoElemento(elemento, texto) {
    let elementoHTML = document.querySelector (elemento);
    elementoHTML.innerHTML = texto;
    return;
}


// Función para manejar el clic del botón
function Verificarintento() {
    let numeroDeUsuario = parseInt(document.getElementById ('valorUsuario').value);
    console.log(numeroDeUsuario);
    console.log (numeroSecreto);
    console.log (intentos)

    if (numeroDeUsuario === numeroSecreto){
        asignarTextoElemento('p', `acertaste el numero en ${intentos} ${intentos=== 1 ? 'Intento' : "Intentos" }`);
        document.querySelector('#reiniciar').removeAttribute('disabled');
    } else {
        //el usuario no acerto
        if (numeroDeUsuario > numeroSecreto ){
            asignarTextoElemento('p','el numero secreto es menor');
        } else {
            asignarTextoElemento('p','el numero secreto es mayor')
        }
    }
    intentos ++;
    limpiarCaja();
    return;
}

function limpiarCaja() {
     document.querySelector('#valorUsuario').value = '';
    
}

//poner numericos

function generarNumeroSecreto() {
    let numeroGenerado = Math.floor(Math.random() * 10) + 1;
    // Si el número generado está incluido en la lista
    if (listaNumerosSorteados.includes(numeroGenerado)) {
        return generarNumeroSecreto();  // Vuelve a generar otro número
    } else {
        listaNumerosSorteados.push(numeroGenerado);  // Añade el número a la lista
        return numeroGenerado;
    }
}

function condicionesIniciales() {
    asignarTextoElemento('h1', 'Juego del número secreto');
    asignarTextoElemento('p', 'Indica un número del 1 al 10');
numeroSecreto = generarNumeroSecreto ();
intentos = 1;

}


function reiniciarJuego() {
    //limpiar caja
    limpiarCaja();
    //deshabilitar el boton de nuevo juego
     condicionesIniciales();

    //inicializar el numero de intentos
    document.querySelector ('#reiniciar').setAttribute('disabled','true');
}
// Asigna texto a los elementos h1 y p
condicionesIniciales();
generarNumeroSecreto();


  <h1>Bienvenidos a nuestra tienda en línea</h1>
  <p>Encuentra los mejores productos y ofertas</p>
</div>

<div class="container">
  <div class="row">
    <div class="col-sm-4">
      <h3>Accesorios para móviles</h3>
      <img src="https://via.placeholder.com/300x200" class="img-fluid" alt="Accesorios para móviles">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <a href="#" class="btn btn-primary">Comprar ahora</a>
    </div>
    <div class="col-sm-4">
      <h3>Fundas para móviles</h3>
      <img src="https://via.placeholder.com/300x200" class="img-fluid" alt="Fundas para móviles">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <a href="#" class="btn btn-primary">Comprar ahora</a>
    </div>
    <div class="col-sm-4">
      <h3>Audífonos inalámbricos</h3>
      <img src="https://via.placeholder.com/300x200" class="img-fluid" alt="Audífonos inalámbricos">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <a href="#" class="btn btn-primary">Comprar ahora</a>
    </div>
  </div>
</div>

</body>
</html>

  <h1>Bienvenidos a nuestra tienda en línea</h1>
  <p>Encuentra los mejores productos y ofertas</p>
</div>

<div class="container">
  <div class="row">
    <div class="col-sm-4">
      <h3>Accesorios para móviles</h3>
      <img src="https://via.placeholder.com/300x200" class="img-fluid" alt="Accesorios para móviles">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <a href="#" class="btn btn-primary">Comprar ahora</a>
    </div>
    <div class="col-sm-4">
      <h3>Fundas para móviles</h3>
      <img src="https://via.placeholder.com/300x200" class="img-fluid" alt="Fundas para móviles">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <a href="#" class="btn btn-primary">Comprar ahora</a>
    </div>
    <div class="col-sm-4">
      <h3>Audífonos inalámbricos</h3>
      <img src="https://via.placeholder.com/300x200" class="img-fluid" alt="Audífonos inalámbricos">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <a href="#" class="btn btn-primary">Comprar ahora</a>
    </div>
  </div>
</div>

</body>
</html>
