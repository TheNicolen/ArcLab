---

## hide:

<div align="center" style="margin-top: 40px; margin-bottom: 55px;">

  <p style="color: #00e5ff; font-size: 0.9em; letter-spacing: 3px; margin-bottom: 10px;">
    ARCLAB STUDIO
  </p>

  <h1 style="font-size: 3em; font-weight: bold; margin-bottom: 15px;">
    Tutoriales
  </h1>

  <p style="
    max-width: 700px;
    margin: 0 auto;
    font-size: 1.1em;
    color: #b0bec5;
    line-height: 1.7;
  ">
    Aprende a utilizar ArcLab y descubre cómo diseñar,
    analizar y transformar sistemas digitales desde una
    única herramienta.
  </p>

</div>

---

# Primeros pasos

Si es la primera vez que utilizas ArcLab, comienza aquí.

En esta sección conocerás la interfaz del programa, aprenderás a crear un diseño y descubrirás las principales herramientas disponibles.

<div style="
  margin: 30px 0 45px 0;
  padding: 25px;
  border-left: 3px solid #00e5ff;
  background: #20232b;
">

<strong style="color: #00e5ff;">Ruta recomendada</strong>

<br><br>

**Interfaz → Esquema lógico → Simulación → RTL → Exportación**

</div>

## La interfaz de ArcLab

ArcLab está dividido en diferentes áreas que permiten construir y analizar un diseño digital.

<!-- IMAGEN: captura general de la interfaz -->

![Interfaz de ArcLab](images/tutoriales/interfaz.png)

### Explorador

Permite visualizar los módulos y elementos que forman parte del proyecto.

### Barra de herramientas

Contiene las herramientas necesarias para agregar entradas, salidas, compuertas, módulos y otras funciones.

### Área de diseño

Es el espacio principal donde se construye y organiza el circuito.

### Herramientas de ingeniería

Desde esta zona es posible acceder a funciones como la generación de RTL, síntesis y otras herramientas de análisis.

---

# 1. Esquema lógico

Aprende a construir circuitos digitales utilizando la interfaz gráfica de ArcLab.

Los esquemas lógicos permiten representar visualmente la estructura de un circuito mediante entradas, salidas, compuertas, módulos y conexiones.

## ¿Qué puedes hacer?

* Crear entradas y salidas.
* Agregar compuertas lógicas.
* Conectar componentes.
* Utilizar módulos.
* Organizar circuitos complejos.
* Simular el comportamiento del diseño.
* Exportar el esquema como imagen.

<!-- IMAGEN: esquema lógico terminado -->

## Crear un circuito

Para comenzar un diseño, agrega las entradas y salidas necesarias para representar el circuito.

<!-- IMAGEN: agregar INPUT y OUTPUT -->

### Agregar compuertas

ArcLab permite utilizar diferentes compuertas lógicas, entre ellas:

* AND
* OR
* XOR
* NOT

<!-- IMAGEN: barra de compuertas -->

## Conectar componentes

Las conexiones permiten definir el flujo de información entre los diferentes elementos del circuito.

<!-- IMAGEN: conexión entre compuertas -->

## Ejemplo: sumador completo

Como primer ejercicio construiremos un **Full Adder**.

El circuito contará con:

* Entrada `A`
* Entrada `B`
* Entrada `Cin`
* Salida `Sum`
* Salida `Cout`

<!-- IMAGEN: full adder -->

### Resultado

Al finalizar deberías obtener un circuito similar al siguiente:

<!-- IMAGEN: resultado full adder -->

---

# 2. Del esquema lógico al RTL

ArcLab permite transformar un diseño gráfico en código RTL utilizando SystemVerilog.

El flujo general es:

<div align="center" style="
  margin: 35px 0;
  font-size: 1.1em;
">

<strong>Esquema lógico</strong>
   →    <strong>ArcLab</strong>
   →    <strong>SystemVerilog</strong>

</div>

## Crear el diseño

Primero construye el circuito utilizando las herramientas de esquemáticos.

<!-- IMAGEN: circuito antes de generar RTL -->

## Generar RTL

Una vez terminado el diseño, utiliza la herramienta de generación de código para obtener la descripción RTL.

<!-- IMAGEN: botón Ver Código Generado -->

## Revisar el código

ArcLab generará una descripción SystemVerilog equivalente al circuito.

