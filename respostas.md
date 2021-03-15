1. Descreva qual é a saída dos seguintes comandos
    -  `git branch` 

    ```
    Mostra as branches disponíveis, indicando qual é a branch atual
    ```

    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)

    ```
    Altera para a outra branch
    ```

    -  `git log --decorate`

    ```
    Mostra as informações básicas dos commits
    ```

2. Tente usar `git log --graph --all`. O que acontece?
```
É mostrada uma árvore com as branches e os commits
```

3. Use `git diff BRANCH_NAME`  para ver as diferenças de um ramo e do ramo atual.
   Sumarize as diferenças do master e do outro ramo.

```
Método foo foi adicionado na classe A e a classe B foi removida.
```

4. Escreva uma sequencia de comandos para mesclar o ramo não-master no `master`

```
git checkout master
git merge feature-foo
```

5. Escreva um comando (ou sequência) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

```
git checkout -b math
```

6. Edite B.java adicionando o código abaixo ao conteúdo do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudanças
```
git add .\handson\B.java
git commit -m "Atualiza arquivo B.java"
```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequência de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```
git merge math

Conflito!!!
```

10. Escreva um conjunto de comandos para abortar a mesclagem
```
git merge --abort
```

11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funções implementadas são necessárias. Explique o seu procedimento
```
Todas as linhas foram mantidas.
```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```
git commit -a -m "Correção de conflitos"
```
