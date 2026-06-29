# Sprint 1: Conceptos básicos - NotebookLM

## Capítulo 1: Programación Funcional en Elixir para Backend

### Resumen del Video

Este curso es una introducción a Elixir enfocada en enseñar los aspectos más importantes del funcionamiento de este lenguaje funcional. El enfoque está orientado a aplicar las herramientas de Elixir desarrollando la primera fase del proyecto Hangman (el juego del ahorcado).

### Requisitos Previos

Es fundamental tener conocimiento previo de algún lenguaje de programación, preferiblemente enfocado al backend. Este no es un curso de programación básica. Si no se tiene experiencia previa, se recomienda comenzar con la trilogía de Python de Platzi:

- Curso Básico de Python
- Curso de Python Intermedio: Comprehensions, Lambdas y Manejo de Errores
- Curso Profesional de Python

### Contexto Adicional

**¿Qué es Elixir?**
Elixir es un lenguaje de programación funcional diseñado para construir sistemas escalables y mantenibles. Se ejecuta sobre la máquina virtual de Erlang (BEAM), lo que le permite:

- Manejar millones de conexiones simultáneas
- Tolerancia a fallos inherente
- Código distribuido fácilmente
- Baja latencia

**¿Por qué programación funcional?**
A diferencia de la programación imperativa (como Python o JavaScript), la programación funcional:
- Usa funciones puras (sin efectos secundarios)
- Los datos son inmutables (no cambian)
- Se enfoca en "qué" hacer, no en "cómo"
- Facilita el paralelismo y concurrencia

**El Proyecto: Hangman**
Desarrollaremos el juego del ahorcado como proyecto práctico. Esto nos permitirá:
- Aplicar conceptos de Elixir en un proyecto real
- Entender módulos y funciones
- Practicar lógica de juegos
- Implementar características avanzadas gradualmente

### Próximos Pasos

En las siguientes clases exploraremos:
- ¿Por qué Elixir?
- Primeros pasos con Elixir
- Introducción a Livebook
- Tipos de datos básicos
- Funciones anónimas, listas y tuplas

### Dudas y Preguntas

*(Sin dudas registradas en esta sesión)*

---

## Capítulo 2: ¿Por qué Elixir?

### Resumen del Video

Este capítulo explica por qué los lenguajes funcionales como Elixir han ganado popularidad recientemente y qué hace especial a Elixir.

### El Problema: Los Procesadores Ya No Son Más Rápidos

**Imagina esto:** Antes, cada año los procesadores de computadora eran más rápidos automáticamente. Tu programa corría más rápido sin que tú hicieras nada. Era como un "almuerzo gratis".

**Pero eso terminó:** En 2005, Herb Sutter (un experto en C++) publicó un famoso paper diciendo que los procesadores habían llegado a su límite físico de velocidad. Ya no podían ser más rápidos.

**La solución:** En lugar de hacer un procesador súper rápido, ahora hacen procesadores con múltiples "cerebros" (cores) que trabajan al mismo tiempo. Es como tener varios ayudantes en lugar de uno súper rápido.

### El Desafío: Programación Concurrente

**El problema:** Para aprovechar estos múltiples cores, tienes que reescribir tu programa para que haga varias cosas al mismo tiempo (concurrente). Pero esto es muy difícil si tienes que hacerlo desde cero.

**La buena noticia:** Los lenguajes que ya soportan programación concurrente obtuvieron una nueva vida. Elixir es uno de ellos.

### ¿Qué es Elixir?

**Elixir es como un superhéroe:**
- Es un lenguaje dinámico y funcional
- Diseñado para construir aplicaciones que:
  - Escalan (crecen sin problemas)
  - Son tolerantes a fallos (si algo falla, no todo se cae)
  - Son fáciles de mantener

**Corre sobre la máquina virtual de Erlang (BEAM):**
- Piensa en Erlang como el "motor" o "plataforma" donde corre Elixir
- Erlang fue creado por Ericsson en los años 80 para sistemas telefónicos
- Tiene décadas de experiencia en producción

