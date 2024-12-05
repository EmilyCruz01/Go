# Simulador de Concurrencia en Go con Fyne

El lenguaje Go es conocido por su eficiente manejo de concurrencia mediante goroutines y canales. En combinación con la biblioteca Fyne, es posible crear interfaces gráficas que permitan visualizar y comprender cómo funcionan los procesos concurrentes en tiempo real. Este enfoque es especialmente útil para enseñar conceptos como sincronización, bloqueo y acceso a recursos compartidos.
Yo realicé un simulador interactivo desarrollado con Fyne que muestra cómo varios "trabajadores" (goroutines) realizan tareas en paralelo, actualizando en tiempo real, en el proceso de hacer el simulador con la librería Fyne me econtré con que debes cumplir varios requerimientos para instalar fyne en la carpeta de tu proyecto  poder hechar a andar un proyecto con esta librería.

## Requisitos

Antes de comenzar, asegúrate de cumplir con los siguientes requisitos:

1. **Instalar Go**  
   Descarga e instala Go desde su [sitio oficial](https://go.dev/dl/).

2. **Descargar Fyne**  
   Ejecuta el siguiente comando en la carpeta de tu proyecto:
   ```bash
   go get fyne.io/fyne/v2

3. **Instalar un compilador C (solo en Windows)**

Si eres usuario de Windows, necesitarás realizar algunos pasos adicionales:

- **Instalar MinGW**: Descárgalo desde [este enlace](https://sourceforge.net/projects/mingw/).  
- **Instalar MSYS2**: Descárgalo desde [su sitio oficial](https://www.msys2.org/).  

Una vez instalado **MSYS2**, abre la terminal de MSYS2 y ejecuta los siguientes comandos:

  ```bash
  pacman -Syu
  Para instalar el compilador GCC:
  pacman -S mingw-w64-x86_64-gcc
  Para instalar las dependencias necesarias para Fyne:
  pacman -S mingw-w64-x86_64-glfw mingw-w64-x86_64-mesa mingw-w64-x86_64-pkg-config

Después es necesario entrar a la cosola de MinGW64 de MSYS2 y instalar go export PATH=$PATH:/c/tu-ruta-a-go/bin
dar cd ruta-a-tu-proyecto  y así estarás listo para usar la librería Fyne. 