Por ejemplo:

```systemverilog
module full_adder(
    input  logic a,
    input  logic b,
    input  logic cin,
    output logic sum,
    output logic cout
);

    assign sum  = a ^ b ^ cin;
    assign cout = (a & b) | (cin & (a ^ b));

endmodule
```

<!-- IMAGEN: código SystemVerilog generado -->

El código generado puede utilizarse posteriormente como punto de partida para la implementación del diseño en una FPGA u otra plataforma compatible con SystemVerilog.

---

# 3. Del RTL al esquema lógico

El flujo también puede realizarse en sentido contrario.

ArcLab puede analizar una descripción RTL y construir una representación visual del circuito.

<div align="center" style="
  margin: 35px 0;
  font-size: 1.1em;
">

<strong>SystemVerilog</strong>
   →    <strong>Analizador RTL</strong>
   →    <strong>Esquema lógico</strong>

</div>

## Introducir el RTL

Comienza con un módulo SystemVerilog.

Por ejemplo:

```systemverilog
module logic_example(
    input  logic a,
    input  logic b,
    input  logic c,
    output logic y
);

    assign y = (a & b) | c;

endmodule
```

<!-- IMAGEN: editor SystemVerilog -->

## Generar el esquema

ArcLab analiza la estructura del módulo y genera una representación gráfica de la lógica.

<!-- IMAGEN: botón de generación de esquema -->

## Interpretar el resultado

El esquema generado permite visualizar:

* Entradas.
* Salidas.
* Operaciones lógicas.
* Módulos.
* Conexiones.
* Jerarquía del diseño.

<!-- IMAGEN: RTL convertido a esquema -->

---

# 4. Máquinas de Estado Finito

ArcLab permite diseñar máquinas de estado finito utilizando representaciones gráficas.

Las FSM pueden utilizarse para modelar sistemas secuenciales como:

* Controladores.
* Detectores de secuencia.
* Protocolos.
* Sistemas de control.
* Secuenciadores.

## Conceptos fundamentales

Una máquina de estados está compuesta principalmente por:

**Estados → Transiciones → Entradas → Salidas**

<!-- IMAGEN: FSM sencilla -->

## Flujo de diseño

Una máquina de estados puede construirse siguiendo este proceso:

<div align="center" style="
  margin: 35px 0;
  line-height: 2;
">

<strong>Definir estados</strong> <br>
↓ <br> <strong>Definir entradas y salidas</strong> <br>
↓ <br> <strong>Definir transiciones</strong> <br>
↓ <br> <strong>Analizar el comportamiento</strong> <br>
↓ <br> <strong>Generar RTL</strong>

</div>

---

# 5. Máquinas de Moore

En una máquina de Moore, las salidas dependen únicamente del estado actual.

```text
Estado actual → Salida
```

## Crear una máquina de Moore

Comienza definiendo los estados necesarios para representar el comportamiento del sistema.

<!-- IMAGEN: creación de estados Moore -->

## Definir transiciones

Las transiciones determinan cómo la máquina cambia de un estado a otro dependiendo de las entradas.

<!-- IMAGEN: transiciones Moore -->

## Definir las salidas

Cada estado puede tener asociada una salida determinada.

<!-- IMAGEN: salidas Moore -->

## Ejemplo: detector de secuencia

Como ejercicio podemos construir un detector de una secuencia binaria.

<!-- IMAGEN: detector de secuencia Moore -->

## Generación RTL

Una vez terminado el diseño, ArcLab puede utilizar la información de la máquina de estados para generar su descripción RTL.

<!-- IMAGEN: Moore a RTL -->

---

# 6. Máquinas de Mealy

En una máquina de Mealy, las salidas dependen del estado actual y de las entradas.

```text
Estado actual + Entrada → Salida
```

## Crear una máquina de Mealy

Define inicialmente los estados necesarios para representar el comportamiento.

<!-- IMAGEN: creación FSM Mealy -->

## Definir las transiciones

Cada transición puede asociarse con las condiciones de entrada y las salidas correspondientes.

<!-- IMAGEN: transición Mealy -->

## Ejemplo: detector de secuencia

Construiremos un detector de secuencia utilizando una máquina de Mealy.

<!-- IMAGEN: detector de secuencia Mealy -->

## Moore vs Mealy