### El Ecosistema de Erlang

**Es como una familia de lenguajes:** La máquina virtual de Erlang puede correr varios lenguajes:
- Elixir (el que aprenderemos)
- Elixir tipado estático (como Alpaca)
- Prolog
- Lúa
- Y otros más

### ¿Por Qué Erlang es Tan Especial?

**Erlang usa procesos pequeños:**
- Imagina miles de pequeños trabajadores que trabajan al mismo tiempo
- Cada trabajador tiene su propio espacio y no molesta a los demás
- Se comunican enviándose mensajes (como cartas)

**Estadísticas increíbles de Cisco:**
- Más de 2 millones de dispositivos con Erlang
- El 90% del tráfico de internet pasa por nodos controlados por Erlang
- Los 8 mayores proveedores de internet usan Erlang

**Intentaron reemplazar Erlang:**
- Una empresa intentó reescribir su sistema en C: tomó 10 veces más esfuerzo
- Otra intentó en Java: después de 6 meses se dieron por vencidos

**Lección:** Usa el lenguaje correcto para el problema correcto.

### ¿Por Qué José Valim Creó Elixir?

**José Valim (el creador de Elixir) amaba Erlang pero extrañaba cosas de otros lenguajes:**
- Metaprogramación (código que escribe código)
- Polimorfismo (mismo nombre, diferentes comportamientos)
- Herramientas que aumentan su productividad

**Decisión:** Creó un nuevo lenguaje encima de la máquina virtual de Erlang, pero con sintaxis moderna y herramientas de productividad.

### Cómo Se Ve Elixir

**Ejemplo de código:**
```elixir
# Llamamos a un módulo llamado "grapheme"
# Llamamos a una función llamada "frequencies"
# Le pasamos un binario (texto)
# Nos retorna las frecuencias de las letras
Grapheme.frequencies("elixir")
# => %{e: 1, i: 2, l: 1, r: 1, x: 1}
```

**Conceptos clave:**
- Las funciones están dentro de módulos
- Cada módulo puede tener su propia documentación
- Cada función también puede tener documentación

### Empresas Que Usan Elixir en Producción

**Casos de éxito documentados:**
- Heroku (plataforma de cloud)
- Discord (chat para gamers)
- Pepsi (empresa de bebidas)
- Mozilla (creadores de Firefox)
- Change.org (plataforma de peticiones)
- Apple (backend de algunos servicios)
- Adobe (donde trabaja el profesor)

### Contexto Adicional

**La revolución de la concurrencia:**
- Antes: 1 core muy rápido
- Ahora: Múltiples cores trabajando en paralelo
- Futuro: Miles de cores en un solo chip

**Por qué Elixir es perfecto para esto:**
- Inmutabilidad: Los datos no cambian, así que no hay conflictos
- Pase de mensajes: Los procesos se comunican sin compartir memoria
- Funciones puras: Sin efectos secundarios, más fácil de predecir

**Analogía para niños:**
- Imperativo (Python/Java): Como una cocina donde todos cocinan en la misma olla
- Funcional (Elixir): Como múltiples cocineros en sus propias cocinas, enviándose platos por una ventanilla

### Dudas y Preguntas

*(Sin dudas registradas en esta sesión)*

---

## Capítulo 3: Primeros Pasos con Elixir

### Resumen del Video

Este capítulo muestra cómo instalar Elixir y usar su consola interactiva (IEx) por primera vez.

### Instalación de Elixir

**Pasos generales:**
1. Ir al sitio oficial de Elixir (elixir-lang.org)
2. Ir a la pestaña "Install"
3. Seleccionar tu sistema operativo (MacOS, Linux, Windows)
4. Seguir las instrucciones según tu manejador de paquetes

**Para MacOS (con Homebrew):**
```bash
# Ver información del paquete
brew info elixir

# Instalar Elixir
brew install elixir
```

