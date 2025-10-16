# formaciononline
Esbozo de web de formación. Proyecto para DAW.


## 1. Fundamentos del sistema
Objetivos del sistema:  

En primer lugar el proyecto debe contar con un servicio de gestión de base de datos (GBD) que respalde los contenidos que se van mostrar a los usuarios, almacenar las cuentas de los usuarios y sus contraseñas. 
Para este tipo de tarea se requiere de un software específico como mysql, postgres o similar. 
Al mismo tiempo los progresos de los alumnos deben ser registrados a través de un ERP dentro de la web para que puedan consultar su calendario, tareas pendientes, etc. 
El administrador (tutor o profesor) debe tener acceso a un servicio similar pero con características ampliadas (mayor nivel de privilegios).

El contenido debe mostrarse a través de una web interactiva que ofrezca todos los servicios. 
La parte más importante del servicio es el contenido educativo se explicará más adelante algunas características concernientes a su licencia.

Dentro de las características descriptivas en las que se enmarca la empresa podríamos ubicarla dentro del grupo de Entretenimiento. Esta clasificación es compleja, una definición alternativa podría ser la de plataforma, una plataforma es un espacio donde múltiples agentes utilizan un mismo canal de distribución de sus productos obteniendo ventajas de alcance (mayor número de clientes/usuarios a los que llegar).



## 2. Análisis y especificación de requisitos
Información sobre la especificación de requisitos acordada entre los clientes y el equipo.  


Funcionales:  

* Nuestra startup (servicio online de recursos de aprendizaje para usuarios y centro de formación) necesita una web que sirva como plataforma para mostrar los contenidos.  
* Requiere de un registro de usuario y diferentes roles en función de si se trata de un profesor o de un alumno.  
* Algunos usuarios pueden adjuntar contenidos como libros y otros materiales  
* Se deberá mostrar un informe de evaluación del alumno similar a un CRM.  
* Deberán existir servicios de evaluación, como test o juegos para mejorar la retención del usuario y su aprendizaje.  

No funcionales:  

* Nuestra plataforma deberá ser implementada por un equipo de desarrollo lo suficientemente capacitado.  
* Al mismo tiempo deberá ser lo suficientemente intuitiva y atractiva para que el usuario pueda permanecer en la plataforma y no desertar de sus estudios.  
* La plataforma debe tener un servicio de almacenamiento (backend) para almacenar todos los contenidos, tales como claves cifradas y respaldo de documentos a través de una base de datos.  
* Se fomentará el aprendizaje autónomo a través de estrategias de economía conductual como por ejemplo Nudge Theory.  
* Todo debe ser conforme a la ley vigente.  
    

## 3. Diseño
Añadir aquí lo relacionado con el diseño y técnicas descriptivas que fuimos creando


## 4. Implementación
Añade aquí aunque no tenga que ver con el proyecto, los ejercicios donde tuviste que corregir el código "feo"
```
**
* Clase Operaciones matematicas
*
* Contiene funciones sumar, restar, multiplicar, dividir
*
* @author Alumno de DAW
* @version 1.0
*/
public class Calculadora {
// Este método suma dos números
public int sumar(int x, int y){
return x+y;
}
// Este método resta dos números
public int restar(int x, int y){
return x-y;
}
// Este método multiplica dos números
public int multiplicar(int x, int y){
return x*y;
}
// Este método divide dos números
public int dividir(int x, int y){
return x/y;
}
public static void main(String[] args){
Calculadora c=new Calculadora();
System.out.println("resultado: "+c.sumar(5,3));
}
}
```

## 5. Plan de pruebas del sistema
Añade aquí lo que hicimos para diseñar las pruebas


### 5.1. Pruebas de aceptación
Nada por aquí 
Prueba 1. El profesor de un curso sube un libro de solo lectura para los alumnos el sistema debe
verificar que solo los usuarios seleccionados pueden ver el contenido.
| Tipo de prueba | Entrada / acción | Resultado |
|-----|-----|-----|
| Funcional | Usuario administrador del curso sube material en pdf de solo lectura | El sistema evalúa que los roles de los usuarios “alumnos” tienen permiso de lectura y que pertenecen todos al mismo curso |
| Funcional / Negativa | Usuario administrador del curso oculta un material a los alumnos | El sistema retira los permisos de lectura del material a los usuarios “alumnos“. El material permanecerá oculto |


Prueba 2. El usuario realiza un test de evaluación y comprueba su nota al finalizar, el sistema mostrará la nota final del test y cuántas preguntas ha errado.  
| Tipo de prueba | Entrada / acción | Resultado |
|-----|-----|-----|
| Funcional | Usuario aprueba un test y comprueba su nota | El sistema felicita al alumno por sus conocimientos, se muestra un reporte de fallos al finalizar el test |
| Funcional / Negativa | Usuario suspende el test y comprueba su nota | El sistema anima al alumno a repasar conceptos, se muestran los fallos cometido y las lecciones que debe revisar para superar la prueba |

## 7. Los diccionarios de datos
