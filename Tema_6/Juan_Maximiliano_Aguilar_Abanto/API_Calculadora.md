# API de Calculadora



**Recursos identificados**:

- Calculadora(calculators): Representa una calculadora


| Método HTTP | URI                             | Query Params  | Cuerpo de la Petición                    | Cuerpo de la Respuesta                                               | Códigos de Respuesta                                    |
|-------------|---------------------------------|---------------|------------------------------------------|-----------------------------------------------------------------------|---------------------------------------------------------|
| POST        | /api/v1/calculators/add                | N/A           | `{"numbers":[2,2,2]}`                    | `{"operationId": "1","total": 6}`                                    | 201 Created<br/>400 Bad Request<br/>500 Internal Server Error |
| POST        | /api/v1/calculators/substract         | N/A           | `{"numbers":[2,2,2]}`                    | `{"operationId": 1,"total": -2}`                                     | 201 Created<br/>400 Bad Request<br/>500 Internal Server Error |
| POST        | /api/v1/calculators/multiply          | N/A           | `{"number1": 2,"number2": 2}`            | `{"operationId": 1,"total": 4}`                                      | 201 Created<br/>400 Bad Request<br/>500 Internal Server Error |
| POST        | /api/v1/calculators/divide            | N/A           | `{"number1": 2,"number2": 2}`            | `{"operationId": 1,"total": 1}`                                      | 201 Created<br/>400 Bad Request<br/>500 Internal Server Error |
| POST        | /api/v1/calculators/squareroot        | N/A           | `{"number": 4,"root": 2}`                | `{"operationId": 1,"total": 2}`                                      | 201 Created<br/>400 Bad Request<br/>500 Internal Server Error |
| POST        | /api/v1/calculators/power             | N/A           | `{"numero":2, "power":3}`                | `{"operationId": 1, "total": 8}`                                      | 201 Created<br/>400 Bad Request<br/>500 Internal Server Error |
| GET         | /api/v1/calculators/{operationaId}/detail | N/A        | N/A                                      | `{"operationId": 1,"operationtype": "add","body": {"numbers":[2,2,2]} ,"total": 8}` | 200 Ok<br/>404 Not Found<br/>500 Internal Server Error |