**Nota importante:** Elixir depende de Erlang. Si no lo tienes instalado, el manejador de paquetes lo instalará automáticamente.

### Verificar la Instalación

**Para verificar la versión instalada:**
```bash
elixir -v
```

Esto mostrará:
- Versión de Erlang/OTP
- Versión de Elixir

**Ejemplo de salida:**
```
Erlang/OTP 26 [erts-14.2.5] [source] [64-bit] [smp:4:4] [ds:4:4:10] [async-threads:1] [jit:ns]
Elixir 1.16.3 (compiled with Erlang/OTP 26)
```

### IEx: Consola Interactiva de Elixir

**¿Qué es IEx?**
- IEx = Interactive Elixir
- Es como una calculadora poderosa donde puedes probar código de Elixir
- Similar a la consola de Python (REPL)

**Para iniciar IEx:**
```bash
iex
```

**Para salir de IEx:**
- Presiona `Ctrl+C` dos veces
- O escribe `System.halt()`

**Ejemplo de uso:**
```elixir
iex(1)> 1 + 1
2
iex(2)> 2 * 3
6
iex(3)> 10 / 2
5.0
```

### Ejecutables Incluidos con Elixir

Al instalar Elixir, obtienes varios ejecutables:
- `elixir` - Para ejecutar archivos .ex
- `iex` - Consola interactiva
- `mix` - Herramienta de construcción (como npm para Node.js)
- `elixirc` - Compilador de Elixir

**Reto del video:** Ir a la documentación oficial y explorar qué otros ejecutables vienen incluidos.

### Contexto Adicional

**¿Por qué usar IEx?**
- Es perfecto para experimentar con código
- Puedes probar funciones sin crear archivos
- Aprender la sintaxis de forma interactiva
- Depurar código rápidamente

**Analogía para niños:**
- IEx es como un patio de recreo donde puedes probar diferentes juguetes (código) sin tener que construir toda la casa (programa completa)

**Sistemas operativos soportados:**
- MacOS (Homebrew, MacPorts)
- Linux (varias distribuciones)
- Windows (instalador oficial, Chocolatey)

### Dudas y Preguntas

**¿Cómo salgo de la terminal iex?**
Para salir de IEx, puedes:
1. Presionar `Ctrl+C` dos veces seguidas
2. Escribir `System.halt()` y presionar Enter

---

## Capítulo 4: Introducción a Livebook

### Resumen del Video

Este capítulo introduce Livebook, una herramienta del ecosistema Elixir para crear notebooks interactivos con celdas de código y markdown.

### ¿Qué es Livebook?

**Livebook es como un cuaderno mágico:**
- Puedes crear notebooks con celdas de código Elixir
- También tiene celdas de texto en formato markdown
- Es perfecto para prototipado rápido
- Autores de librerías pueden crear tutoriales interactivos

**Casos de uso:**
- Prototipado rápido de ideas
- Tutoriales interactivos de librerías
- Aprendizaje de Elixir
- Documentación ejecutable

### Instalación de Livebook

**Opciones de instalación:**
1. **Local con Elixir** (la que usamos)
2. **Docker**
3. **Servicio en la nube** (Fly.io)

**Pasos para instalación local:**

1. **Instalar Rebar3** (herramienta para construir proyectos Erlang)
   ```bash
   mix local.rebar --force
   ```

2. **Instalar Hex** (manejador de paquetes del ecosistema Erlang/Elixir)
   ```bash
   mix local.hex --force
   ```

3. **Instalar Livebook desde Hex**
   ```bash
   mix escript.install hex livebook
   ```

### ¿Qué es un Script (Escript)?

**Analogía:** Un script es como un programa portable que puedes ejecutar desde la terminal.

**Características:**
- Es un ejecutable que se invoca desde la línea de comandos
- Puede correr en cualquier plataforma donde tengas Erlang/Elixir
- No necesita instalar Elixir porque está embebido en el script
- Livebook es un ejemplo de escript

### Configurar el PATH

**¿Por qué agregar al PATH?**
Para poder ejecutar `livebook` desde cualquier lugar sin escribir la ruta completa.

**En el video (Mac con fish):**
```bash
fish_add_path ~/.mix/escripts
```

**En Linux (bash):**
```bash
export PATH="$HOME/.asdf/installs/elixir/1.18.0/.mix/escripts:$PATH"
```

**Para hacerlo permanente:**
```bash
echo 'export PATH="$HOME/.asdf/installs/elixir/1.18.0/.mix/escripts:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

### Ejecutar Livebook

**Para iniciar Livebook:**
```bash
livebook server
```

**Opciones adicionales:**
- Por defecto usa tu home directory
- Puedes especificar otro directorio con `--home`

**Livebook genera un servidor web:**
- Necesitas ir al navegador para verlo
- Te pedirá un token de seguridad
- El token aparece en la terminal

### Conceptos Clave: Celdas

**La unidad básica de Livebook es la CELDA:**

**Celdas de Markdown:**
- Contienen texto formateado
- Títulos, listas, explicaciones
- Como documentos de documentación

**Celdas de Código:**
- Contienen código Elixir
- Al ejecutarlas, evalúan código Elixir real
- Es como IEx pero con un editor visual

**Analogía para niños:**
- Livebook es como IEx (la consola) + un editor de texto
- Es como tener una pizarra mágica donde escribes código y se ejecuta solo

### Celdas Inteligentes

**Livebook tiene celdas especiales:**
- Pueden generar gráficos
- Pueden conectarse a bases de datos (PostgreSQL, MySQL)
- Pueden instalar paquetes de Elixir y Erlang
- Requieren reiniciar la sesión para instalar dependencias

**Ejemplo de conexión a base de datos:**
1. Seleccionar celda inteligente de PostgreSQL
2. Livebook pide reiniciar la sesión
3. Llenar el cuadro de diálogo con datos de conexión
4. Puedes hacer queries directamente desde Livebook

### Instalar Paquetes en Livebook

**Puedes instalar paquetes directamente:**
- Paquetes de Elixir
- Paquetes de Erlang
- Usarlos mientras defines tu prototipo

**Esto es útil porque:**
- No necesitas salir de Livebook
- Todo está en un solo lugar
- Puedes experimentar rápidamente

### Reto del Video

**Orden recomendado de notebooks a explorar:**
1. Welcome to Livebook
2. Elixir and Livebook

### Contexto Adicional

**Livebook vs Jupyter:**
- Livebook es para Elixir (como Jupyter es para Python)
- Pero Livebook tiene características únicas del ecosistema Elixir

**Ventajas de Livebook:**
- Interfaz moderna
- Celdas inteligentes
- Integración con bases de datos
- Colaboración en tiempo real
- Despliegue fácil

**Analogía para niños:**
- Livebook es como un laboratorio de ciencias donde tienes:
  - Una pizarra para escribir (markdown)
  - Un microscopio para experimentar (código)
  - Herramientas especiales para conectar cosas (celdas inteligentes)

### Dudas y Preguntas

**Problema: Livebook requiere Elixir 1.18+ pero tenía 1.16.3**
**Solución:** Actualizar Elixir usando asdf:
```bash
asdf install elixir 1.18.0
asdf global elixir 1.18.0
```

**Problema: livebook server dice "command not found"**
**Causa:** Livebook se instaló pero no está en el PATH
**Solución:** Agregar la ruta de escripts al PATH:
```bash
export PATH="$HOME/.asdf/installs/elixir/1.18.0/.mix/escripts:$PATH"
```

**¿Necesito instalar Hex y Rebar manualmente?**
- **Hex:** Viene incluido con Elixir moderno, pero `mix local.hex --force` asegura que esté actualizado
- **Rebar3:** Solo si necesitas compilar dependencias puras de Erlang

**¿Necesito agregar el PATH con asdf?**
- asdf moderno maneja esto automáticamente con shims
- Pero los escripts de Mix necesitan PATH manual
- La ruta es específica de la versión de Elixir instalada

---

## Capítulo 5: Tipos de Datos Básicos - Parte 1

### Resumen del Video

Este capítulo explora los tipos de datos básicos que soporta Elixir: enteros, flotantes, booleanos, átomos, cadenas, listas y tuplas. Se practica en Livebook con operaciones aritméticas y funciones de documentación.

### Tipos de Datos Básicos en Elixir

**Elixir soporta:**
- Enteros (integers)
- Flotantes (decimales)
- Booleanos (true/false)
- Listas
- Tuplas
- Mapas
- Átomos (símbolos)
- Cadenas (strings)

### Operaciones Aritméticas

**En Livebook:**
1. Crear un nuevo notebook
2. Agregar celdas de código
3. Evaluar con el botón "Evaluate"

**Operaciones básicas:**
```elixir
# Suma
1 + 1
# => 2

