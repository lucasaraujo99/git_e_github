# Gerar uma chave SSH

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

## Atenção

* Nunca compartilhe a chave privada (`id_ed25519`).
* A chave pública (`id_ed25519.pub`) pode ser adicionada ao GitHub.

## Token (alternativa à chave SSH)

https://www.alura.com.br/artigos/nova-exigencia-do-git-de-autenticacao-por-token-o-que-e-o-que-devo-fazer