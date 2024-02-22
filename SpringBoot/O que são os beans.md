Os beans no Spring são frequentemente anotados com annotations especiais que informam ao container do Spring como criar e gerenciar esses objetos. Algumas das annotations comuns usadas para marcar classes como beans incluem:

1. **@Component**: É a annotation mais genérica e serve como ponto de partida para outras annotations de estereótipo. Ela indica que uma classe é um componente genérico que deve ser detectado e configurado pelo container do Spring.

2. **@Service**: Usada para marcar classes de serviço que contêm a lógica de negócios da aplicação.

3. **@Repository**: Usada para marcar classes que acessam o banco de dados ou realizam operações de persistência.

4. **@Controller**: Usada para marcar classes que tratam solicitações web em aplicativos baseados em Spring MVC.

5. **@RestController**: Semelhante a `@Controller`, mas específica para a construção de APIs RESTful que retornam dados no formato JSON ou XML.

6. **@Configuration**: Usada para marcar classes que fornecem configurações para o container do Spring. As classes marcadas com `@Configuration` podem conter métodos anotados com `@Bean`, que registram beans customizados no contexto do Spring.