# Multiplicación
2 * 3
# => 6

# División (siempre devuelve flotante)
10 / 2
# => 5.0
```

**División entera:**
```elixir
# div/2 - división entera
div(10, 3)
# => 3

# rem/2 - remanente de la división
rem(10, 3)
# => 1
```

**Nota sobre paréntesis:**
- Elixir no obliga a usar paréntesis
- Esto hace el código más limpio
- Se recomienda paréntesis para funciones normales
- Sin paréntesis para funciones de control de flujo

**Funciones de redondeo:**
```elixir
# round/1 - redondea al entero más cercano
round(3.58)
# => 4

# trunc/1 - corta la parte decimal
trunc(3.58)
# => 3
```

**Números flotantes:**
- Tienen doble precisión de 64 bits
- Siempre devuelven decimales en operaciones

### Identificando Funciones y Documentación

**Cómo se identifica una función:**
- Nombre del módulo
- Nombre de la función
- Número de argumentos (aridad)

**Ejemplo:** `div/2` significa función `div` con 2 argumentos.

**En IEx (consola interactiva):**
```elixir
# h/1 - muestra documentación de una función
h(trunc)
```

**En Livebook:**
- Pasa el cursor sobre el nombre de la función
- Aparece la documentación automáticamente
- También funciona para módulos

**Módulo Kernel:**
- Es autoimportado (no necesitas escribir el nombre)
- Contiene funciones básicas como `div`, `rem`, `round`, `trunc`

### Valores Booleanos

**Elixir soporta:**
- `true`
- `false`

**Operaciones:**
```elixir
# Comparación
true == false
# => false

# Verificar tipo de dato
is_boolean(true)
# => true

is_boolean(1)
# => false
```

**Funciones de verificación de tipo:**
- `is_boolean/1` - ¿es booleano?
- `is_integer/1` - ¿es entero?
- `is_float/1` - ¿es flotante?
- `is_number/1` - ¿es número?

### Átomos (Símbolos)

**¿Qué es un átomo?**
- Una constante cuyo valor es su propio nombre
- En otros lenguajes se llaman "símbolos"
- Se usan para enumerar valores

**Ejemplos:**
```elixir
:apple
:orange
:water
```

**Comparaciones:**
```elixir
:apple == :orange
# => false
```

**Usos comunes:**
- Expresar estado de operaciones
- `:ok` - operación exitosa
- `:error` - operación fallida

**Booleanos son átomos:**
```elixir
# true y false también son átomos
is_atom(true)
# => true

is_atom(:ok)
# => true
```

**Alias (módulos):**
- Comienzan con letra mayúscula
- También son átomos
- Ejemplo: `Hello` es un átomo

```elixir
is_atom(Hello)
# => true
```

### Cadenas (Strings)

**Cadenas básicas:**
```elixir
"hello world"
```

**Interpolación:**
```elixir
name = "world"

