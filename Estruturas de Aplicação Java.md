# Modulo, Agrupamento lógico de pacotes relacionados

![[Pasted image 20240126114259.png]]

- Se é algo financeiro, serviço e repositórios, eu agrupo isso em um módulo.
- Se é algo de gráfico, Graphics3D, 2D ou Utilitários, posso agrupar em outro módulo.

	 O Runtime é uma unidade física que pode ser instalado para rodar dispositivos. 

### Packages, agrupamentos LÓGICOS de classes relacionadas
- Na minha aplicação eu posso ter **vários** tipos de **classes**, posso ter classes que representam as entidades dos negócios, como por exemplo: ![[Pasted image 20240126114626.png]]
- Cliente, produto, pedido.
- As **Classes** que são entidades eu posso criar um pacote para elas (**PACKAGES**) chamado de *Entities* para organizar e agrupar a minha aplicação.
- Da mesma forma posso organizar as classes de serviços em outros pacotes, como por exemplo: *Serviço de emails, Serviço de pedidos, Logins e etc*...
- Também podemos fazer com os **Repositores** que são classes para acessar Dados.


Vamos pensar como construir esse método. Vamos imaginar, no nosso _array_ de 100, que as primeiras dez posições já estão preenchidas. Queremos inserir um aluno na terceira posição, como na imagem abaixo:

![Imagem de fundo azul escuro, com nove retângulos verticais na cor cinza e enfileirados horizontalmente. O terceiro retângulo está destacado pela cor vermelha.](https://www.alura.com.br/artigos/assets/estrutura-dados-computacao-na-pratica-com-java/img1.jpg)

Para isso, vamos arrastar todos os alunos da terceira posição em diante para a direita e colocamos aquele aluno no buraco que ficou, como podemos observar na imagem a seguir: