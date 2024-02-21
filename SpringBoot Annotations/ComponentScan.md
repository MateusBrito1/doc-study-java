O componente Scan é uma funcionalidade que permite varrer automaticamente o código-fonte do seu projeto em busca de classes anotadas com determinadas annotation, como `@Component`, `@Service`, `@Repository`, `@Controller` e outras, e registrá-las como beans no contexto do Spring.

### Resumo:
O componente Scan automatiza o processo de descoberta e registro de beans no spring, não precisa configurar manualmente cada bean no arquivo de config do spring.
Mas basicamente o @SpringBootApplication já faz isso, então às vezes nem precisa usá-lo, ela vai servir se for pra algo muito específico.