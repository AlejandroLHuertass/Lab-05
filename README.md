# LABORATORIO 5 - MVC PRIMEFACES INTRODUCTION - 2021-2

## PARTE I. - JUGANDO A SER UN CLIENTE HTTP

![image](https://user-images.githubusercontent.com/88836525/134589947-50962de7-841e-4eba-923f-e447784667e3.png)
![image](https://user-images.githubusercontent.com/88836525/134589971-a1482ee7-6b70-4505-b089-379f771dbce4.png)
![image](https://user-images.githubusercontent.com/88836525/134589995-2219c697-abc2-4274-8e5c-cf1ca2c5399f.png)


¿Qué otros códigos de error existen?, ¿En qué caso se manejarán?

1: Respuestas informativas

2: Peticiones correctas

3: Redirecciones

4: Errores del cliente

5: Errores de servidor
¿Cuál es la diferencia entre los verbos GET y POST? ¿Qué otros tipos de peticiones existen?

GET El método GET solicita una representación de un recurso específico. Las peticiones que usan el método GET sólo deben recuperar datos. HEAD El método HEAD pide una respuesta idéntica a la de una petición GET, pero sin el cuerpo de la respuesta. POST El método POST se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor. PUT El modo PUT reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.

DELETE El método DELETE borra un recurso en específico. CONNECT El método CONNECT establece un túnel hacia el servidor identificado por el recurso.

OPTIONS El método OPTIONS es utilizado para describir las opciones de comunicación para el recurso de destino. TRACE El método TRACE realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino.

PATCH El método PATCH es utilizado para aplicar modificaciones parciales a un recurso.

¿Cuáles son las diferencias con los diferentes parámetros?

-v, --verbose Hacer que la operación sea más comunicativa -i, --include Incluir encabezados de respuesta de protocolo en la salida

![image](https://user-images.githubusercontent.com/88836525/134590016-22551153-e8fe-414c-a210-877c13313d3c.png)
![image](https://user-images.githubusercontent.com/88836525/134590045-ce8d7b5c-0f93-40b3-9f8c-6ff0ad1ce263.png)
![image](https://user-images.githubusercontent.com/88836525/134590072-e6f21cf3-9167-44b7-97ea-e87fce7be093.png)


## PARTE II. - HACIENDO UNA APLICACIÓN WEB DINÁMICA A BAJO NIVEL.

I. Para esto, cree un proyecto maven nuevo usando el arquetipo de aplicación Web estándar maven-archetype-webapp y realice lo siguiente:
![image](https://user-images.githubusercontent.com/88836525/134454695-3b2d31a3-a35b-4e9d-ad99-ca2a87660c97.png)
![image](https://user-images.githubusercontent.com/88836525/134454722-3e592204-1f24-49e2-9799-b9b1a868f9f5.png)

Observe que el Servlet ‘SampleServlet’ acepta peticiones GET, y opcionalmente, lee el parámetro ‘name’. Ingrese la misma URL, pero ahora agregando un parámetro GET (si no sabe como hacerlo, revise la documentación en http://www.w3schools.com/tags/ref_httpmethods.asp).

![image](https://user-images.githubusercontent.com/88836525/134454811-adca36af-a7bb-471c-bed2-5cda67982306.png)
![image](https://user-images.githubusercontent.com/88836525/134454820-3601a266-c243-48e4-9aa0-3ea1aba6113e.png)




Observe que el Servlet ‘SampleServlet’ acepta peticiones GET, y opcionalmente, lee el parámetro ‘name’. Ingrese la misma URL, pero ahora agregando un parámetro GET (si no sabe como hacerlo, revise la documentación en http://www.w3schools.com/tags/ref_httpmethods.asp).

Busque el artefacto gson en el repositorio de maven y agregue la dependencia.

![image](https://user-images.githubusercontent.com/88836525/134454841-ebc90dc9-238b-4733-a1da-1d921d264358.png)


En el navegador revise la dirección https://jsonplaceholder.typicode.com/todos/1. Intente cambiando diferentes números al final del path de la url.
![image](https://user-images.githubusercontent.com/88836525/134454861-51d509ee-6ac3-4065-a01e-b6fd9ccdb5f5.png)
![image](https://user-images.githubusercontent.com/88836525/134454872-a8db3424-d89f-475b-bfdc-b803ffba0046.png)
![image](https://user-images.githubusercontent.com/88836525/134454881-7c34b21a-aae7-4e0a-b817-af4e0e1e358d.png)


Basado en la respuesta que le da el servicio del punto anterior, cree la clase edu.eci.cvds.servlet.model.Todo con un constructor vacío y los métodos getter y setter para las propiedades de los "To Dos" que se encuentran en la url indicada.

![image](https://user-images.githubusercontent.com/88836525/134454908-b6e50373-e906-4a31-addf-090186e68bb1.png)


Utilice la siguiente clase para consumir el servicio que se encuentra en la dirección url del punto anterior:

eniendo en cuenta las siguientes métodos disponibles en los objetos ServletRequest y ServletResponse recibidos por el método doGet:

![image](https://user-images.githubusercontent.com/88836525/134454949-cb940eba-dd04-4c13-8d19-f2378417e2de.png)

![image](https://user-images.githubusercontent.com/88836525/134454968-4e5587e0-f9f6-4425-85de-8b04c5b63b7e.png)
![image](https://user-images.githubusercontent.com/88836525/134454975-4a530148-5dce-4e21-be2f-5d46cb394b7b.png)

Intente hacer diferentes consultas desde un navegador Web para probar las diferentes funcionalidades.
![image](https://user-images.githubusercontent.com/88836525/134455279-426598f8-d6df-492b-a3e0-19e663ab4197.png)


## PARTE III.
En su servlet, sobreescriba el método doPost, y haga la misma implementación del doGet.
Cree el archivo index.html en el directorio src/main/webapp/index.html de la siguiente manera:

<!DOCTYPE html>
<html>
    <head>
        <title>Start Page</title>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    </head>
    <body>
        <h1>Hello World!</h1>
    </body>
</html>
En la página anterior, cree un formulario que tenga un campo para ingresar un número (si no ha manejado html antes, revise http://www.w3schools.com/html/ ) y un botón. El formulario debe usar como método ‘POST’, y como acción, la ruta relativa del último servlet creado (es decir la URL pero excluyendo ‘http://localhost:8080/’).

Revise este ejemplo de validación de formularios con javascript y agruéguelo a su formulario, de manera que -al momento de hacer ‘submit’- desde el browser se valide que el valor ingresado es un valor numérico.

Recompile y ejecute la aplicación. Abra en su navegador en la página del formulario, y rectifique que la página hecha anteriormente sea mostrada. Ingrese los datos y verifique los resultados. Cambie el formulario para que ahora en lugar de POST, use el método GET . Qué diferencia observa?

¿Qué se está viendo? Revise cómo están implementados los métodos de la clase Service.java para entender el funcionamiento interno.

