# API Status Codes

| Código | Estado            | Descripción                                                  |
|--------|--------------------|--------------------------------------------------------------|
| 200    | OK                 | La petición ha tenido éxito                                  |
| 201    | Created            | La solicitud ha tenido éxito y se ha creado un nuevo recurso |
| 204    | No Content         | La solicitud ha tenido éxito, pero no hay contenido para enviar de vuelta |
| 400    | Bad Request        | La solicitud es inválida o está malformada                   |
| 401    | Unauthorized       | Falta autenticación para la solicitud                        |
| 403    | Forbidden          | No tienes permiso para acceder al recurso solicitado         |
| 404    | Not Found          | El recurso solicitado no existe                              |
| 500    | Internal Server Error | Error general del servidor                                 |
| 503    | Service Unavailable | El servicio no está disponible temporalmente                 |
