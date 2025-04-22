primer error encontrado: 
 let randomNumber = Math.random() * 10;
 SOLUCION:   let randomNumber = Math.floor(Math.random() * 100) + 1;
 el programa ha sido dieseñado para poder encontrar un numero de entre uno y cien.


segundo error: 
const lowOrHi = document.querySelector('lowOrHi');
SOLUCION: const lowOrHi = document.querySelector('.lowOrHi');
Hace falta el punto para la clase.

tercer error: 
guessSubmit.addeventListener('click', checkGuess);
resetButton.addeventListener('click', resetGame);
SOLUCION: addEventListener
JavaScript ditingue entre mayusculas y minusculas en los nombres de los metodos.


Cuarto error: 
let userGuess = guessField.value;
SOLUCION: let userGuess = Number(guessField.value);
no se puede comparar un valor de tipo texto con un valor de tipo numero.

Sexto error: 
    if(userGuess === randomNumber) {
      lastResult.textContent = '!!!Pérdistes!!!';
      lastResult.style.backgroundColor = 'black';
      lowOrHi.textContent = '';
      setGameOver();
    } else if(guessCount === ATTEMPS) {
      lastResult.textContent = 'Felicitaciones! adivinaste el número!';
      lastResult.style.backgroundColor = 'red';
      setGameOver();
SOLUCION: 
    if (userGuess === randomNumber) {
  lastResult.textContent = '¡Felicitaciones! ¡Adivinaste!';
  lastResult.style.backgroundColor = 'green';
  lowOrHi.textContent = '';
  setGameOver();
} else if (guessCount === ATTEMPTS) {
  lastResult.textContent = '!!!Pérdistes!!!';
  lastResult.style.backgroundColor = 'red';
  setGameOver();
Logica Invertida, cuando el usuario adivina el numero, muestra “¡¡¡Perdiste!!!” y cuando agota sus intentos muestra “¡Felicitaciones! adivinaste”.

Septimo error: 
const ATTEMPS = 5;
SOLUCION : const ATTEMPS = 10;
El programa esta diseñado para que el usuario tenga diez intentos y en este caso el programa solo esta aceptando cinco intentos.

Agregacion de codigo para la validacion que sea un entero en el rango de uno a cien: 
 if (!Number.isInteger(userGuess) || userGuess < 1 || userGuess > 100) {
          alert('Por favor, ingresa un número entero válido entre 1 y 100.');
          guessField.value = '';
          guessField.focus();
          return; 
        }
no incrementa los intentos que tiene cada usuario



