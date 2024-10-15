# ParcialSoftware
Estudiar mucho
# Sistema de Reservas de Canchas de Fútbol

## Descripción
Este proyecto implementa un sistema para la gestión de reservas de canchas de fútbol. Permite a los usuarios realizar reservas, elegir diferentes tipos de canchas y seleccionar métodos de pago. El sistema valida las reservas y proporciona información detallada sobre cada cancha.

## Tecnologías Utilizadas
- Java
- NetBeans (IDE)
- Patrón de diseño Factory Method

## Instrucciones de Instalación
1. Asegúrate de tener [Java JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) instalado en tu sistema.
2. Descarga e instala [NetBeans](https://netbeans.apache.org/) si aún no lo tienes.
3. Clona este repositorio o descarga los archivos del proyecto.

   ```bash
   git clone https://github.com/tu_usuario/nombre_del_repositorio.git

##Casos de Prueba
El sistema incluye varios casos de prueba para verificar su funcionalidad. Al ejecutar el programa, se probarán los siguientes escenarios:

##Caso de prueba 1: Reserva válida con tarjeta.
##Caso de prueba 2: Reserva de cancha no válida.
##Caso de prueba 3: Reserva válida con pago en efectivo.
##Caso de prueba 4: Reserva sin método de pago.

##Caso de Prueba 1: Reserva válida con tarjeta
Descripción: Se realiza una reserva válida para una cancha de fútbol sala utilizando un pago con tarjeta.
Entrada:
Cliente: Fraison Zúñiga
Cancha: Fútbol Sala
Método de Pago: Tarjeta
Resultado Esperado:
Reserva realizada con éxito.
Se imprime la información de la reserva.
Se procesa el pago con tarjeta.

// Ejemplo de ejecución
Cliente cliente1 = new Cliente("Fraison Zúñiga");
Cancha canchaFutbolSala = new FutbolSala();
Reserva reserva1 = new Reserva(cliente1, canchaFutbolSala);
reserva1.realizarReserva(new PagoTarjeta());



##Caso de Prueba 2: Reserva de cancha no válida
Descripción: Se intenta realizar una reserva para una cancha que no existe.
Entrada:
Cliente: Fraison Zúñiga
Cancha: null (cancha no válida)
Resultado Esperado:
Se muestra un mensaje de error indicando que la cancha no es válida.

// Ejemplo de ejecución
Cancha canchaInvalida = null; // Cancha no válida
Reserva reservaInvalida = new Reserva(cliente1, canchaInvalida);
reservaInvalida.realizarReserva(new PagoTarjeta());



##Caso de Prueba 3: Reserva válida con pago en efectivo
Descripción: Se realiza una reserva válida para una cancha de fútbol 7 utilizando un pago en efectivo.
Entrada:
Cliente: Fraison Zúñiga
Cancha: Fútbol 7
Método de Pago: Efectivo
Resultado Esperado:
Reserva realizada con éxito.
Se imprime la información de la reserva.
Se procesa el pago en efectivo.

// Ejemplo de ejecución
Cancha canchaFutbol7 = new Futbol7();
Reserva reserva2 = new Reserva(cliente1, canchaFutbol7);
reserva2.realizarReserva(new PagoEfectivo());



##Caso de Prueba 4: Reserva sin método de pago
Descripción: Se intenta realizar una reserva sin especificar un método de pago.
Entrada:
Cliente: Fraison Zúñiga
Cancha: Fútbol 11
Método de Pago: null
Resultado Esperado:
Se muestra un mensaje de error indicando que no se puede realizar la reserva sin un método de pago válido.

// Ejemplo de ejecución
Cancha canchaFutbol11 = new Futbol11();
Reserva reservaSinPago = new Reserva(cliente1, canchaFutbol11);
reservaSinPago.realizarReserva(null); // Sin método de pago