"hello #{name}"
# => "hello world"
```

**Saltos de línea:**
```elixir
"hello\nworld"
```

**Imprimir cadenas:**
```elixir
IO.puts("hello\nworld")
# hello
# world
# => :ok
```

**Nota:** `IO.puts/1` devuelve `:ok` como resultado, pero tiene el efecto secundario de imprimir.

**Módulo String:**
```elixir
# length/1 - longitud de la cadena
String.length("hello")
# => 5

# upcase/1 - convertir a mayúsculas
String.upcase("hello")
# => "HELLO"
```

### Organización de Celdas en Livebook

**Reordenar celdas:**
- Puedes mover celdas arriba/abajo
- Útil si cometiste un error en el orden
- Arrastra y suelta

### Contexto Adicional

**Por qué Elixir es especial:**
- Documentación excelente
- Muchas funciones incluyen ejemplos
- Livebook muestra documentación automáticamente

**Analogía para niños:**
- **Enteros:** Como contar manzanas enteras (1, 2, 3)
- **Flotantes:** Como medir con regla (1.5, 2.7, 3.14)
- **Booleanos:** Como responder sí o no (true/false)
- **Átomos:** Como etiquetas con nombres (:rojo, :verde, :azul)
- **Cadenas:** Como escribir cartas ("hola mundo")

**Diferencia clave:**
- `div(10, 3)` → 3 (división entera)
- `10 / 3` → 3.333... (división flotante)

**Arity (número de argumentos):**
- Es importante en Elixir
- `round/1` vs `round/2` son funciones diferentes
- La documentación siempre muestra la aridad

### Dudas y Preguntas

*(Sin dudas registradas en esta sesión)*

---

## Capítulo 6: Tipos de Datos Básicos - Parte 2

### Resumen del Video

Este capítulo continúa explorando los tipos de datos básicos de Elixir: funciones anónimas, listas y tuplas. Se practica en Livebook con ejemplos prácticos.

### Funciones Anónimas

**¿Qué son las funciones anónimas?**
- Son funciones sin nombre
- Pueden ser asignadas a variables
- Se pueden pasar como argumentos
- Están delimitadas por `fn` y `end`

**Sintaxis:**
```elixir
# Definir función anónima
add = fn a, b -> a + b end

# Invocar función anónima
add.(1, 2)
# => 3
```

**Nota importante:** Para invocar una función anónima, se usa un punto `.` antes de los paréntesis.

**Verificar si es una función:**
```elixir
# is_function/1 - verifica si es función
is_function(add)
# => true

# is_function/2 - verifica si es función con N argumentos
is_function(add, 2)
# => true
```

### Clausuras (Closures)

**¿Qué es una clausura?**
- Las funciones anónimas pueden acceder a variables del alcance donde fueron definidas
- Esto se llama "closure" o clausura

**Ejemplo:**
```elixir
# Función que suma
add = fn a, b -> a + b end

# Función que usa la función anterior
double = fn x -> add.(x, x) end

double.(2)
# => 4
```

### Alcance de Variables (Scope)

**Regla importante:** Una variable definida fuera del alcance de una función NO puede ser redefinida dentro de la función.

**Ejemplo:**
```elixir
x = 42

