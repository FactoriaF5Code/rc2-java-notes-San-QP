# Instalación
[Fuente: Notion RuralCamp II 4.0.](https://chrome-ravioli-2d4.notion.site/4-0-Setup-de-Java-con-Visual-Studio-Code-bcebccf6c46f45afb7a29c0b0439053f)

- ¿Qué versión de Java tengo?: `java -version`
- ¿Dónde tengo instalado Java?: `(Get-Command java).Path`

## Instalación con Jabba
### 1. CÓMO INSTALAR JABBA
JABBA es una herramienta que simplifica la instalación y gestión de múltiples versiones de Java en un sistema. Facilita la configuración del entorno de desarrollo y el cambio entre versiones de Java de manera eficiente.
[Fuente: jvmaware.com](https://jvmaware.com/multiple-java-versions/)

Lanzar el siguiente comando en PowerShel COMO ADMINISTRADOR. ( *Botón derecho > Ejecutar como administrador* )
~~~
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
Invoke-Expression (
  Invoke-WebRequest https://github.com/shyiko/jabba/raw/master/install.ps1 -UseBasicParsing
).Content
~~~

### 2. CÓMO INSTALAR JAVA
~~~
# fetch and install openjdk versions available in the remote repo
jabba ls-remote | grep "openjdk"
jabba install openjdk@1.15.0
~~~

## Instalación cruda
- Descargar de [openJDK](https://openjdk.org/) el zip de la versión que se requiere.
- Para gestionar varias versiones de Java, crear una `carpeta openJDK` donde guardar cada una y descomprimirla.
- Copiar la ruta de la carpeta.
- Abrir `Variables de entorno` en nuestro sistema
- En `Variables del sistema` crear una variable JAVA_HOME:
~~~
Nombre: JAVA_HOME
Valor: ruta de la carpeta.
~~~
- Editar la variable `Path` en `Variables de usuario`. Botón NUEVO y añadir `%JAVA_HOME%\bin`