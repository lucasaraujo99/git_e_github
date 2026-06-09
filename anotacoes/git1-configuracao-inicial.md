# Configuração Inicial de um Repositório Git

## Inicializar um repositório local

```bash
git init
```

Cria um novo repositório Git no diretório atual.

---

## Adicionar arquivos

### Adicionar um arquivo específico

```bash
git add arquivo.extensao
```

### Adicionar todos os arquivos do diretório

```bash
git add .
```

---

## Configurar usuário

Caso seja necessário configurar sua identidade:

```bash
git config --global user.email "your@example.com"
git config --global user.name "Your Name"
```

Verificar configurações:

```bash
git config --list
```

---

## Criar um commit

```bash
git commit -m "first commit"
```

Cria um commit com a mensagem informada.

---

## Criar ou renomear a branch principal para main

```bash
git branch -M main
```

---

## Conectar a um repositório remoto

Adicionar um repositório remoto:

```bash
git remote add origin git@github.com:usuario/repositorio.git
```

Listar repositórios remotos:

```bash
git remote -v
```

Remover um repositório remoto:

```bash
git remote remove origin
```

Renomear um repositório remoto:

```bash
git remote rename origin novo-origin
```

Alterar a URL de um repositório remoto:

```bash
git remote set-url origin https://github.com/seu-usuario/seu-repositorio.git
```

Alterar o apelido de um repositório remoto:

```bash
git remote rename origin novo-origin
```

### Gerar uma chave SSH

Para fazer a conexão de um diretório remoto com um diretório local, é preciso de um chave SSH.

### Token (alternativa à chave SSH)

https://www.alura.com.br/artigos/nova-exigencia-do-git-de-autenticacao-por-token-o-que-e-o-que-devo-fazer

---

## Enviar alterações para o GitHub

Primeiro envio da branch:

```bash
git push -u origin main
```

Envios posteriores:

```bash
git push
```
