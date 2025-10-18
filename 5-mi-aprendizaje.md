# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.

Consultar: Cómo se gestionan datos confidenciales con los secretos de Docker (Docker Secrets).
Docker Secrets es una funcionalidad de Docker que permite gestionar datos confidenciales, como contraseñas, certificados o claves API, de forma segura dentro de contenedores y servicios. Los secretos se almacenan cifrados en los nodos manager del clúster Docker Swarm y solo pueden ser accedidos por los servicios autorizados. En lugar de exponer información sensible en variables de entorno, Docker inyecta los secretos como archivos temporales dentro del contenedor, ubicados en el directorio /run/secrets/, accesibles únicamente por el proceso correspondiente. Esto garantiza un manejo seguro, centralizado y aislado de la información sensible, evitando filtraciones y manteniendo la integridad de los datos confidenciales.
