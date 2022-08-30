# flow1_NodeRed
Repositorio creado para las primeras actividades de NodeRed

## Introducción
El flow 1 (o programa) representa el primer ejercicio a realizar con NodeRed. El ejercicio consiste solo en conectar un nodo Inject con un nodo Debug y automatizarlo para que genere un TimeStamp cada 1 segundo.
## Material necesario
- Ubuntu 20.04
- NodeJS
 - NPM
 - NodeRed

## Referencias
Enlaces de apoyo para las configuraciones:
- [Instalación de Virtual Box y Ubuntu 20.04](https://edu.codigoiot.com/course/view.php?id=812 "nstalación de Virtual Box y Ubuntu 20.04")
- [Instalación de NodeRed](https://edu.codigoiot.com/course/view.php?id=817 "Instalación de NodeRed")
- [Introducción de NodeRed](https://edu.codigoiot.com/course/view.php?id=278 "Introducción de NodeRed")

## Instrucciones
### Requisitos previos
1. **Instalación de NodeJS. **Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM
2. **Instalación de NodeRed.**La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2

### Intrucciones de preparación del entorno
1. Arrancar NodeRed con el comando `node-red`
2. Importar el flow desde el repositorio
3. Hacer clic en el boton Deploy

### Intrucciones primer flow
Para observar el resutlado de este flow, sólo es necesario abrir la pestaña Debug.
### Instrucciones segundo flow

1. Clonar el flow
2. Configurar el nodo Inject para mandar el timestamp cada 1 segundo
3. Agregamos un nodo función que convierta el timestamp en fecha legible
	Código función:
		// Crea un objeto Date a partir del payload enviado por timestamp
		var date = new Date(msg.payload);
		// Cambia el payload para que sea una fecha con formato
		msg.payload = date.toString();
		// Regresa el mensaje para que se envíe al sigueinte nodo
		return msg;

### Instrucciones tercer flow

1. Clonar el flow 2
2. Agregamos los nodos dashboard
3. Mandamos el resultado del nodo función al dashboard
4. Dirigirse al dashboard en http://localhost:1880/ui

### Resultados y Evidencias
**Flow 1**
![](https://github.com/HilarioBarcenas/flow1_NodeRed/blob/main/Flow1.png?raw=true)

**Flow 2**
![](https://github.com/HilarioBarcenas/flow1_NodeRed/blob/main/Flow2.png?raw=true)

**Flow 3**
![](https://github.com/HilarioBarcenas/flow1_NodeRed/blob/main/Flow3-1.png?raw=true)
![](https://github.com/HilarioBarcenas/flow1_NodeRed/blob/main/Flow3-2.png?raw=true)

### Créditos
**Desarrollado por **`Hilario Barcenas`