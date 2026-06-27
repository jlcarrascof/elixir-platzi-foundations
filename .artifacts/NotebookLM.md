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
