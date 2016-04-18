
# Definición
Herramienta que permite diseñar interfaces de forma visual generando automáticamente el código fuente de las mismas y estabeciendo un feedback con el mismo; si cambias el código fuente se actualizará lo mostrado por la herramienta.

(Al generar código podemos crear excepciones, por ejemplo si [...] [^1])

---

# Instalación 
1. Help
2. Install new software
3. Seleccionar versión de eclipse en el desplegable o "all available sites"
4. Instalar window builder y swing designer

---

# Uso de la herramienta
Es necesario que exista un proyecto y un paquete

1. Nuevo
2. Other
2. WindowBuilder
3. Swing Designer  
    - Application Window
    - JApplet
    - JDialog
    - JFrame
    - JInternalFrame 
    - JPanel
5. Nombre de la clase
6. Pestaña inferior, Design

---

# Distribución de la pantalla 

4 Paneles principales.

- Barra de herramientas
- Palette
- Structure
    + Components
    + Properties
- Canvas 

---

# Cómo trabaja WindowBuilder
Por defecto todos los objetos se instancian y configuran en un método initialize () que se genera automáticamente.

No se generan constantes, cualquier valor requerido por los constructores de los objetos está codificado en el mismo método

Por defecto los objetos no pertenecen a la clase sino al método. Solo el JFrame principal si es un atributo private de la clase. Esto se modifica mediante a opción field to local / local to field. (EN PROPERTIES)

---

# Barrar de herramientas
- Externalize Strings: Permite independizar todos las strings del código y colocarlas en ficheros aparte, permitiendo el uso de varios idiomas. Genera una clase nueva (con sólo métodos estáticos) y una serie de ficheros con pares clave texto / string en el idioma
- Quickly Test: Permite probar la aplicación sin necesidad de compilar. Esto es útil también para probar únicamente JPanels sin ncesidad de añadirlos a un JFrame
- Layout Assistant: Permite editar el layout del elemento y el del padre de forma sencilla 
- Look-n-feel: Permite cambiar el diseño de la interfaz para aproximarla por ejemplo a la nativa gtk. DA PROBLEMAS

---



---


---



---

# Properties
- Show events: Permite añadir un listener concreto al objeto. Para ello
te lleva al código de la clase habiendo creado una clase anónima que recibe el evento
- Goto definition
- Convert Local / Field: Pasa a considerar un elemento como atributo privado de la clase 
- Show Advanced

Se pueden seleccionar varios elementos del canvas y editarlos de forma conjunta 
- Mismo tipo de elemento: todas las propiedades
- Distintos tipos de elementos: propiedades comunes a ambos

---

# Clic derecho sobre los elementos
- **Morph**, dependiendo del tipo de objeto te permite cambiarlo a otros del mismo tipo o cualquier otra clase
- **Expose component**, genera los getter del elemento (protected o public)
- **Factory**
- **Sorround with** (necesario layout)
- **Set action** Genera una action que el botón es capaz de lanzar
- **Add event handler** igual al de palette

---

## Casos particulares
### Button 
- Crear group buttons y añadirlos

---

# ToDo
[ ] Preferences / WindowBuilder
[ ] Ampliar y darle sentido a las opciones de clic derecho
[ ] Extender en general todos los campos, por ejemplo el de externaliza strings 
[ ] Pensar qué demostraciones en directo vamos a hacer
[ ] Hablar de posibles alternativas tanto para Eclipse como para otros IDEs
[ ] Probar bien la composición teniendo varios elementos gráficos en distintas clases
[ ] Entender las factories

---

# Notas a pie de página 
[^1]: No recuerdo com ose recreaba. Es lo de que el canvas decía que había error en el código tras borrar algo del layout o cambiarlo

Problemas con las refactorizaciones y el uso de otras clases en el frame principal (no actualiza los nombres o directamente los borra)

Pop UP no mola