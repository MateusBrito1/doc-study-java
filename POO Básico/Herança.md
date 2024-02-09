A herança é um conceito que literalmente herda as coisas que você pega de outra classe. Por exemplo, eu tenho uma classe Pessoa, certo? nela vai conter as seguintes variáveis:
- CPF
- NOME
- IDADE
- COR
Até ai ok, então, vamos querer criar um PROFESSOR/ALUNO, são pessoas, certo? 
Então vamos criar uma classe delas, elas irão conter as seguintes variáveis:
Professor:
- Salário
- Matéria
Aluno:
- Número de matricula 
### E como herdar as coisas da classe da Pessoa padrão?
Vamos fazer do seguinte jeito.

```Java
public class Professor extends Pessoa {  
    private double salarios;  
  
    public double getSalarios() {  
        return salarios;  
    }  
  
    public void setSalarios(double salarios) {  
        this.salarios = salarios;  
    }  
}
```

Vamos usar o **Extends** que no caso ela vai HERDAR/EXTENDER da classe Pessoa os atributos/variáveis de lá, que são as mencionadas acima: CPF, NOME, IDADE e etc...
E vamos criar a única variável do professor que vai ser EXCLUSIVAMENTE dele, ninguém mais vai poder usar, que no caso é o SALÁRIO. E assim podemos se repetir com o Aluno.

```Java
public class Aluno extends Pessoa{  
    private String matricula;  
  
    public String getMatricula() {  
        return matricula;  
    }  
  
    public void setMatricula(String matricula) {  
        this.matricula = matricula;  
    }  
}
```

```Java
    public static void main(String[] args) {  
        Professor prof = new Professor();  
        prof.setCpf("3333333");  
        prof.setNome("Mateus");  
        prof.setIdade(15);  
        prof.setSalarios(50000);  
  
        System.out.println(prof.imprimirDadosPessoais());  
  
        Aluno aluno = new Aluno();  
        aluno.setCpf("555555");  
        aluno.setNome("Brito");  
        aluno.setIdade(18);  
        aluno.setMatricula("Matriculado");  
  
        System.out.println(aluno.imprimirDadosPessoais());  
    }  
}
```

Aqui vemos na prática de como é usado.