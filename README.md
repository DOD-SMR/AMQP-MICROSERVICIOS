En este proyecto hemos creado un microservicio intermediario utilizando RabbitMQ, node y express para esta práctica hemos seguido estos pasos:

1. Crear un contenedor docker con la imagen de RabbitMQ

2. Inicializar un proyecto node con node init -y

3. Crear un producer.js que se encargue de recibir las peticiones

4. Crear un consumer.js que se encargue de tratar las peticiones y confirmarlas

5. Iniciamos consumer y producer con el comando node <archivo>

6. Probar con 10 peticiones para comprobar el servidor, para hacerlo escribimos el siguiente comando en powershell  => 1..10 | ForEach-Object { Invoke-RestMethod -Uri "http://localhost:3000/comprar" -Method Post -ContentType "application/json" -Body (@{ id=101; producto="Teclado"; email="alumno@escuela.com" } | ConvertTo-Json) }

7. Probamos a inicializar varios consumers y ver como trabajan de manera concurrente para responder a las peticiones
