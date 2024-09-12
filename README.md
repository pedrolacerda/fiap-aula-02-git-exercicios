### **Exercício Prático em Duplas ou Trios**

#### **Objetivo:**
Colaborar com outro aluno em um projeto compartilhado, utilizando conceitos de branches, commits, merge e tags.

#### **Instruções:**

1. **Formem uma dupla ou trio** e sigam as etapas abaixo:
   
2. **Escolha de um "repositório principal"**:
   - Um dos membros do grupo criará um repositório local chamado `projeto-colaborativo`.
   - Esse membro deverá inicializar o repositório local com o comando:
     ```bash
     git init
     ```

3. **Criação de um arquivo inicial**:
   - No repositório, crie um arquivo de texto simples chamado `texto.txt` e adicione uma frase inicial:
     - Exemplo: "Essa é a primeira frase do projeto colaborativo."
   - Adicione o arquivo ao stage e faça um commit:
     ```bash
     git add texto.txt
     git commit -m "Adicionando o arquivo texto.txt"
     ```

4. **Compartilhamento do Repositório via GitHub**:
   - O membro que criou o repositório deverá criar um repositório no GitHub e fazer o primeiro push:
     ```bash
     git remote add origin <URL_DO_REPOSITÓRIO_NO_GITHUB>
     git push origin main
     ```

5. **Clonagem do Repositório pelos Outros Membros**:
   - Os outros membros do grupo clonarão o repositório:
     ```bash
     git clone <URL_DO_REPOSITÓRIO_NO_GITHUB>
     ```

6. **Criação de Branches Individuais**:
   - Cada membro deve criar um **branch** com seu nome:
     ```bash
     git checkout -b nome_do_aluno
     ```
   - Nesse branch, cada membro deverá **adicionar uma nova frase** ao arquivo `texto.txt` e fazer um commit:
     ```bash
     echo "Nova frase do nome_do_aluno." >> texto.txt
     git add texto.txt
     git commit -m "Adicionando frase de nome_do_aluno"
     ```

7. **Merge no Branch Principal (main)**:
   - Após as alterações, cada membro deve voltar ao branch `main` e fazer o merge de seu branch:
     ```bash
     git checkout main
     git merge nome_do_aluno
     ```

8. **Resolução de Conflitos (se houver)**:
   - Caso dois ou mais alunos tenham modificado a mesma linha no arquivo, o Git poderá gerar um conflito. Resolvam o conflito editando o arquivo manualmente, mantendo ambas as contribuições, e depois façam um commit para finalizar:
     ```bash
     git add texto.txt
     git commit -m "Resolvendo conflito"
     ```

9. **Criação de uma Tag**:
   - Após todas as alterações estarem no branch `main`, criem uma **tag** para marcar a versão final do projeto:
     ```bash
     git tag -a v1.0 -m "Versão final do projeto colaborativo"
     ```

10. **Envio das Alterações e Tag para o GitHub**:
    - Façam push do branch `main` atualizado e da tag criada:
      ```bash
      git push origin main
      git push origin v1.0
      ```

---

### **Objetivo do Exercício**:
- **Colaboração**: Os alunos praticarão o fluxo de trabalho colaborativo com Git e GitHub.
- **Branches**: Cada aluno trabalhará de forma isolada em seu branch.
- **Merge e Conflitos**: Resolverão conflitos simples, caso ocorram.
- **Tags**: Criarão uma tag para marcar a versão final do projeto.