# Intentar redefinir x dentro de la función
# Esto NO funcionará
change_x = fn -> x = 0 end
```

**Analogía para niños:**
- Imagina que tienes una caja con tu nombre afuera
- Dentro de la caja no puedes cambiar el nombre de la caja
- Solo puedes mirar lo que hay dentro

### Listas

**¿Qué son las listas?**
- Colecciones de valores
- Usan corchetes `[]`
- Pueden contener cualquier tipo de dato

**Sintaxis:**
```elixir
[1, 2, 3, true]
```

**Funciones de listas:**
```elixir
# length/1 - longitud de la lista
length([1, 2, 3])
# => 3
```

**Concatenar listas:**
```elixir
# ++ - concatenar
[1, 2] ++ [3, 4]
# => [1, 2, 3, 4]
```

**Restar elementos:**
```elixir
# -- - restar elementos
[1, 2, 3, true] -- [true]
# => [1, 2, 3]
```

**Nota importante sobre la resta:**
- Solo elimina la PRIMERA coincidencia
- Ejemplo: `[true, false, 3, true] -- [false, true]` solo elimina `false` y la primera `true`

### Inmutabilidad

**Concepto clave:** Las estructuras de datos en Elixir son INMUTABLES.

**¿Qué significa?**
- Concatenar o remover elementos SIEMPRE retorna una lista NUEVA
- La lista original NO se modifica
- Las operaciones transforman datos, no los mutan

**Ventajas de la inmutabilidad:**
- Código más limpio
- Puedes pasar datos con garantía de que no serán modificados
- Sin efectos secundarios inesperados

**Analogía para niños:**
- **Mutable:** Como una pizarra donde borras y escribes (la pizarra cambia)
- **Inmutable:** Como una hoja de papel donde escribes una nueva (la hoja original sigue igual)

### Cabeza y Cola de Listas

**Conceptos importantes:**
- **Head (cabeza):** Primer elemento de la lista
- **Tail (cola):** Resto de los elementos

**Funciones:**
```elixir
lista = [1, 2, 3]

# hd/1 - obtener primer elemento
hd(lista)
# => 1

# tl/1 - obtener resto de elementos
tl(lista)
# => [2, 3]
```

**Advertencia:** Si intentas obtener `hd` o `tl` de una lista vacía, obtendrás un error.

### Tuplas

**¿Qué son las tuplas?**
- Colecciones de valores
- Usan llaves `{}`
- Pueden contener diferentes tipos de datos

**Sintaxis:**
```elixir
{:ok, "hello"}
```

**Características:**
- Se almacenan de manera contigua en memoria
- Acceso rápido por índice
- Obtener tamaño es rápido

**Funciones de tuplas:**
```elixir
# tuple_size/1 - tamaño de la tupla
tuple_size({:ok, "hello"})
# => 2

# elem/2 - obtener elemento por índice
elem({:ok, "hello"}, 0)
# => :ok

elem({:ok, "hello"}, 1)
# => "hello"
```

**Nota:** Los índices comienzan desde 0.

**Poner elemento en tupla:**
```elixir
# put_elem/3 - poner elemento en índice (retorna nueva tupla)
put_elem({:ok, "hello"}, 1, "world")
# => {:ok, "world"}

# La tupla original NO cambia
{:ok, "hello"}
# => {:ok, "hello"}
```

### Listas vs Tuplas

**¿Cuándo usar listas:**
- Cuando necesitas agregar/remover elementos frecuentemente
- Cuando el orden es importante
- Cuando la cantidad de elementos puede variar

**¿Cuándo usar tuplas:**
- Cuando tienes un número fijo de elementos
- Cuando necesitas acceso rápido por índice
- Cuando representas datos estructurados (como `{:ok, resultado}`)

### Contexto Adicional

**Funciones anónimas vs funciones con nombre:**
- Las funciones anónimas son útiles para callbacks
- Las funciones con nombre se definen en módulos (veremos más adelante)

**Operadores de lista:**
- `++` es O(n) - depende del tamaño de la lista izquierda
- `--` es O(n*m) - depende de ambos tamaños
- Úsalos con cuidado en listas grandes

**Analogía para niños:**
- **Función anónima:** Como una receta sin nombre que puedes guardar en una caja
- **Lista:** Como un tren con vagones (puedes agregar/quitar vagones)
- **Tupla:** Como una caja con compartimentos fijos (rápido de encontrar, difícil de cambiar)

**Inmutabilidad en la práctica:**
```elixir
# Esto NO modifica la lista original
lista = [1, 2, 3]
nueva_lista = [0] ++ lista

# lista sigue siendo [1, 2, 3]
# nueva_lista es [0, 1, 2, 3]
```

### Reto del Video

**Crear un conversor de monedas:**
- Función anónima que recibe dólares americanos
- Convierte a pesos colombianos
- Ejemplo: `100 USD → X pesos`

### Dudas y Preguntas

*(Sin dudas registradas en esta sesión)*
