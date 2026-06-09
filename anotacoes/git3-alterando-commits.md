# Alterando Commits

## Reverter um commit

```bash
git revert <commit-id>
```

Cria um novo commit que desfaz as alterações realizadas pelo commit informado.

### Quando usar

* O commit já foi enviado para o repositório remoto.
* Outras pessoas podem estar utilizando a mesma branch.
* Deseja manter o histórico completo das alterações.

### Exemplo

```bash
git revert a1b2c3d
```

---

## Resetar para um commit anterior

```bash
git reset --hard <commit-id>
```

Move a branch para o commit informado e descarta os commits posteriores.

### Exemplo

Considere o histórico:

```text
A → B → C → D (HEAD)
```

Executando:

```bash
git reset --hard B
```

O resultado será:

```text
A → B (HEAD)
```

Os commits `C` e `D` deixam de fazer parte da branch atual.

### Modos de reset

#### Hard

```bash
git reset --hard <commit-id>
```

* Remove os commits posteriores.
* Restaura os arquivos para o estado do commit informado.
* Descarta alterações locais.

#### Mixed

```bash
git reset --mixed <commit-id>
```

* Remove os commits posteriores.
* Mantém as alterações nos arquivos.
* Remove os arquivos da área de staging.

#### Soft

```bash
git reset --soft <commit-id>
```

* Remove os commits posteriores.
* Mantém as alterações.
* Mantém os arquivos na área de staging.

### Atenção

Evite utilizar `git reset` em commits que já foram enviados (`push`) para um repositório compartilhado.

Fonte: https://git-scm.com/docs/git-reset
---

## Alterar a mensagem do último commit

```bash
git commit --amend -m "mensagem corrigida"
```

Substitui a mensagem do commit mais recente.

### Exemplo

```bash
git commit --amend -m "Corrigir validação de login"
```

---

## Adicionar arquivos esquecidos ao último commit

Adicionar o arquivo:

```bash
git add forgotten-file.js
```

Atualizar o commit mantendo a mensagem original:

```bash
git commit --amend --no-edit
```

### Quando usar

Situações em que um arquivo foi esquecido no commit mais recente.

---

## Boas práticas para o uso de amend

O comando `git commit --amend` deve ser utilizado apenas quando o commit ainda não foi enviado para o repositório remoto.

Caso o commit já tenha sido enviado com `git push`, alterar seu conteúdo pode causar conflitos para outras pessoas que estejam utilizando a mesma branch.