| Característica    | Moore              | Mealy                       |
| ----------------- | ------------------ | --------------------------- |
| Salida depende de | Estado             | Estado + entrada            |
| Cambio de salida  | Asociado al estado | Asociado a transición       |
| Representación    | Estado → salida    | Transición → salida         |
| Aplicación        | Control secuencial | Respuesta rápida a entradas |

---

# 7. Diagramas de tiempo

Los diagramas de tiempo permiten observar cómo evolucionan las señales digitales a través del tiempo.

Son especialmente útiles para analizar circuitos secuenciales y máquinas de estado.

## Conceptos básicos

### Señales

Representan los valores de las entradas, salidas y señales internas del circuito.

### Ticks

Representan los pasos temporales utilizados para analizar el comportamiento.

### Flancos

Permiten identificar cambios de estado en señales digitales.

<!-- IMAGEN: diagrama de tiempo -->

## Crear un diagrama

Selecciona las señales que deseas analizar y agrega sus valores correspondientes.

<!-- IMAGEN: creación de timing diagram -->

## Analizar el comportamiento

Utiliza el diagrama para observar:

* Cambios de estado.
* Respuestas a entradas.
* Señales de reloj.
* Secuencias de activación.
* Errores de comportamiento.

<!-- IMAGEN: análisis de señales -->

## Ejemplo: contador

Podemos utilizar un contador para observar cómo cambian sus salidas en cada ciclo de reloj.

<!-- IMAGEN: contador timing -->

---

# 8. Resolvedor de Álgebra Booleana

ArcLab incorpora una herramienta para trabajar con expresiones de álgebra booleana y observar su simplificación paso a paso.

## Ingresar una expresión

Introduce la función lógica que deseas simplificar.

<!-- IMAGEN: entrada algebra booleana -->

## Operadores

Dependiendo de la sintaxis disponible en ArcLab, pueden utilizarse operadores como:

| Operación | Ejemplo |
| --------- | ------- |
| AND       | `A · B` |
| OR        | `A + B` |
| NOT       | `¬A`    |
| XOR       | `A ⊕ B` |

<!-- IMAGEN: operadores -->

## Simplificación paso a paso

El resolvedor muestra las transformaciones aplicadas a la expresión hasta obtener una forma simplificada.

Por ejemplo:

```text
F = A·B + A·¬B
```

Aplicando factorización:

```text
F = A(B + ¬B)
```

Utilizando la ley del complemento:

```text
F = A
```

<!-- IMAGEN: simplificación paso a paso -->

## Exportar a LaTeX

Una vez obtenida la expresión final, puedes utilizar el resultado para incorporarlo directamente en documentación matemática o informes.

<!-- IMAGEN: exportación LaTeX -->

---

# 9. Ejercicio integrador

Una vez que conozcas las herramientas principales de ArcLab, puedes combinarlas en un mismo proyecto.

## Proyecto: controlador digital

Como ejercicio final puedes construir un sistema que combine:

* Esquema lógico.
* Máquina de estados.
* SystemVerilog.
* Diagramas de tiempo.
* Álgebra Booleana.

### Paso 1 — Diseñar la lógica

<!-- IMAGEN -->

### Paso 2 — Diseñar la FSM

<!-- IMAGEN -->

### Paso 3 — Generar RTL

<!-- IMAGEN -->

### Paso 4 — Analizar las señales

<!-- IMAGEN -->

### Paso 5 — Simplificar la lógica

<!-- IMAGEN -->

### Resultado final

El objetivo es obtener un diseño completo que pueda ser analizado desde diferentes representaciones dentro de ArcLab.

---

<div align="center" style="
  margin: 80px auto 40px auto;
  padding: 45px 20px;
  border-top: 1px solid #30343d;
  border-bottom: 1px solid #30343d;
">

  <p style="
    color: #00e5ff;
    letter-spacing: 2px;
    font-size: 0.85em;
  ">
    ARCLAB STUDIO
  </p>

  <h2 style="margin-bottom: 15px;">
    Aprende. Diseña. Implementa.
  </h2>

  <p style="
    max-width: 600px;
    margin: 0 auto;
    color: #b0bec5;
    line-height: 1.7;
  ">
    Explora las herramientas de ArcLab y desarrolla tus propios
    sistemas digitales desde el esquema hasta el RTL.
  </p>

</div>
