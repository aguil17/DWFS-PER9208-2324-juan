# API de Calculadora



**Recursos identificados**:

- Calculadora(calculators): Representa una calculadora


| Método HTTP                            | URI                   | Query Params  | Cuerpo de la Petición                                              | Cuerpo de la Respuesta                                                                | Códigos de Respuesta                                    |
|----------------------------------------|-----------------------|---------------|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------|
| POST                                   | /calculators/sumar    | N/A           | `[2,2,2]`                                                             | `4`           | 200 OK<br/>400 Bad Request<br/>500 Internal Server Error   |
| POST                                   | /loans                | N/A           | `{"userId": 123, "bookId": 789, "dueDate": "2023-08-01"}`          | `{"loanId": 321, "userId": 123, "bookId": 789, "dueDate": "2023-08-01"}`              | 201 Created<br/>400 Bad Request<br/>500 Internal Server Error |
| DELETE (podría haber sido PUT o PATCH) | /loans/{loanId}       | N/A           | N/A                                                                | `{"message": "Loan returned"}`                                                        | 200 OK<br/>404 Not Found<br/>500 Internal Server Error      |
| GET                                    | /users/{userId}/loans | N/A           | N/A                                                                | `{"loans": [{"loanId": 321, "bookId": 789, "dueDate": "2023-08-01"}]}`                | 200 OK<br/>404 Not Found<br/>500 Internal Server Error      |
| PATCH                                  | /books/{bookId}       | N/A           | `{"title": "Advanced REST", "author": "Jane Smith", "year": 2023}` | `{"bookId": 789, "title": "Advanced REST", "author": "Jane Smith", "year": 2023}`     | 200 OK<br/>400 Bad Request<br/>404 Not Found<br/>500 Internal Server Error |
| POST                                   | /users/{userId}/reports/     | N/A           | N/A                                                                | `{"userId": 123, "loans": [{"loanId": 321, "bookId": 789, "dueDate": "2023-08-01"}]}` | 202 Accepted<br/>404 Not Found<br/>500 Internal Server Error    |