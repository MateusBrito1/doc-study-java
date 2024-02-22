O ResponseEntity é uma classe fundamental que retorna respostas HTTP personalizadas a partir dos *seus controladores*. Ele *encapsula* tanto o corpo da resposta quanto os cabeçalhos HTTP, permitindo que você retorna uma resposta HTTP com o código de status desejado.

#### O que é ResponseEntity?
- O ResponseEntity representa toda a resposta HTTP: o corpo (body), cabeçalhos (headers) e os status.
#### Por que usá-lo?
- Ele oferece mais flexibilidade do que simplesmente retornar um objeto como resposta. Com o ResponseEntity, você pode definir explicitamente o código de status HTTP, os cabeçalhos da resposta e o corpo da resposta.
#### Como usá-lo? 
- Você pode criar um ResponseEntity usando um construtor que aceita o corpo da resposta, os cabeçalhos (headers) e o código do status. Por exemplo:
- ![[Tipos de ResponseEntity.png]]
- Eu aprendi a usar dessas 3 maneiras. 
- E também aprendi que se eu tiver certeza de que o que eu for receber no *Body Params* for uma String, eu irei usar String no ResponseEntity String.
- Agora por outro lado, se o corpo da resposta pode ser várias tipos diferentes e eu queira que seja capaz de retornar qualquer um desses tipos, então o `<Object>` é uma escolha mais genérica e flexível. Isso me permite que retorne objetos de qualquer outra classe.
