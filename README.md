# Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams
Creación de una Logic App en Azure que permita identificar cuando se ha creado un nuevo Tweet con un Hashtag establecido, analizarlo y registrarlo en una hoja de cálculo de google y postear el contenido en teams


![Logo de Logic Apps](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/Logicapp.jpg)     ![Logo de Twitter](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/twitter.jpg)
![Logo de Gsheets](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/Gsheets.jpg)   ![Logo de teams](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/teams.jpg)

## Requisitos

- Cuenta de [Azure](https://portal.azure.com/) con suscripción activa
- Cuenta de [Twitter](https://twitter.com/). Si no se tiene, es necesario seguir las instrucciones en el sitio para crear una nueva cuenta con su e-mail.
- Cuenta de [Google Drive](https://drive.google.com/). Si no se tiene, es necesario seguir las instrucciones en el sitio para crear una nueva cuenta de gmail y tener acceso.
- Computadora con Windows, Linux o MacOs.

---------------------------------------------------------

## Pasos

1. Se inicia sesión en la página de [Azure](https://portal.azure.com/)

![Inicio Azure](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/inicio%20Azure.PNG)

2. Se busca "Logic Apps" y se presiona enter

![P8-1](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-1.PNG)

3. Se presiona el botón "Agregar"

![P8-2](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-2.PNG)

4. En el apartado de grupo de recursos, se da click en "crear nuevo", luego se le da un nombre y se presiona "aceptar"

![P8-3](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-3.PNG)

5. Se la da un nombre, se selecciona la región y se selecciona el tipo de plan "consumo"

![P8-4](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-4.PNG)

6. Redundancia de zona deshabilitada y prsionamos "revisar y crear"

![P8-5](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-5.PNG)

7. Esperamos a que se valide la configuración y se habilite el botón de "crear". Se presiona el botón "crear"

![P8-6](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-6.PNG)

8. Se comenzará con la creación del recurso. Una vez termine se mostrará la siguiente pestaña donde presionamos "ir al recurso"

![P8-8](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-8.PNG)

9. Se mostrará una pantalla como la siguiente:

![P8-9](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-9.PNG)

10. Bajamos un poco sobre la misma pestaña y seleccionamos la opción mostrada en la imagen:

![P8-10](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-10.PNG)

11. Se abrirá una pestaña como la siguiente, presionamos en "iniciar sesión"

![P8-11](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-11.PNG)

12. Nos mostrará una ventana como la siguiente donde debemos colocar un nombre para la conexión y después presionamos "iniciar sesión"

![P8-12](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-12.PNG)

13. No abrirá otra ventan donde debemos iniciar sesión con nuestra cuenta de Twitter

14. Después de iniciar sesión en Twitter nos regresará a la siguiente ventana, presionamos ""continuar"

![P8-13](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-13.PNG)

15. Abrirá otro apartado como el siguiente, donde se debe colocar el texto de búsqueda (en este caso un hashtag) y la frecuencia de comprobación. Al temrinar se da click en "nuevo paso"

![P8-14](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-14.PNG)

16. Abrirá otro apartado como el siguiente, donde debemos buscar "sentimientos" en la barra de búsqueda y seleccionar la opción mostrada en la imagen

![P8-15](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-15.PNG)

17. Se abrirá un apartado como el siguiente

![P8-16](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-16.PNG)

18. Se abre otra pestaña del navegador y se ingresa de nuevo a [Azure](https://portal.azure.com/)

19. En la barra superior de búsqueda se busca "cognitive services" y se selecciona la opión mostrada en la imagen

![P8-17](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-17.PNG)

20. Si es la primera vez que se va a crear un cognitive services, prosiga con el siguiente paso, en caso contrario, salte hasta el paso 28

21. Baje sobre la pestaña derecha de coginitive services hasta encontrar "Cuenta de varios servidores de cognitive services" y se presiona en "crear"

![P8-18](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-18.PNG)

22. En el grupo de recursos se selecciona el que creamos anteriormente y se selecciona la región

![P8-19](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-19.PNG)

23. Más abajo se coloca el nombre, se selecciona el plan de tarifa y se marca de casilla de "términos y condiciones" y se da click en "revisar y crear"

![P8-20](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-20.PNG)

24. Esperamos a que termine la validación y una vez se habilite el botón de "crear" se presiona.

![P8-21](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-21.PNG)

25. Nos mostrará una ventana que indica que esta en proceso de implementación

![P8-22](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-22.PNG)

26. Una vez temrinada la implementació se mostrará una ventana como la siguiente:

![P8-23](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-23.PNG)

27. Se busca en la parte superior de la página "cognitive services" y se selecciona la opción que se muestra a continuación:

![P8-24](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-24.PNG)

28. En el apartado "servicio de lenguaje" se selecciona "crear"

![P8-25](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-25.PNG)

29. En la siguiente ventana se selecciona "continuar con la creación del recurso"

![P8-26](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-26.PNG)

30. En el apartado "grupo de recursos" se selecciona "crear nuevo", se le coloca un nombre y se presiona "aceptar"

![P8-27](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-27.PNG)

31. Más abajo se selecciona la región, se le coloca un nombre y se selecciona el plan de tarifa "FREE". Después se selecciona "revisar y crear".

![P8-28](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-28.PNG)

32. En la siguiente pestaña se espera que se valide la configuración y se habilite el botón de "crear". Se presiona y se mostrará una ventana como la siguiente:

![P8-29](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-29.PNG)

33. Una vez termine, se mostrará un mensaje como el siguiente, se presiona "ir al recurso"

![P8-30](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-30.PNG)

34. Se abrirá una nueva pestaña, en el menú laterla izquierdo se navega hasta encontrar el apartado de "claves y puntos de conexión" y se da click.

![P8-31](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-31.PNG)

35. Se copia la clave 1, como se muestra en la imagen:

![P8-32](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-32.PNG)

36. Se regresa a la otra pestaña del navegador y se pega en el apartado de "clave de cuenta"

![P8-33](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-33.PNG)

37. Se cambia de pestaña en el navegador de nuevo y ahora se copia la URL del apartado "extremo" como se muestra en la imagen:

![P8-34](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-34.PNG)

38. Se cambia de pestaña en el navegador y se pega en el apartado "URL del sitio"

![P8-35](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-35.PNG)

39. Se presiona el botón "crear"

![P8-36](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-36.PNG)

40. Se da click en el apartado "id documento" y en la ventana que se abrirá a la derecha se busca "id" en la barra de búsqueda y se selecciona la opción que se muestra en la imagen:

![P8-37](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-37.PNG)

41. Se da click en el apartado "texto del documento" y en la ventana que se abrirá a la derecha se busca "texto del tweet" en la barra de búsqueda y se selecciona la opción que se muestra en la imagen:

![P8-38](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-38.PNG)

42. Después se abre otra pestaña del navegador, se accede a [Google Drive](https://drive.google.com/), y se crea una nueva hoja de cálculo como la siguiente:

![P8-39](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-39.PNG)

43. Después se vuelve a la pestaña del navegador de la logic App y se presiona en "Nuevo paso"

![P8-40](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-40.PNG)

44. En la barra de búsqueda del apartado "Elija una operación" se escribe "sheets" y se selecciona la opción que se muestra en la imagen:

![P8-41](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-41.PNG)

45. En el submenú que se abre se selecciona "insertar fila"

![P8-42](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-42.PNG)

46. Después se mostrará un menú como el siguiente, se presiona "iniciar sesión"

![P8-43](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-43.PNG)

47. Nos redigirá a otra pestaña donde se debe iniciar sesión con su cuenta de google y después se cerrará automáticamente

48. En el apartado "archivo" se da click en el ícono de carpeta y se desplegará otro menú donde debemos buscar el archivo de hoja de cálculo que se creó anteriormente y se da click en él

![P8-44](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-44.PNG)

49. Si al hacer click en el partado de "hoja de cálculo" se muesta el siguiente error, 

![P8-45](https://github.com/AlanAlvaradoR/Azure-Logic-App-para-registrar-Twitts-en-GSheets-y-postear-teams/blob/main/imagenes/P8-45.PNG)

50. 







