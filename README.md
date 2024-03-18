# Recursion_server
Algoritmo Recursivo Servidor

El proyecto es un sistema médico que permite realizar diversas operaciones, como hacer citas, ver citas, buscar pacientes, registrar nuevos pacientes y modificar o cancelar citas. Está diseñado para funcionar en un entorno de red utilizando WebSockets para la comunicación entre un cliente y un servidor.

 Las funcionalidades del proyecto:

Hacer Cita: Permite a los usuarios programar nuevas citas proporcionando su nombre, número de cédula y número de teléfono.

Ver Citas: Muestra la lista de citas programadas en el sistema.

Buscar Paciente: Permite buscar un paciente por su nombre completo o parte de él. La búsqueda es recursiva, lo que significa que si el nombre proporcionado coincide con varios pacientes, se mostrarán todos los resultados que comiencen con ese nombre.

Registrar Nuevo Paciente: Permite registrar un nuevo paciente en el sistema proporcionando su nombre.

Modificar/Cancelar Citas: Permite al usuario modificar o cancelar una cita existente proporcionando el número de cita correspondiente.

El proyecto utiliza programación asíncrona para manejar las solicitudes de los clientes y está diseñado para funcionar en una arquitectura cliente-servidor, donde el servidor actúa como el punto central para gestionar las operaciones del sistema médico.

Se puede:
El algoritmo aplicado en la función BuscarPacienteRecursivo se encarga de buscar pacientes cuyos nombres coincidan con un prefijo dado de manera eficiente en una lista ordenada de pacientes. Aquí está cómo funciona el algoritmo:

Divide y vencerás: El algoritmo utiliza un enfoque de "divide y vencerás" para buscar en la lista de pacientes. En cada iteración, divide la lista en mitades y busca en la mitad correcta basándose en el valor del nombre del paciente en el punto medio de la lista.

Recursión: La función BuscarPacienteRecursivo es recursiva. Comienza con una llamada inicial pasando la lista completa de pacientes. Luego, en cada paso recursivo, divide la lista en mitades y realiza la búsqueda solo en una de las mitades, basándose en si el nombre del paciente en el punto medio de la lista es menor o mayor que el prefijo dado.

Ordenamiento de la lista: Antes de realizar la búsqueda, la lista de pacientes se ordena alfabéticamente. Esto permite que el algoritmo realice búsquedas eficientes utilizando una técnica conocida como "búsqueda binaria".

Comparación de prefijos: En cada paso recursivo, el algoritmo compara el prefijo dado con el nombre del paciente en el punto medio de la lista. Si el nombre del paciente comienza con el prefijo dado, se agrega a la lista de resultados.

Ordenación de los resultados: Después de encontrar todas las coincidencias, la lista de resultados se ordena alfabéticamente utilizando el método Sort(). Esto garantiza que los resultados devueltos estén en orden alfabético.

Modificación para Búsqueda de Prefijo: En nuestro caso, en lugar de buscar un valor exacto, estamos buscando todos los nombres de pacientes que comienzan con un cierto prefijo (en este caso, el nombre completo del paciente). Por lo tanto, la modificación que hicimos al algoritmo de búsqueda binaria es que cuando encontramos un paciente cuyo nombre comienza con el prefijo dado, lo agregamos a una lista de resultados en lugar de devolverlo inmediatamente. Luego continuamos la búsqueda binaria en ambas mitades de la lista original para encontrar más coincidencias.

Recursión: La función BuscarPacienteRecursivo se llama recursivamente en ambas mitades de la lista original según el resultado de la comparación del paciente medio con el prefijo dado. Esto permite buscar en la lista completa de manera eficiente mientras se mantiene la propiedad de orden de la lista.

