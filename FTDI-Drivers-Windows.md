El chip FTDI de la *iCEstick* o la *IceZUM Alhambra* tiene dos interfaces de comunicaciones:
* La **Interfaz 0** se utiliza para descargar el bitstream
* La **Interfaz 1** está conectada con la FPGA para permitir la comunicación con una UART sintetizada

![](https://groups.google.com/group/fpga-wars-explorando-el-lado-libre/attach/1b0354d041335/imagen.png?part=0.1&authuser=0)

Al conectar por primera vez la placa a un puerto USB ambas interfaces se configuran como puerto COM:

![](https://groups.google.com/group/fpga-wars-explorando-el-lado-libre/attach/1b0354d041335/imagen.png?part=0.3&authuser=0)

Tras instalar los drivers con [Apio](http://apiodoc.readthedocs.io/en/stable/source/installation.html#install-fpga-ftdi-drivers) o [Icestudio](http://icestudio.readthedocs.io/en/latest/source/quickstart.html#setup-the-drivers) mediante Zadig, la Interfaz 0 debe aparecer como dispositivo libusbK:

![](https://groups.google.com/group/fpga-wars-explorando-el-lado-libre/attach/1b0354d041335/imagen.png?part=0.2&authuser=0)

### Procedimiento si no aparecen los puertos COM

Para hacer funcionar la fpga hay que seguir el **procedimiento estándar**, no influye en el funcionamiento de la fpga que no aparezcan los puertos COM. En caso de querer comunicarse con la fpga mediante el **puerto serie** habrá que realizar los siguientes pasos para hacerlos aparecer. Los pasos que se detallan a continuación se han realizado tras completar el proceso estándar.

Vamos al Administrador de dispositivos > Controladores de bus serie universal > USB Serial Converter B > (Click derecho) Propiedades

![](https://lh3.googleusercontent.com/-vrdV_1npX0M/WXhPXB6R9zI/AAAAAAAAHPg/P_PFcyRGN10MpB1-szZm0QMKIuYd9tVcgCLcBGAs/s1600/puertoscom1.png)

Vamos a la pestaña de Avanzado, activamos la opción Cargar VCP y pulsamos Aceptar.

![](https://lh3.googleusercontent.com/-joxTEN9Q7tI/WXhP0qwU9lI/AAAAAAAAHPk/t-G71x1vIMIU8YJNFJEU64_s12dHjgVygCLcBGAs/s1600/puertoscom2.png)

Desenchufamos y enchufamos la fpga, y ahora nos aparecerá el puerto COM.

![](https://lh3.googleusercontent.com/-SHERYohSK6M/WXhRDLUwAZI/AAAAAAAAHPs/BuAam8EqtcUqtCvrYcCNrN5_sypNZ0nWgCLcBGAs/s1600/puertoscom3.png)

### NOTAS

* Cada vez que la placa se conecte a un **puerto USB nuevo** se deberán **instalar los drivers** para ese puerto.
* Después de configurar los drivers se ha de **desconectar y reconectar la placa**.
* En **Windows 10** con **USB 3.0** puede dar problemas. En tal caso probar:
  * En el administrador de dispositivos buscar el "Dispositivo Compuesto USB" que corresponde a la placa (clic derecho->propiedades->Detalles, en el desplegable buscar "Descripción del dispositivo notificada por el bus". Debe aparecer "IceZUM Alhambra v1.1...". Si es la Icestick pondrá "Lattice FTUSB Interface Cable"
  * Cuando se localiza el dispositivo compuesto que corresponde a la placa, clic derecho->Desinstalar.
  * Desconectar la placa y reiniciar el PC
  * Conectar la placa, se reinstará automáticamente del driver de Microsoft.

### Comunicación con UART (TX y RX) sintetizada en la FPGA

1. Abres el Administrador de dispositivos. (para ir rápido, tecla windows + R, te saldrá la ventanita de ejecutar, ahí escribes "devmgmt.msc")
2. En "Controladoras de bus serie Universal" haces clic con el botón de derecho a "USB Serial Converter B".
3. Propiedades.
4. Pestaña: "Avanzados"
5. Habilitas la casilla "Cargar VCP".
6. Aceptar.
7. Enchufas y desenchufas.
8. Te ha de aparecer el puerto COM nuevo más abajo. En "Puertos (COM y LPT)"

Si te sigue sin aparecer, prueba a enchufar y desenchufar de nuevo.