# Proyectos C# — Validaciones, MDI y Juego de Craps

Colección de tres aplicaciones en C# desarrolladas con Visual Studio. Cada programa está en su propia carpeta, con su proyecto y su solución, para poder abrirlo y ejecutarlo de forma independiente.

## Estructura

```
Proyectos_CSharp/
├── Problema 1 - Validaciones/
│   └── EjemploGrid/          Formulario con validaciones y tabla (DataGridView)
├── Problema 2 - MDI/
│   └── FormularioMDI/        Formulario contenedor MDI con ventana hija
└── Problema 3 - Juego de Craps/
    └── Craps/                Juego de dados en consola
```

## Requisitos

- **Visual Studio** 2022 o superior, con la carga de trabajo **Desarrollo de escritorio con .NET**.
- **.NET Framework 4.7.2** (paquete de destino) para los problemas 1 y 2.
- **.NET 10 SDK** para el juego de craps (problema 3).

## Cómo ejecutar cada programa

1. Descarga o clona el repositorio.
2. Abre la solución de la carpeta del programa que quieras (`.slnx`).
3. Si el proyecto aparece con error de bloqueo de Windows, desbloquea los archivos (clic derecho sobre la carpeta > Propiedades, o con PowerShell: `Get-ChildItem -Recurse | Unblock-File`).
4. Presiona **F5** para ejecutar.

Para abrir el diseñador de un formulario, haz clic derecho sobre `Form1.cs` (o `Form2.cs`) > **Ver diseñador**.

## Problema 1 — Validaciones (EjemploGrid)

Formulario para registrar colaboradores. Antes de agregar un registro a la tabla, valida:

- **ID de empleado:** obligatorio y numérico.
- **Nombres** y **apellidos:** obligatorios.
- **Email:** formato válido (debe contener `@` y un dominio con punto).
- **Salario:** número decimal válido.

Si un campo no cumple, se marca con un mensaje de error y el cursor se coloca en ese campo. Los datos válidos se agregan a la tabla y el formulario se limpia.

Archivos principales: `Form1.cs`, `Utilidades.cs` (validación de correo) y `Persona.cs` (modelo).

## Problema 2 — MDI (FormularioMDI)

Aplicación de interfaz de documentos múltiples (MDI):

- El formulario principal (`Form1`) es el contenedor, con una barra de herramientas.
- Al hacer clic en el botón de la barra se abre una ventana hija (`formVentanaText`) dentro del contenedor.

Archivos principales: `Form1.cs` y `Form2.cs`.

## Problema 3 — Juego de Craps (Craps)

Simulación en consola del juego de dados craps:

- **Primer tiro:** 7 u 11 gana; 2, 3 o 12 pierde; cualquier otro número se convierte en el *punto*.
- **Tiros siguientes:** se gana si se repite el punto y se pierde si sale 7 antes.

Archivos principales: `Craps.cs` (lógica del juego) y `Program.cs` (punto de entrada).

## Notas

- Las carpetas `bin/`, `obj/` y `.vs/` se generan al compilar y no están incluidas en el repositorio.
- Proyecto de autoría propia para práctica académica.
