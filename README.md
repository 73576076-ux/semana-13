# Semana 13 — Diseño de Interfaces Gráficas (GUI) con Tkinter

**Curso:** Construcción de Software  
**Institución:** Universidad Continental  
**Docente:** Ing. Henderson Nozart Gibaja Reyes  

## Descripción del Proyecto
Este repositorio contiene el desarrollo de dos aplicaciones de escritorio creadas en Python utilizando la biblioteca estándar **Tkinter**, aplicando principios fundamentales de diseño de interfaces, usabilidad, accesibilidad y programación orientada a objetos.

---

## Estructura del Repositorio
* `calculadora.py`: Calculadora básica con operaciones aritméticas (`+`, `-`, `*`, `/`), limpieza de pantalla (`C`) y manejo controlado de excepciones.
* `formulario.py`: Formulario de registro de usuario con validación completa de campos y retroalimentación visual.
* `wireframe.png`: Boceto inicial de baja fidelidad que define la estructura visual del formulario de registro.
* `captura_calculadora.png` / `captura_formulario.png`: Evidencias de ejecución de ambas interfaces.

---

## Principios de Usabilidad y Accesibilidad Aplicados

### 1. Organización Visual y Jerarquía (`grid()`)
* Se utilizó el gestor de diseño `grid()` para alinear las etiquetas a la derecha (`sticky="e"`) junto a sus respectivos campos de entrada (`sticky="w"`), facilitando la lectura rápida y la asociación visual entre etiqueta y campo.
* Se aplicaron márgenes internos y externos (`padx`, `pady`) para evitar la saturación visual y mejorar la legibilidad.

### 2. Prevención de Errores y Retroalimentación Clara
* **Validación integral:** Antes de procesar el registro, el sistema verifica campos vacíos, formato válido de correo electrónico mediante expresiones regulares (`re`), longitud mínima de contraseña (8 caracteres), coincidencia de contraseñas, rango numérico de edad (15 a 99 años), selección de género y aceptación de términos.
* **Mensajes descriptivos:** Mediante `messagebox.showerror`, se listan todos los errores detectados en un solo cuadro de diálogo claro para que el usuario sepa exactamente qué corregir.
* **Confirmación de éxito:** Al completar correctamente el formulario, se muestra un mensaje personalizado de bienvenida (`messagebox.showinfo`).

### 3. Privacidad y Accesibilidad
* **Campos ocultos:** Los campos de *Contraseña* y *Confirmar contraseña* utilizan el atributo `show="*"` para proteger la privacidad del usuario al digitar.
* **Navegación por teclado (Tab Order):** El orden secuencial de creación de los `Entry`, `Radiobutton`, `Checkbutton` y `Button` permite recorrer todo el formulario usando únicamente la tecla `Tab`.
* **Contraste y diferenciación de acciones:** El botón principal **Registrar** destaca en color verde (`#4CAF50`) con texto blanco para guiar la acción principal, diferenciándose visualmente del botón secundario **Limpiar**.

---

## Ejecución del Proyecto
Asegúrate de tener Python 3 instalado y ejecuta desde la terminal:

```bash
python calculadora.py
python formulario.py
```
