**MultiSistemas GPS App Services Documentation**
----
  _A continuacion se muestra de forma general cada uno de los servicios creados para la aplicación móvil GPS MULTISISTEMAS , se incluye toda la información necesaria para hacer las consultas correspondientes._

**Servicios**
----
| Titulo      | Inicio de Sesión  | 
| :------------ |:---------------    | 
| URL         | `/gps/login`   |
| Metodo      | **GET**             |
| Parametros  | `codigo[string]*`    |
|             | `password[string]*`     | 
| Success Response | `{token:***********,is_signup:true}`  |
| Error Response | `{error_msg':'Faltan Parametros Obligatorios}`  |
|                | `{error_msg:'Asegurate que el codigo y la contraseña correctos',is_signup:false}`  |
|                | `{error_msg:'Contraseña incorrecta',is_signup:false}`  |

_*Parametro obligatorio_

| Titulo      | Información General  |
| :------------ |:---------------    |
| URL         | `/gps/infoGeneral`   |
| Metodo      | **GET**             |
| Parametros  | `token[string]*`    |
| Success Response | `{"usuario":"----","grupo":"---","sitios":[{"nombre":"--","id":-},{"nombre":"--","id":-}],"qtyVehiculos":--}`  |
| Error Response | `{error_msg':'Faltan Parametros Obligatorios}`  |
|                | `{error_msg:'Token Incorrecto'}`  |
|                | `{error_msg:'Ha ocurrido un error, intenta de nuevo'}`  |

_*Parametro obligatorio_

| Titulo      | Busqueda por Placa  |
| :------------ |:---------------    |
| URL         | `/gps/filtroPlacas`   |
| Metodo      | **GET**             |
| Parametros  | `token[string]*`    |
|             | `placa[string]*`|
| Success Response | `[{"imei": "----","placa": "---"},{"imei": "---","placa": "-"}]`  |
|                | `{ "msg": "No existen coincidencias para xxx"}` |
| Error Response | `{error_msg':'Faltan Parametros Obligatorios}`  |
|                | `{error_msg:'Token Incorrecto'}`  |
|                | `{error_msg:'Ha ocurrido un error, intenta de nuevo'}`  |

_*Parametro obligatorio_

| Titulo      | Información Vehiculo  |
| :------------ |:---------------    |
| URL         | `/gps/infoVehiculo`   |
| Metodo      | **GET**             |
| Parametros  | `token[string]*`    |
|             | `imei[string]*`    |
| Success Response | `{"placa": "--", "num_economico": "--","velocidad": "--","motor": -}`  |
|                | `{ "msg": "No existen coincidencias para la IMEI: ---"}` |
| Error Response | `{error_msg':'Faltan Parametros Obligatorios}`  |
|                | `{error_msg:'Token Incorrecto'}`  |
|                | `{error_msg:'Ha ocurrido un error al obtener la informacion, intenta de nuevo'}`  |

_*Parametro obligatorio_

| Titulo      | Coordenadas  |
| :------------ |:---------------    |
| URL         | `/gps/coordenadas`   |
| Metodo      | **GET**             |
| Parametros  | `token[string]*`    |
|             | `imei[string]`    |
|             | `sitio_id[string]`    |
| Success Response | `[{"imei": "--","latitud": "-","longitud": "-","status":-},{"imei": "--","latitud": "--","longitud": "--","status":-}...]`  |
|                | `{ "msg": "No existen coincidencias :("}` |
| Error Response | `{error_msg':'Faltan Parametros Obligatorios}`  |
|                | `{error_msg:'Token Incorrecto'}`  |
|                | `{error_msg:'Ha ocurrido un error, intenta de nuevo'}`  |

_*Parametro obligatorio_


