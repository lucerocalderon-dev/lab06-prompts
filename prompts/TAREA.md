# Tarea: Mi prompt profesional 

## Funcionalidad elegida 
Módulo de **Registro y Gestión de Clientes** con validaciones para una aplicación de escritorio en Java Swing.

## Version 1: prompt basico 
```text
Haz un programa en Java para registrar clientes.
Qué cambié: Se utilizó una petición mínima sin rol, contexto ni formato definido.

Por qué: Para evaluar el resultado base que entrega la IA cuando debe adivinar los requerimientos.

Qué mejoró en la respuesta: La IA entregó un código básico por consola usando Scanner, pero sin interfaz gráfica ni estructura orientada a objetos adecuada.
```

## Version 2: 
```text
Actúa como desarrollador Java. Diseña un formulario en Java Swing para registrar clientes de una tienda. El formulario debe pedir nombre, DNI, correo y teléfono. Al presionar un botón "Registrar", debe mostrar los datos ingresados en un área de texto.

Qué cambié: Se agregó un Rol (Desarrollador Java), la tecnología exacta (Java Swing) y los campos requeridos.

Por qué: Para evitar que la IA asumiera una aplicación de consola y guiara el diseño de la interfaz.

Qué mejoró en la respuesta: Creó la ventana con JFrame, los campos con JTextField y el botón funcional, pero todo el código dentro de una sola clase y sin validaciones de formato.
```

## Version 3: prompt Final 
```text
Actúa como desarrollador Java Senior especialista en interfaces de escritorio. Diseña un módulo de Registro de Clientes utilizando Java Swing para un sistema de ventas comercial.

Contexto: El módulo debe capturar los datos básicos de nuevos clientes (Nombre completo, DNI, Correo electrónico y Teléfono). El sistema requiere almacenar los registros en una lista en memoria y mostrarlos en una tabla (JTable).

Restricciones:
- No uses librerías externas (solo bibliotecas nativas javax.swing y java.awt).
- Valida que ningún campo quede vacío.
- Valida que el DNI contenga exactamente 8 dígitos numéricos.
- Valida que el correo contenga un símbolo "@" y un punto ".".
- Si una validación falla, muestra una alerta emergente con JOptionPane explicándole el error al usuario y detén el proceso.

Ejemplo de mensaje de éxito:
"Cliente [Juan Pérez - DNI: 12345678] registrado correctamente."

Formato de entrega: Explica brevemente la estructura de las clases a utilizar y entrega el código organizado en dos clases separadas: Cliente.java (modelo de datos) y FormularioCliente.java (vista y lógica de la interfaz).

Qué cambié: Se incluyeron los 5 componentes principales, restricciones strictly necesarias (validación de DNI, correo y campos vacíos sin librerías externas), un ejemplo de mensaje y un formato de entrega especificando la arquitectura en dos clases.

Por qué: Para garantizar un código profesional, ordenado, reutilizable y que prevenga errores de ingreso de datos.

Qué mejoró en la respuesta: Entregó un código modular (Modelo-Vista), con validaciones mediante JOptionPane, uso de JTable para visualizar registros y cumplimiento de todas las restricciones.
```

## Componentes del prompt final 
| Componente | Texto exacto en mi prompt |
|---|---|
| **Rol** | `Actúa como desarrollador Java Senior especialista en interfaces de escritorio.` |
| **Instrucción** | `Diseña un módulo de Registro de Clientes utilizando Java Swing para un sistema de ventas comercial.` |
| **Contexto** | `El módulo debe capturar los datos básicos de nuevos clientes (Nombre completo, DNI, Correo electrónico y Teléfono). El sistema requiere almacenar los registros en una lista en memoria y mostrarlos en una tabla (JTable).` |
| **Ejemplo** | `"Cliente [Juan Pérez - DNI: 12345678] registrado correctamente."` |
| **Formato** | `Explica brevemente la estructura de las clases a utilizar y entrega el código organizado en dos clases separadas: Cliente.java (modelo de datos) y FormularioCliente.java (vista y lógica de la interfaz).` |

## Evaluacion del resultado 

| Criterio | Cumple (Sí / No) |
|---|---|
| ¿El código utiliza únicamente bibliotecas nativas de Java Swing sin librerías externas? | Sí |
| ¿Aplica las validaciones solicitadas (DNI de 8 dígitos, formato de correo y no campos vacíos)? | Sí |
| ¿Muestra los errores con ventanas emergentes de `JOptionPane`? | Sí |
| ¿Entrega el código separado en clases (`Cliente.java` y `FormularioCliente.java`)? | Sí |

## Errores que evite

1. **Ser demasiado general (no dar contexto ni restricciones):** En la versión 1 no se especificaron restricciones de negocio, por lo que la IA entregó una aplicación de consola que aceptaba DNIs inválidos o campos vacíos. Se evitó agregando restricciones explícitas de validación (DNI de 8 dígitos y correo con "@").
2. **No indicar el formato de salida:** Al no indicar el formato inicial, la IA colocó toda la lógica en un solo método `main`. Se evitó instruyendo en el prompt final que dividiera el código en dos clases independientes (`Cliente` y `FormularioCliente`).