#Ultimate Vocal Remover GUI v5.5.1
<img src="https://raw.githubusercontent.com/Anjok07/ultimatevocalremovergui/master/gui_data/img/UVR_5_5_1.png?raw=true" />

[![Lanzamiento](https://img.shields.io/github/release/anjok07/ultimatevocalremovergui.svg)](https://github.com/anjok07/ultimatevocalremovergui/releases/latest)
[![Descargas](https://img.shields.io/github/downloads/anjok07/ultimatevocalremovergui/total.svg)](https://github.com/anjok07/ultimatevocalremovergui/releases)

## Acerca de

Esta aplicación utiliza modelos de separación de fuentes de última generación para eliminar las voces de los archivos de audio. Los desarrolladores principales de UVR entrenaron todos los modelos provistos en este paquete (excepto los modelos de 4 vástagos Demucs v3 y v4).

- **Desarrolladores principales**
     - [Anjok07](https://github.com/anjok07)
     - [aufr33](https://github.com/aufr33)

- **Apoya el Proyecto**
     - [Donar](https://www.buymeacoffee.com/uvr5)

## Instalación

Estos paquetes contienen la interfaz UVR, Python, PyTorch y otras dependencias necesarias para ejecutar la aplicación de manera efectiva. No se requieren requisitos previos.

### Instalación de Windows

- Tenga en cuenta:
     - Este instalador está destinado a aquellos que ejecutan Windows 10 o superior.
     - No se garantiza la funcionalidad de la aplicación para sistemas que ejecutan Windows 7 o inferior.
     - No se garantiza la funcionalidad de la aplicación para los sistemas de CPU Intel Pentium y Celeron.
     - Debe instalar UVR en la unidad principal C:\. La instalación de UVR en una unidad secundaria provocará inestabilidad.

- Descargue el instalador UVR para Windows a través del siguiente enlace:
     - [Enlace de descarga principal](https://github.com/Anjok07/ultimatevocalremovergui/releases/download/v5.5.0/UVR_v5.5.1_setup.exe)
     - [Espejo de enlace de descarga principal] (https://www.mediafire.com/file_premium/j8hkuvbic6nqy7i/UVR_v5.5.1_setup.exe/file)
- Instrucciones del paquete de actualización para aquellos que ya tienen UVR instalado:
     - Si ya tienes instalado UVR puedes instalar este paquete sobre él o descargarlo directamente desde la aplicación.

<detalles id="WindowsManual">
   <summary>Instalación manual de Windows</summary>

### Instalación manual de Windows

- Descarga y extrae el repositorio [aquí](https://github.com/Anjok07/ultimatevocalremovergui/archive/refs/heads/master.zip)
- Descargue e instale Python [aquí] (https://www.python.org/ftp/python/3.9.8/python-3.9.8-amd64.exe)
    - Asegúrese de marcar "Agregar python.exe a PATH" durante la instalación
- Ejecute los siguientes comandos desde el directorio del repositorio extraído:

```
python.exe -m pip install -r requisitos.txt
```

Si tiene una GPU Nvidia compatible, ejecute el siguiente comando:

```
python.exe -m pip install --upgrade torch --extra-index-url https://download.pytorch.org/whl/cu117
```

Si no tiene instalado FFmpeg o Rubber Band y desea evitar pasar por el largo proceso de instalación, siga las instrucciones a continuación.

**Instalación de FFmpeg**

- Descargue la compilación precompilada [aquí] (https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.zip)
- Del archivo, extraiga el siguiente archivo al directorio de la aplicación UVR:
    - ```ffmpeg-5.1.2-essentials_build/bin/ffmpeg.exe```

**Instalación de banda elástica**

Para usar la herramienta Time Stretch o Change Pitch, necesitarás una banda elástica.

- Descargue la compilación precompilada [aquí] (https://breakfastquay.com/files/releases/rubberband-3.1.2-gpl-executable-windows.zip)
- Del archivo, extraiga los siguientes archivos al directorio de la aplicación UVR:
    - ```rubberband-3.1.2-gpl-ejecutable-windows/rubberband.exe```
    - ```rubberband-3.1.2-gpl-ejecutable-windows/sndfile.dll```

</detalles>

### Instalación de Mac OS

- Tenga en cuenta:
     - Este paquete está diseñado para aquellos que ejecutan macOS Catalina y superior.
     - No se garantiza la funcionalidad de la aplicación para sistemas que ejecutan macOS Mojave o inferior.
     - No se garantiza la funcionalidad de la aplicación para sistemas Mac más antiguos o económicos.
     - Una vez que todo esté instalado, la aplicación puede tardar entre 5 y 10 minutos en iniciarse por primera vez (dependiendo de su Macbook).
    
- Descargue el archivo UVR dmg para MacOS a través de uno de los siguientes enlaces:
     - Usuarios de Mac M1 (arm64):
        - [Enlace de descarga principal](https://github.com/Anjok07/ultimatevocalremovergui/releases/download/v5.5.0/Ultimate_Vocal_Remover_v5_5_MacOS_arm64.dmg)
        - [Espejo de enlace de descarga principal] (https://www.mediafire.com/file_premium/o0tfneebhqw554e/Ultimate_Vocal_Remover_v5_5_MacOS_arm64.dmg/file)

     - Usuarios de Mac Intel (x86_64):
        - [Enlace de descarga principal](https://github.com/Anjok07/ultimatevocalremovergui/releases/download/v5.5.0/Ultimate_Vocal_Remover_v5_5_MacOS_x86_64.dmg)
        - [Reflejo del enlace de descarga principal] (https://www.mediafire.com/file_premium/m19wucslk9uzpcc/Ultimate_Vocal_Remover_v5_5_MacOS_x86_64.dmg/file)

<detalles id="No se puede abrir">
   <summary>Usuarios de MacOS: ¿Tienen problemas para abrir UVR?</summary>

> Debido a la estricta seguridad de las aplicaciones de Apple, es posible que deba seguir estos pasos para abrir UVR.
>
> Primero, ejecute el siguiente comando a través de Terminal.app para permitir que las aplicaciones se ejecuten desde todas las fuentes (se recomienda
terminó que vuelva a habilitar esto una vez que UVR se abra correctamente).
>
> ```bash
> sudo spctl --master-disable
> ```
>
> En segundo lugar, ejecute el siguiente comando para evitar la notarización:
>
> ```bash
> sudo xattr -rd com.apple.quarantine /Aplicaciones/Ultimate\ Vocal\ Remover.app
> ```

</detalles>

<detalles id="MacInstall">
   <summary>Instalación manual de MacOS</summary>

### Instalación manual de MacOS

- Descarga y guarda este repositorio [aquí](https://github.com/Anjok07/ultimatevocalremovergui/archive/refs/heads/master.zip)
- Descargue e instale Python 3.10 [aquí](https://www.python.org/ftp/python/3.10.9/python-3.10.9-macos11.pkg)
- Desde el directorio guardado ejecuta lo siguiente -

```
pip3 install -r requisitos.txt
```

- Si su Mac se ejecuta con un M1, ejecute el siguiente comando a continuación. Si no, omita este paso. -

```
cp /Library/Frameworks/Python.framework/Versions/3.10/lib/python3.10/site-packages/_soundfile_data/libsndfile_arm64.dylib /Library/Frameworks/Python.framework/Versions/3.10/lib/python3.10/site- paquetes/_soundfile_data/libsndfile.dylib
```

**Instalación de FFmpeg**

- Una vez que todo haya terminado con la instalación, descargue el binario FFmpeg correcto para su sistema [aquí] (http://www.osxexperts.net) y colóquelo en el directorio principal de la aplicación.

**Instalación de banda elástica**

Para usar la herramienta Time Stretch o Change Pitch, necesitarás una banda elástica.

- Descargue la compilación precompilada [aquí] (https://breakfastquay.com/files/releases/rubberband-3.1.2-gpl-executable-windows.zip)
- Del archivo, extraiga los siguientes archivos al directorio de la aplicación UVR/lib_v5:
    - ```rubberband-3.1.2-gpl-ejecutable-macos/rubberband```

Este proceso ha sido probado en una MacBook Pro 2021 (usando M1) y una MacBook Air 2017 y se confirma que funciona en ambas.

</detalles>

### Instalación de Linux

<detalles id="LinuxInstall">
   <summary>Consulte las instrucciones de instalación de Linux</summary>

<br />
    
**Estas instrucciones de instalación son para Ubuntu 22.10.**

- Descarga y guarda este repositorio [aquí](https://github.com/Anjok07/ultimatevocalremovergui/archive/refs/heads/master.zip)
- Desde el directorio guardado, ejecute los siguientes comandos en este orden-

```
actualización de sudo apt && actualización de sudo apt
sudo apt-obtener actualización
sudo apt instalar ffmpeg
sudo apt instalar python3-pip
sudo apt-get -y install python3-tk
pip3 install -r requisitos.txt
```

</detalles>

### Otras notas de aplicación

- Nvidia RTX 1060 6GB es el requisito mínimo para las conversiones de GPU.
- Se recomiendan GPU Nvidia con al menos 8 GB de V-RAM.
- Las GPU AMD Radeon no son compatibles en este momento.
- Esta aplicación solo es compatible con plataformas de 64 bits.
- Esta aplicación se basa en la biblioteca de bandas elásticas para las opciones Time-Stretch y Pitch-Shift.
- Esta aplicación se basa en FFmpeg para procesar archivos de audio no wav.
- La aplicación recordará automáticamente su configuración cuando se cierre.
- Los tiempos de conversión dependerán significativamente de su hardware.
- Estos modelos son computacionalmente intensivos.

## Registro de cambios

### Cambios más recientes:
- Se corrigió el problema de la lista de modelos del Centro de descargas.
- Clip de audio fijo en modo conjunto.
- Se corrigió el problema del nombre del modelo de salida en el modo conjunto.
- Se agregó "Modo por lotes" para MDX-Net para aumentar el rendimiento.
   - El modo por lotes es más eficiente en memoria.
   - El modo por lotes produce la mejor salida, independientemente del tamaño del lote.
- Se agregó el modo por lotes para la arquitectura VR.
- Modo Mezclador agregado para Demucs.
   - Esta opción puede mejorar la separación para algunos modelos de 4 vástagos.

### Correcciones y cambios que van de UVR v5.4 a v5.5:

- La barra de progreso ahora está completamente sincronizada con cada proceso en la aplicación.
- La función de arrastrar y soltar ahora debería funcionar siempre.
- Los usuarios ahora pueden colocar grandes lotes de archivos y directorios como entradas. Cuando se eliminan los directorios, la aplicación buscará cualquier archivo con una extensión de audio y lo agregará a la lista de entradas.
- Icono fijo de baja resolución.
- Se agregó la capacidad de descargar modelos manualmente si la aplicación no puede conectarse a Internet.
- Varias correcciones de errores para el Centro de descargas.
- Varios cambios de diseño.

### Actuación:

- Los tiempos de carga del modelo son más rápidos.
- La importación/exportación de archivos de audio es más rápida.

### Nuevas opciones:

- Opción "Seleccionar configuración guardada": permite al usuario guardar la configuración actual de toda la aplicación. También puede cargar configuraciones guardadas o restablecerlas a los valores predeterminados.
- Menú "clic derecho" - Permite un acceso rápido a opciones importantes.
- Opción "Consejos de ayuda": cuando está habilitada, los usuarios pueden pasar el cursor sobre las opciones para ver el texto emergente que describe esa opción. La opción de hacer clic derecho también permite copiar el texto "Sugerencia de ayuda".
- Modo de modelo secundario: esta opción es una versión ampliada de la opción "Modelo Demucs" solo disponible para MDX-Net. Excepto ahora, esta opción está disponible en las tres AI Networks y para cualquier vástago. Cualquier modelo ahora puede ser secundario y el usuario puede elegir la cantidad de influencia que tiene en el resultado final.
- Almacenamiento en caché robusto para el modo de conjunto, lo que permite tiempos de procesamiento mucho más rápidos.
- Al hacer clic en el campo "Entrada", aparecerá una nueva ventana que t permite al usuario pasar por todas las entradas de audio seleccionadas. Dentro de este menú, los usuarios pueden:
     - Eliminar entradas.
     - Verificar entradas.
     - Crear muestras de insumos seleccionados.
- Opción "Modo de muestra": permite al usuario procesar solo una parte de una pista para muestrear configuraciones o un modelo sin ejecutar una conversión completa.
     - El número entre paréntesis es el número actual de segundos que tendrá la muestra generada.
     - Puede elegir la cantidad de segundos para extraer de la pista en el menú "Configuración adicional".

### Arquitectura de realidad virtual:

- Posibilidad de alternar "Procesamiento de gama alta".
- Soporte para la última arquitectura VR
     - Tamaño de recorte y Tamaño de lote son específicamente para modelos que usan la arquitectura más reciente únicamente.

### MDX-RED:

- La opción "Salida de eliminación de ruido" da como resultado resultados más limpios, pero el tiempo de procesamiento será más largo. Esta opción ha reemplazado a la reducción de ruido.
- La opción "Spectral Inversion" utiliza técnicas de inversión espectral para obtener un resultado de tallo secundario más limpio. Esta opción puede ralentizar el proceso de exportación de audio.
- El vástago secundario ahora tiene el mismo corte de frecuencia que el vástago principal.

### Demucs:

- Los modelos Demucs v4 ahora son compatibles, incluido el modelo de 6 vástagos.
- Combinar los tallos restantes en lugar de invertir el tallo seleccionado con la mezcla solo cuando un usuario no selecciona "Todos los tallos".
- Un modelo de "Pre-proceso" que permite al usuario ejecutar una inferencia a través de un modelo vocal o instrumental robusto y separar los tallos restantes de su mezcla instrumental generada. Esta opción puede reducir significativamente el sangrado vocal en otras raíces no vocales generadas por Demucs.
   - El modelo de preproceso está diseñado para separaciones de Demucs para todos los temas, excepto voces e instrumentales.

### Modo conjunto:

- El modo Conjunto se ha ampliado para incluir lo siguiente:
     - "Averaging" es un nuevo algoritmo que promedia los resultados finales.
     - Modelos ilimitados en el conjunto.
     - Posibilidad de guardar diferentes conjuntos.
     - Capacidad para ensamblar salidas para todos los tipos de tallos individuales.
     - Capacidad para elegir algoritmos de conjunto únicos.
     - Posibilidad de ensamblar los 4 tallos Demucs a la vez.

## Solución de problemas

### Problemas comunes

- Si FFmpeg no está instalado, la aplicación arrojará un error si el usuario intenta convertir un archivo que no sea WAV.
- Los errores de asignación de memoria generalmente se pueden resolver al reducir el "Tamaño del fragmento".

### Informe de problemas

Sea lo más detallado posible cuando publique un nuevo problema.

Si es posible, haga clic en el botón "Configuración" a la izquierda del botón "Iniciar procesamiento" y haga clic en el botón "Registro de errores" para obtener información detallada sobre errores que se nos puede proporcionar.

## Licencia

El código GUI de **Ultimate Vocal Remover** es [con licencia MIT] (LICENCIA).

- **Tenga en cuenta:** Para todos los desarrolladores de aplicaciones de terceros que deseen utilizar nuestros modelos, respete la licencia MIT proporcionando crédito a UVR y sus desarrolladores.

## Créditos

- [DilanBoskan](https://github.com/DilanBoskan) - Sus contribuciones al inicio de este proyecto fueron esenciales para el éxito de UVR. ¡Gracias!
- [Bas Curtiz](https://www.youtube.com/user/bascurtiz) - Diseñé el logo, ícono, banner y pantalla de bienvenida oficial de la UVR.
- [tsurumeso](https://github.com/tsurumeso) - Desarrolló el código original de VR Architecture.
- [Kuielab & Woosung Choi](https://github.com/kuielab) - Desarrolló el código AI original de MDX-Net.
- [Adefossez & Demucs](https://github.com/facebookresearch/demucs) - Desarrolló el código original de IA de Demucs.
- [KimberleyJSN](https://github.com/KimberleyJensen) - Asesoró y ayudó en la implementación de los scripts de capacitación para MDX-Net y Demucs. ¡Gracias!
- [Hv](https://github.com/NaJeongMo/Colab-for-MDX_B) - Ayudó a implementar fragmentos en el código MDX-Net AI. ¡Gracias!

## Contribuyendo

- Para cualquier persona interesada en el desarrollo continuo de **Ultimate Vocal Remover GUI**, envíenos una solicitud de extracción y la revisaremos.
- Este proyecto es 100% de código abierto y gratuito para que cualquiera pueda usarlo y modificarlo como desee.
- Solo mantenemos el desarrollo y el soporte para la GUI de **Ultimate Vocal Remover** y los modelos proporcionados.

## Referencias
- [1] Takahashi et al., "DenseNets multibanda y multiescala para la separación de fuentes de audio", https://arxiv.org/pdf/1706.09588.pdf
