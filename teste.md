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

---

## Gerar uma chave SSH

Documentação oficial:

https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

No Git Bash:

```bash
ssh-keygen -t ed25519 -C "your@example.com"
```

Arquivos gerados:

```text
id_ed25519      -> chave privada
id_ed25519.pub  -> chave pública
```

### Atenção

* Nunca compartilhe a chave privada (`id_ed25519`).
* A chave pública (`id_ed25519.pub`) pode ser adicionada ao GitHub.

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
