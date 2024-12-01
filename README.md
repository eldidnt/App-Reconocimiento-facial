# Sistema de Seguridad de Reconocimiento Facial

Este proyecto es una aplicación de seguridad que utiliza reconocimiento facial para verificar si las personas que se encuentran en el campo de visión de la cámara están registradas. Si se detecta a un rostro desconocido, el sistema envía automáticamente un correo con la imagen del rostro capturado.

## Requisitos

Antes de usar la aplicación, asegúrate de tener instalados los siguientes requisitos:

- **Python 3.x**  
  Puedes descargar Python desde su [sitio web oficial](https://www.python.org/downloads/).
  
- **Librerías necesarias**  
  Usa el siguiente comando para instalar las librerías necesarias:
  ```bash
  pip install opencv-python opencv-python-headless numpy pillow smtplib  
  ```
- **Archivo Haar Cascade**
  El archivo Haar Cascade (haarcascade_frontalface_default.xml) se utiliza para la detección de rostros. Puedes descargarlo desde el repositorio oficial de OpenCV [aquí](https://github.com/opencv/opencv/tree/master/data/haarcascades).

## Descripción del Proyecto

Esta aplicación proporciona un sistema de vigilancia basado en reconocimiento facial utilizando la cámara web. El sistema permite registrar rostros, verificar rostros desconocidos y enviar notificaciones por correo electrónico si se detecta una persona no registrada.

### Características principales:
* **Registro de rostros:** Puedes registrar nuevos rostros ingresando un nombre para asociarlo con la imagen capturada.
* **Verificación en tiempo real:** El sistema verifica los rostros detectados en tiempo real y los compara con los registrados.
* **Notificaciones por correo:** Si se detecta un rostro desconocido, el sistema enviará automáticamente un correo con la imagen del rostro capturado.

## Cómo Usar la Aplicación

### 1. Ejecutar el Sistema
Para iniciar la aplicación, ejecuta el archivo Python principal. En la terminal, navega hasta el directorio donde se encuentra el archivo app.py y ejecuta:

```bash
python app.py
```
Esto abrirá una ventana de la interfaz gráfica donde podrás interactuar con el sistema.

### 2. Registrar Nuevos Rostros
Para registrar un nuevo rostro, haz lo siguiente:

* Haz clic en el botón "Registrar Nuevo Rostro" en la interfaz.
* Se abrirá una nueva ventana con la cámara en vivo.
* Escribe un nombre para el nuevo rostro en el campo correspondiente.
* Haz clic en "Guardar". El rostro será capturado y guardado en la carpeta `assets/` asociada con el nombre que proporcionaste.

### 3. Activar el Sistema de Vigilancia
* Haz clic en el botón "Activar Sistema" en la interfaz principal.
* El sistema comenzará a verificar los rostros detectados en la cámara en tiempo real.
* Si se detecta un rostro registrado, se mostrará el nombre del mismo.
* Si se detecta un rostro desconocido, se mostrará "¡DESCONOCIDO!" y el sistema enviará automáticamente un correo con * la imagen del rostro capturado.

### 4. Desactivar el Sistema de Vigilancia
Si deseas desactivar el sistema de vigilancia:

* Haz clic en el botón "Desactivar Sistema".
* El sistema dejará de verificar rostros hasta que lo reactives nuevamente.

### 5. Recibir Notificaciones por Correo
Si se detecta un rostro desconocido, el sistema enviará automáticamente un correo a la dirección configurada con la imagen capturada del rostro. Para configurar el correo, deberás editar la sección de Configuración de correo en el código fuente.

**Configuración de Correo:**
En el archivo app.py, edita las siguientes variables con tus credenciales y el destinatario del correo:

```python
remitente = "tucorreo@gmail.com"
destinatario = "correo_destino@gmail.com"
contraseña = "tu_contraseña_o_contraseña_de_aplicación"
smtp_server = 'smtp.gmail.com'
smtp_port = 587
```

**Importante:** Si usas una cuenta de Gmail y tienes habilitada la verificación en dos pasos (2FA), necesitarás crear una contraseña de aplicación desde tu cuenta de Google, en lugar de utilizar tu contraseña regular.














