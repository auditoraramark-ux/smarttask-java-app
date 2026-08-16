## Descripción
Esta es una aplicación de consola desarrollada en Java utilizando Maven. Su objetivo es gestionar tareas personales, permitiendo clasificarlas en tareas normales y urgentes, realizar un seguimiento de su estado (activa/completada), asignación dinámica y secuencial de identificadores únicos, así como operaciones de eliminación.

## Cómo compilar
Para compilar el proyecto y descargar todas las dependencias necesarias de Maven, ejecute el siguiente comando en la raíz del directorio:
```bash
mvn clean compile
```

## Cómo ejecutar
Para lanzar y desplegar la aplicación de consola interactiva, ejecute:
```bash
mvn exec:java -Dexec.mainClass="com.smarttask.Main"
```
Para correr el set de pruebas unitarias automatizadas:
```bash
mvn test
```

## Estructura de clases
*   **com.smarttask.model.Tarea**: Clase base abstractiva de datos que encapsula el `id`, `nombre` y estado `completado`.
*   **com.smarttask.model.TareaNormal**: Subclase de Tarea que sobrescribe el comportamiento textual formateado agregando el tag `[NORMAL]`.
*   **com.smarttask.model.TareaUrgente**: Subclase de Tarea que incorpora la métrica temporal `diasLimite` junto a la lógica de caducidad `estaVencida()`.
*   **com.smarttask.service.Accionable**: Interfaz de servicio funcional que prescribe el contrato de operaciones de gestión requeridas.
*   **com.smarttask.service.GestorTareas**: Motor del servicio que implementa `Accionable`, centralizando el almacenamiento temporal y el autoincremento controlado de IDs sin reciclaje.

## Enlace al repositorio
[https://github.com](https://github.com)
