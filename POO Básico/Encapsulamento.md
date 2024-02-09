O encapsulamento se refere à prática de **esconder** os detalhes internos de uma classe, mantendo os atributos (variáveis e instância) e métodos (funções) relacionados a essa classe protegido e inacessíveis diretamente fora da classe.

Motivos pelo quais o encapsulamento é importante:

1. **Segurança de dados:** Ao ocultar os detalhes internos de uma classe, você evita que dados sensíveis ou críticos sejam inadvertidamente ou intencionalmente alterados/modificados ou acessados de maneiras inadequadas. Por exemplo: 

Nesse código que eu fiz, é a representação de uma conta bancária e na conta bancária eu quero que nada seja alterado, apenas irei settar, e a única coisa que será 'alterado' será o saldo/saque/depósito, que será o cliente que irá fazer. 

```Java
public class TesteContaBancaria {  
    public static void main(String[] args) {  
        ContaBancaria contaBancaria1 = new ContaBancaria();  
        //Settando, estou definindo o numero e o titular 
        //etc... (Set = definindo)  
        contaBancaria1.setNumero("36547895499");  
  
        contaBancaria1.setTitular("José");  
        //Setando o saldo  
        contaBancaria1.setSaldo(100);  
  
        //Depositando o saldo, ficará 100 reais.  
        contaBancaria1.depositar(50);  
        contaBancaria1.sacar(100);  
  
        //Aqui eu estou dando get no número (get = pegando)  
        System.out.println(" Olá, " + 
        contaBancaria1.getTitular());  
        System.out.println(" O número da conta é : " + 
        contaBancaria1.getNumero());  
    }  
}
```

```Java
public class ContaBancaria {  
    private String numero;  
    private String titular;  
    private double saldo;  
  
  
    public String getNumero() {  
        return numero;  
    }  
  
    public void setNumero(String numero) {  
        this.numero = numero;  
    }  
  
    public String getTitular() {  
        return titular;  
    }  
  
    public void setTitular(String titular) {  
        this.titular = titular;  
    }  
  
    public double getSaldo() {  
        return saldo;  
    }  
  
    public void setSaldo(double saldo) {  
        //Também posso setar que o saldo possa começar com 0 
        //reais.  
        this.saldo = saldo;  
    }  
  
    void depositar (double valor) {  
        if (valor > 0) {  
            saldo += valor;  
            System.out.println("Depósito de R$ " + valor + " 
            Saldo atual :" + saldo);  
        } else {  
            System.out.println(" O valor do depósito é 
            inválido");  
        }  
    }  
  
    void sacar (double valor) {  
        if (valor < 0 && valor <= saldo) {  
            saldo -= valor;  
            System.out.println("Saque de R$ " + saldo + " 
            Efetuado com sucesso.");  
        }  
    }  
}
```

Aqui eu coloco como private o número da conta, titular e saldo.

2. **Controle de acesso:** O encapsulamento permite que você controle quem pode acessar e modificar os atributos de uma classe. Isso ajuda a evitar bugs causados por modificação inesperada.
3. **Flexibilidade:** Você pode adicionar validações, lógica de negócios o tratamento de exceção dentro dos métodos de acesso (getters e setters), no caso, ali dentro do getSaldo ou algo do tipo, você pode fazer uma lógica naquele escopo.

Pode-se aplicar o encapsulamento usando modificadores de acesso, como "private", "protected", "public" e "default" (pacote), para controlar a visibilidade de atributos e métodos. Geralmente, os atributos declarados como "private", e métodos públicos (Getters e Setters) são fornecidos para acessar e modificar esses atributos. 

### Valores Padrões
Por exemplo, se eu quero que a idade, saldo ou algo do tipo seja FIXO, eu vou ter que criar um constructor desse jeito aqui, por exemplo:

```Java
public class ContaBancaria {  
    private String numero;  
    private String titular;  
    private double saldo;  
  
  
    //Constructor  
    public ContaBancaria() {  
        saldo = 0.0;  
    }
```

Desse jeito aqui, o saldo vai sempre se permanecer em 0,0 reais. Não vai dar para altera-lo. E tendo isso, você não precisa usar um Setter nele. Apenas o get.