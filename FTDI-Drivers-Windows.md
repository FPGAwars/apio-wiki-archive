El chip FTDI de la *iCEstick* o la *IceZUM Alhambra* tienen dos interfaces de comunicaciones:
* La **Interfaz 0** se utiliza para descargar el bitstream
* La **Interfaz 1** está conectada con la FPGA para permitir la comunicación con una UART sintetizada

![](https://groups.google.com/group/fpga-wars-explorando-el-lado-libre/attach/1b0354d041335/imagen.png?part=0.1&authuser=0)

Al conectar por primera vez la placa a un puerto USB ambas interfaces se configuran como puerto COM:

![](https://groups.google.com/group/fpga-wars-explorando-el-lado-libre/attach/1b0354d041335/imagen.png?part=0.3&authuser=0)

Tras instalar los drivers con [Apio](http://apiodoc.readthedocs.io/en/stable/source/installation.html#install-fpga-ftdi-drivers) o [Icestudio](http://icestudio.readthedocs.io/en/latest/source/quickstart.html#setup-the-drivers) mediante Zadig, la Interfaz 0 debe aparecer como dispositivo libusbK:

![](https://groups.google.com/group/fpga-wars-explorando-el-lado-libre/attach/1b0354d041335/imagen.png?part=0.2&authuser=0)

### NOTAS

* Cada vez que la placa se conecte a un **puerto USB nuevo** se deberán **instalar los drivers** para ese puerto.
* Después de configurar los drivers se ha de **desconectar y reconectar la placa**.
* En **Windows 10** con **USB 3.0** suele dar problemas. En tal caso probar:
  * En el administrador de dispositivos buscar el "Dispositivo Compuesto USB" que corresponde a la placa (clic derecho->propiedades->Detalles, en el desplegable buscar "Descripción del dispositivo notificada por el bus". Debe aparecer "IceZUM Alhambra v1.1...". Si es la Icestick pondrá "Lattice FTUSB Interface Cable"
  * Cuando se localiza el dispositivo compuesto que corresponde a la placa, clic derecho->Desinstalar.
  * Desconectar la placa y reiniciar el PC
  * Conectar la placa, se reinstará automáticamente del driver de Microsoft.
