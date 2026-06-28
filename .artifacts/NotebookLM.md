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
