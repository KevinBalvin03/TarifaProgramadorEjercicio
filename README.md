REFACTOR CALCULADORA DE PAGOS PARA PROGRAMADORES
Este programa en Java permite calcular el pago total que debe recibir un programador freelance con base en su experiencia, tipo de contrato, 
horas trabajadas por proyecto y bonificaciones adicionales. Además, realiza descuentos e impuestos aplicables, y genera un reporte detallado de la liquidación. 🧾💰

🐛 Errores encontrados en la versión inicial
A continuación se listan los errores detectados en el código original:

🔸 Errores de sintaxis y compilación
Uso incorrecto de la coma , en tarifaBase = 50,0,0; en lugar del punto decimal ..
Declaración incorrecta del Scanner: Scanner sc = new scanner(system); en lugar de Scanner sc = new Scanner(System.in);.
Uso incorrecto de System.out.print"Ingrese el nombre... (faltaban paréntesis).
Uso incorrecto de métodos del Scanner: nextline(), nex(), scanner.nextLine() → todos mal escritos o usados con nombres incorrectos de variable.
Uso de variables no declaradas o mal nombradas:
leer.nextLine(); (no existe la variable leer)
bonusCliene1, horasProyec1, tarifaHoraFnal y similares no declaradas correctamente.
Expresiones incorrectas:
subtotal ==== pagoProyecto1... (cuádruple signo = en lugar de =)
Falta de punto y coma ; en múltiples líneas.
LocalDate usado sin importar la librería correspondiente.

EXPLICITAMENTE:
En la línea 4, se declaró mal el objeto Scanner al escribirlo en minúscula y referenciar incorrectamente System.
En la línea 8, la instrucción System.out.print no tenía paréntesis ni comillas correctas para la cadena de texto.
En la línea 20, se utilizaron comas en lugar de puntos para definir un número decimal en tarifaBase.
En la línea 10, se escribió incorrectamente nextline() (todo en minúscula).
En las líneas 28 y 30, se utilizaron métodos nex() y next() inexistentes o incompletos para capturar los nombres de los clientes.
En la línea 38, se usaron variables con nombres incorrectos como horasProyec1 y bonusCliene1, las cuales no estaban declaradas previamente.
En la línea 40, se empleó incorrectamente el operador de asignación con múltiples signos de igual (====), lo que genera un error de compilación.
En las líneas 11 y 13, se referenciaron objetos scanner y leer que no fueron declarados ni inicializados, lo cual impide la lectura de datos desde la consola.

✔️ Correcciones generales
Se corrigió la declaración de Scanner con Scanner sc = new Scanner(System.in);.
Se corrigieron todos los nombres de métodos mal escritos como nextline() a nextLine(), nex() a next(), etc.
Se renombraron correctamente todas las variables con errores tipográficos (por ejemplo, bonusCliene1 → bonusCliente1).
Se agregaron los ; faltantes en cada instrucción.
Se corrigió el operador ==== por el correcto =.
Se reemplazaron las comas decimales por puntos (50,0,0 → 50.00).
Se agregó la importación import java.time.LocalDate; para permitir capturar la fecha actual.
Se homogeneizó el uso de la instancia del Scanner (sc) en todo el código.

✨ Mejoras adicionales
Se organizó el flujo de entrada/salida para evitar errores con nextLine() después de nextInt() mediante el uso de sc.nextLine() para limpiar el buffer.
Se utilizó el operador ternario para ajustar la tarifa según el nivel (Senior o Junior).
Se agregó claridad en la salida con etiquetas como ----- REPORTE DE PAGO -----.

REFERENCIAS
https://chatgpt.com/
https://github.com/profejuanjosegallego/examen1logica/
