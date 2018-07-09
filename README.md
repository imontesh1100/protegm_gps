**MultiSistemas GPS App Services Documentation**
----
  _A continuacion se muestra de forma general cada uno de los servicios creados para la aplicación móvil GPS MULTISISTEMAS , se incluye toda la información necesaria para hacer las consultas correspondientes._

**Usuarios**
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

