

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

![image](https://user-images.githubusercontent.com/88836525/134454949-cb940eba-dd04-4c13-8d19-f2378417e2de.png)

![image](https://user-images.githubusercontent.com/88836525/134454968-4e5587e0-f9f6-4425-85de-8b04c5b63b7e.png)
![image](https://user-images.githubusercontent.com/88836525/134454975-4a530148-5dce-4e21-be2f-5d46cb394b7b.png)
