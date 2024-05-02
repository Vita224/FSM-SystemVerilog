# FSM en SystemVerilog

Máquina de Estados Finitos tipo Mealy.

## Descripción
Se desarrolla un semaforo para este proyecto, el cual debe funcionar dependiendo si tiene carros o no en suc arril, tiene un boton de reset y cuenta con una caracteristica extra que coloca todos los semaforos en rojo, en caso de una emergencia.<br>

## Registro del Development Flow 🚀
Se describe a continuación cada uno de los pasos del Development Flow, analizando los resultados obtenidos.<br>

## 1. RTL Code 
Aquí definimos en el código de nuestro circuito, se realiza la descripción de Hardware en Software dentro de Vivado. Creamos nuestro Design Sources, Constraints y Simulation Sources, para poder realizar los esquemáticos, simulaciones sin placa y por ultimo el cargado del código en nuestra placa Basys 3. En este proceso definimos las entradas, salidas y el clk de frecuencia de nuestro diseño.<br>

![Imagen1](https://github.com/Vita224/FSM-SystemVerilog/assets/53021236/7c87d28c-e5a8-4fa1-808e-80f7eda4e059) <br>
Imagen 1. Vemos los distintos archivos elaborados para nuestro diseño. <br><br>
![Imagen2](https://github.com/Vita224/FSM-SystemVerilog/assets/53021236/483fa536-9402-4dcf-b9b2-191548e6c310)  <br>
Imagen 2. Esquemático de nuestro circuito, podemos ver las compuertas de su diseño.   <br>

## 2. Simulation
Para la simulación se utiliza nuestro Testbench “Simulation Sources”, donde definimos las entradas que tendrá nuestro diseño y corroborar si las salidas están correcta con relación al comportamiento definido. <br>

![Imagen3](https://github.com/Vita224/FSM-SystemVerilog/assets/53021236/b0950a8c-90ed-4b5e-9187-66694e24c9c5)  <br>
Imagen 3. Vemos los pulsos (1 y 0) de nuestras entradas y salidas. <br>

## 3. Synthesis
En esta parte vemos los componentes físicos que nos ayudaran a lograr la función lógica dentro de nuestro FPGA, donde vemos los MUX, Flip flops, Lookup tables y demás componentes necesarios para poder elaborar nuestro circuito. <br>

![Imagen4](https://github.com/Vita224/FSM-SystemVerilog/assets/53021236/11aafeec-7767-47d0-98c0-588cf17e33e5) <br>
Imagen 4. Vemos encendidos los componentes dentro de nuestra FPGA necesarios para el circuito. <br><br>
![Imagen5](https://github.com/Vita224/FSM-SystemVerilog/assets/53021236/d94bdde6-1688-4fad-8b6e-c75b933127d9) <br>
Imagen 5. Se aprecia la diferencia entre los apagados y encendidos. <br><br>
![Imagen6](https://github.com/Vita224/FSM-SystemVerilog/assets/53021236/0a80f469-b667-4840-bdc7-641c0c0215f7) <br>
Imagen 6. Esquemático con los componentes encendidos de nuestra FPGA. <br>

## 4 y 5.	Implementation y Static timing Analysis
Aquí creamos una netlist donde mapeamos las rutas para conectar los componentes físicos para elaborar nuestro diseño. En la imagen podemos ver las conexiones entre los distintos componentes y las lookup tables que tienen. <br>

![Imagen7](https://github.com/Vita224/FSM-SystemVerilog/assets/53021236/bcde87ea-aa82-4d01-9cab-c5d0766e172e) <br>
Imagen 7. Vemos las conexiones entre los componentes dentro de la FPGA. <br><br>
![Imagen8](https://github.com/Vita224/FSM-SystemVerilog/assets/53021236/db2589c7-bdb0-4277-853b-9757abece525) <br>
Imagen 8. Vemos las Lookup tables que definen el comportamiento que tienen entre si los componentes. <br>

## 6. Device Programming 
Por último, seleccionamos “Generate Bitstream” para concerca y cargar el código en nuestra placa para poder realizar las pruebas para lo que vendría siendo el prototipo de nuestro circuito antes de su futura producción. El funcionamiento de aprecia en el video indicado. <br>

![Imagen9](https://github.com/Vita224/FSM-SystemVerilog/assets/53021236/9d73491b-be42-459c-92f6-60f3a8c708f8) <br>
Imagen 9. Se carga código en placa Basys3 para sus pruebas.<br>

## Video de Youtube
Aquí vemos la explicación de elaboración de proyecto y simulación en placa Basys3.<br>
Video : https://www.youtube.com/watch?v=PCk5yyFFD7o<br>

---
Desarrolado por Vitalino Guerra (091-19-1394) 😊




