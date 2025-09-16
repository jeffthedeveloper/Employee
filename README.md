# Employee (Cadastro de Funcionário)

Este é um programa de console simples, escrito em Java, focado nos princípios de Programação Orientada a Objetos (POO). O programa permite o registro de um funcionário, calcula seu salário líquido com base no salário bruto e nos impostos, e aplica um aumento salarial com base em uma porcentagem.

## Funcionalidades

  * **Registro de Dados:** Solicita ao usuário o nome, o salário bruto e o valor do imposto de um funcionário.
  * **Cálculo de Salário Líquido:** Possui um método (`netSalary`) para calcular e retornar o salário líquido (Salário Bruto - Imposto).
  * **Aumento Salarial:** Inclui um método (`increaseSalary`) que atualiza o salário bruto com base em uma porcentagem de aumento fornecida.
  * **Exibição de Dados:** Mostra os dados iniciais do funcionário e, em seguida, os dados atualizados após o aumento.

## Estrutura do Repositório

O projeto está organizado da seguinte forma:

```
/
├── src/                      # Pasta contendo o código-fonte .java
│   ├── application/
│   │   └── Program.java      # Classe principal (main) que executa a aplicação
│   ├── entities/
│   │   └── employee.java     # Classe de entidade que define o Funcionário
│   └── module-info.java    # Define o módulo Java (empregado)
│
├── bin/                      # Pasta contendo os arquivos .class compilados
│   ├── application/
│   │   └── Program.class
│   ├── entities/
│   │   └── employee.class
│   └── module-info.class
│
└── README.md                 # Este arquivo de descrição
```

## Como Usar

Este é um projeto de console Java. Para executá-lo, você precisará ter o Java Development Kit (JDK) instalado e configurado.

1.  **Compilação (Opcional, se já não estiver compilado):**
    Navegue até a pasta `src` e compile os arquivos:

    ```bash
    javac -d ../bin application/Program.java entities/employee.java
    ```

2.  **Execução:**
    A partir da raiz do projeto, execute a classe `Program` que está dentro da pasta `bin`:

    ```bash
    java -cp bin application.Program
    ```

3.  **Interação com o Programa:**
    O console solicitará as seguintes informações:

      * `name:` (Nome do funcionário)
      * `Gross salary:` (Salário bruto)
      * `Tax:` (Valor do imposto)

    Após a entrada inicial, o programa exibirá os dados do funcionário com o salário líquido calculado.

    Em seguida, ele perguntará:

      * `Which percentage to increase salary?` (Qual porcentagem para aumentar o salário?)

    Depois de informar a porcentagem, o programa exibirá os "Dados atualizados" (`Updated data:`) com o novo salário líquido.

## Observações

  * **Formato de Números:** O programa está configurado com `Locale.US`. Isso significa que, ao inserir valores decimais (como salário ou imposto), você deve usar o **ponto** (`.`) como separador (ex: `3000.50` ou `100.00`).
  * **Persistência de Dados:** O programa *não* salva os dados em um banco de dados ou arquivo. As informações do funcionário são mantidas em memória apenas durante a execução do programa.
