# Operações Básicas com Git

## Clonar um repositório

```bash
git clone https://github.com/nome-do-usuario/nome-do-repositorio.git
```

Cria uma cópia local de um repositório remoto.

---

## Verificar o status do repositório

```bash
git status
```

Permite verificar:

* Arquivos modificados.
* Arquivos adicionados.
* Arquivos prontos para commit.
* Arquivos não rastreados (*untracked*).

---

## Adicionar arquivos para commit

### Adicionar todos os arquivos modificados

```bash
git add .
```

### Adicionar um arquivo específico

```bash
git add nome-do-arquivo
```

---

## Criar um commit

```bash
git commit -m "mensagem informando o que foi alterado"
```

Um commit normalmente deve ser realizado quando:

* Uma funcionalidade foi concluída.
* Um bug foi corrigido.
* Uma alteração lógica foi finalizada.

### Boas práticas para mensagens de commit

* Manter a mensagem curta e objetiva.
* Descrever claramente a alteração realizada.
* Evitar textos excessivamente longos.
* Utilizar um padrão consistente ao longo do projeto.

### Exemplos

```text
Adicionar validação de login

Corrigir erro no cadastro de usuários

Atualizar README
```

---

## Visualizar histórico de commits

```bash
git log
```

Exibe informações como:

* Autor do commit.
* Data.
* Hash do commit.
* Mensagem de commit.

---

## Enviar commits para o repositório remoto

```bash
git push origin main
```

Onde:

* `origin` → nome do repositório remoto.
* `main` → branch de destino.

---

## Atualizar o repositório local com mudanças remotas

```bash
git pull origin main
```

Busca e aplica as alterações existentes no repositório remoto.

---

## Listar repositórios remotos

```bash
git remote -v
```

Exibe todos os repositórios remotos configurados e suas URLs.

---

## Comparar alterações

```bash
git diff
```

Mostra as diferenças entre os arquivos modificados e a última versão registrada no Git.

### Exemplos úteis

Comparar alterações ainda não adicionadas:

```bash
git diff
```

Comparar alterações já adicionadas para commit:

```bash
git diff --staged
```
