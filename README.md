# <a name="_wqoikhl3tzzb"></a>**Documentación de la Aplicación Art Space**
## <a name="_s51mhwheua4g"></a>**Introducción**
La aplicación **Art Space** permite a los usuarios visualizar diversas imágenes de obras icónicas junto con sus descripciones. Los usuarios pueden navegar entre las imágenes utilizando los botones **"Anterior"** y **"Siguiente"**, además de contar con la opción de cerrar la aplicación.

![](Aspose.Words.61da1fca-b7e1-48e1-9f57-d8e9ddc2a9e6.001.png)
![Aspose Words 2f26bc27-d001-4cba-9eed-676758c88830 001](https://github.com/user-attachments/assets/264608f2-70e8-43dc-8f9d-d3c2b7bf5db2)

##
## <a name="_tonff1l2kzn6"></a><a name="_brqn4997o259"></a><a name="_cmbgxle4t4n"></a>**Descripción del Código**
La aplicación está construida en **Jetpack Compose**, utilizando un diseño basado en una columna con elementos de UI bien estructurados.
### <a name="_cztvmn4aqgq2"></a>**MainActivity**
![](Aspose.Words.61da1fca-b7e1-48e1-9f57-d8e9ddc2a9e6.002.png)
![Aspose Words 2f26bc27-d001-4cba-9eed-676758c88830 002](https://github.com/user-attachments/assets/c504d1ac-df1e-4530-a33c-7622c801d5dd)

Esta clase representa la actividad principal de la aplicación, donde se define la interfaz de usuario llamando a la función composable **ArtSpaceScreen()**.
<a name="_2z35ydx8ura5"></a>En el método **onCreate()**, establece el contenido con la función:
**setContent { ArtSpaceScreen(activity = this) }**
-----------------------------------------------------------------------------------------------
### <a name="_qyvq2lalunay"></a>Esto significa que se mostrará la interfaz de **ArtSpaceScreen.**
###
###
###
###
###
###
###
###
###
###
### <a name="_9qxov7wynud3"></a><a name="_il6hm9aq4wg7"></a><a name="_4vyjckugwoqd"></a><a name="_ugk1bw2cy45q"></a><a name="_rqib2qmb9rrc"></a><a name="_48d90maj8kk5"></a><a name="_60smox6lxxv7"></a><a name="_9u5lul25hngd"></a><a name="_4614ug21r8ta"></a><a name="_y6w43jhabwc3"></a><a name="_fqyg14f138qf"></a>**Función Composable ArtSpaceScreen**
![](Aspose.Words.61da1fca-b7e1-48e1-9f57-d8e9ddc2a9e6.003.png)
![Aspose Words 2f26bc27-d001-4cba-9eed-676758c88830 003](https://github.com/user-attachments/assets/e748bc91-3324-4a0c-b90c-0d4c50b666fe)

Esta función define la interfaz de usuario que muestra las imágenes y permite la navegación entre ellas. Contiene una lista de imágenes y descripciones.

Se usa **remember { mutableStateOf(0) }** para manejar el índice actual de la imagen.

Muestra la imagen actual con **Image(painter = painterResource(id=images[currentIndex])).**

Incluye botones para la navegación:

**"Anterior":** Retrocede en la lista.

**"Siguiente":** Avanza en la lista.

**"Cerrar":** Cierra la aplicación.


![](Aspose.Words.61da1fca-b7e1-48e1-9f57-d8e9ddc2a9e6.004.png)![](Aspose.Words.61da1fca-b7e1-48e1-9f57-d8e9ddc2a9e6.005.png)
![Aspose Words 2f26bc27-d001-4cba-9eed-676758c88830 004](https://github.com/user-attachments/assets/c646d77a-7b0c-455d-be6c-81d356c57afb)

![](Aspose.Words.61da1fca-b7e1-48e1-9f57-d8e9ddc2a9e6.006.png)
![Aspose Words 2f26bc27-d001-4cba-9eed-676758c88830 005](https://github.com/user-attachments/assets/b383b2f0-0c85-4bfd-9576-3e1140658e3e)
![Aspose Words 2f26bc27-d001-4cba-9eed-676758c88830 006](https://github.com/user-attachments/assets/753d12f9-fd17-4b9c-92a4-c3c1ad3655a3)

## <a name="_n492o0ora1yx"></a>
## <a name="_y9gs4x5eyiiw"></a>**Tests Realizados**
Se han desarrollado pruebas tanto de UI como unitarias para garantizar el correcto funcionamiento de la aplicación.
### <a name="_ixy5z7c8h8ua"></a>**Pruebas de UI**
Las pruebas de UI se implementan utilizando composeTestRule y verifican que los botones funcionan correctamente.
![](Aspose.Words.61da1fca-b7e1-48e1-9f57-d8e9ddc2a9e6.007.png)
![Aspose Words 2f26bc27-d001-4cba-9eed-676758c88830 007](https://github.com/user-attachments/assets/004819b4-cafb-40ce-9099-2db82a9c51f9)

<a name="_363bud9n4hng"></a>**testLaunchApp():** Comprueba que la pantalla inicial muestra la primera imagen y el nombre del autor.

**testNextButtonChangesImage():** Simula un clic en "Siguiente" y verifica que la imagen cambie.

**testPreviousButtonChangesImage():** Simula un clic en "Anterior" y verifica que la imagen cambie.

**testCloseButton():** Simula un clic en "Cerrar" y comprueba que la actividad se cierre correctamente.

###
###
###
###
###
###
###
###
###
###
###
###
###
###
###
###
### <a name="_4v85r56266xn"></a><a name="_2r6dtwzf25da"></a><a name="_5q1v1686k2z6"></a><a name="_a0j3k4ggwkgo"></a><a name="_2o5kfmh0hopn"></a><a name="_dvlspenqbc1u"></a><a name="_ybcdrbk6uhuf"></a><a name="_jn30c4kdnatf"></a><a name="_cf16mxy0jk04"></a><a name="_pizgygzhb6ez"></a><a name="_ts6rymrdwmig"></a><a name="_6olkfw3j78ib"></a><a name="_26extl1byqvw"></a><a name="_5hnnwe1h1u3x"></a><a name="_60ksk92zyo4o"></a><a name="_cvm1ryaeh683"></a><a name="_s068oz625wzz"></a>**Pruebas Unitarias**
Se han desarrollado pruebas unitarias para garantizar el comportamiento esperado de la lógica de cambio de imágenes.![](Aspose.Words.61da1fca-b7e1-48e1-9f57-d8e9ddc2a9e6.008.png)
![Aspose Words 2f26bc27-d001-4cba-9eed-676758c88830 008](https://github.com/user-attachments/assets/cb48447a-76fa-44f2-9b3a-399365640e1c)



Estas pruebas validan la navegación cíclica entre las imágenes.

**testNextImage():** Verifica que al presionar "Siguiente", el índice aumenta correctamente.

**testPreviousImage():** Verifica que al presionar "Anterior", el índice disminuye correctamente.

**testLoopNextImage():** Verifica que si la imagen actual es la última, al presionar "Siguiente" vuelve a la primera.

**testLoopPreviousImage():** Verifica que si la imagen actual es la primera, al presionar "Anterior", cambia a la última.

## <a name="_zbg612t5l71t"></a>**Conclusión**
La aplicación **Art Space** ofrece una experiencia sencilla pero efectiva para visualizar imágenes de obras icónicas. A través de pruebas de UI y unitarias, se ha asegurado su correcto funcionamiento, cumpliendo con los requisitos esperados.

## <a name="_3obnjdydgyp6"></a>**Futuras versiones**

Para futuras versiones se planea que se puedan subir imágenes o borrarlas, también que se puedan compartir dichas imagenes.
