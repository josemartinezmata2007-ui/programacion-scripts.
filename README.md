# Informe Técnico: Programación de Scripts

**Autor:** José Martínez  
**Asignatura:** Programación de Scripts / Informática  

---

## 1. Introducción
Un **script** (o guión de código) es un conjunto de instrucciones escritas en un lenguaje de programación interpretado (como PHP, JavaScript o Python) que se ejecutan secuencia a secuencia para automatizar tareas, manipular datos e interactuar con el usuario a través de interfaces web o de consola. A diferencia de los lenguajes compilados (como C++ o Java), los scripts se ejecutan mediante un intérprete en tiempo real, lo que agiliza el desarrollo de aplicaciones dinámicas.

---

## 2. Variables
Una **variable** es un espacio en memoria reservado para almacenar valores que pueden cambiar durante la ejecución del script.

* **Tipos de datos comunes:**
  * **Enteros (Integer):** Números sin decimales (ej. `19`, `-5`).
  * **Flotantes (Float/Double):** Números con decimales (ej. `18.5`).
  * **Cadenas de texto (String):** Secuencias de caracteres (ej. `"Hola mundo"`).
  * **Booleanos (Boolean):** Valores de verdad (`true` o `false`).
* **Alcance (Scope):** Determina la visibilidad de una variable. Pueden ser **locales** (acceso solo dentro de la función donde se definen) o **globales** (acceso en todo el script).

---

## 3. Operadores
Los operadores permiten realizar cálculos, comparaciones y evaluaciones lógicas.

1. **Aritméticos:** Realizan operaciones matemáticas (`+` suma, `-` resta, `*` multiplicación, `/` división, `%` módulo).
2. **Relacionales / Comparación:** Comparan dos valores devolviendo un booleano (`==` igual a, `===` idéntico, `!=` diferente, `>` mayor que, `<` menor que, `>=` mayor o igual, `<=` menor o igual).
3. **Lógicos:** Combinan expresiones booleanas (`&&` / `AND` intersección, `||` / `OR` unión, `!` / `NOT` negación).

---

## 4. Sentencias de Control
Controlan el flujo de ejecución de las instrucciones dentro del script.

* **Condicionales:**
  * `if / else`: Ejecuta un bloque de código si se cumple una condición determinada; de lo contrario, ejecuta otro bloque.
  * `switch`: Selecciona uno de muchos bloques de código a ejecutar en función del valor de una expresión.
* **Bucles (Iteraciones):**
  * `for`: Repite un bloque de código un número conocido de veces.
  * `while`: Repite el bloque mientras una condición se mantenga verdadera.
  * `foreach`: Diseñado para recorrer estructuras como arreglos o vectores iterando elemento por elemento.

---

## 5. Vectores (Tablas / Arreglos)
Un **vector** o *array* es una estructura de datos que permite almacenar múltiples elementos bajo una sola variable.

* **Vectores Indexados:** Usan índices numéricos consecutivos que inician en cero (ej. `$frutas = ["Manzana", "Pera", "Uva"];`).
* **Vectores Asociativos:** Utilizan claves personalizadas (cadenas) en lugar de índices numéricos para acceder a cada valor (ej. `$usuario = ["nombre" => "José", "edad" => 19];`).

---

## 6. Formularios
Los formularios HTML permiten la recolección de datos ingresados por el usuario para ser procesados por un script en el servidor.

* **Métodos de Envío:**
  * `GET`: Envía los datos adjuntos en la URL. Es visible, de longitud limitada y útil para búsquedas o consultas.
  * `POST`: Envía los datos de forma oculta en el cuerpo de la petición HTTP. Es más seguro para información sensible (contraseñas) y volúmenes de datos grandes.
* **Procesamiento:** El script recibe la información del formulario mediante arreglos globales (como `$_POST` o `$_GET` en PHP) e interactúa validando o guardando la entrada.

---

## 7. Almacenamiento de Información con Bases de Datos (BD)
Para guardar información de forma permanente y estructurada, los scripts interactúan con **Sistemas Gestores de Bases de Datos (SGBD)** relacionales (como MySQL o PostgreSQL).

* **Ciclo de interacción:**
  1. **Conexión:** Establecimiento del enlace cliente-servidor mediante credenciales de acceso.
  2. **Ejecución de consultas SQL (CRUD):**
     * **Create:** Operaciones `INSERT` para registrar nuevos datos.
     * **Read:** Operaciones `SELECT` para consultar información existente.
     * **Update:** Operaciones `UPDATE` para actualizar registros.
     * **Delete:** Operaciones `DELETE` para eliminar datos.
  3. **Cierre de conexión:** Liberación de recursos en el servidor.

---

## 8. Gestión de Archivos
Permite a un script interactuar directamente con el sistema de archivos del servidor (lectura, creación, modificación y eliminación de archivos).

* **Operaciones Principales:**
  * **Apertura:** Modos de acceso (`r` lectura, `w` escritura sobrescribiendo, `a` escritura al final/append).
  * **Lectura/Escritura:** Métodos para leer líneas/bloques o escribir datos formateados (como archivos `.txt`, `.json` o `.csv`).
  * **Cierre:** Garantiza que los cambios se guarden correctamente en disco y no queden archivos bloqueados en memoria.
