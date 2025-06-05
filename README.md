# 🧪 Prova Técnica

Este repositório contém **dois desafios práticos** que simulam situações reais enfrentadas por administradores Linux. Eles foram projetados para avaliar sua capacidade de investigação, diagnóstico e clareza na comunicação técnica.

---

## 📌 Instruções Gerais

1. Execute cada container individualmente.
2. Analise os comportamentos observados e investigue o que pode estar errado.
3. Use somente os recursos disponíveis dentro do ambiente.
4. Documente os comandos utilizados e todas as suas observações.
5. Suas conclusões devem ser apresentadas durante a entrevista técnica.

Nenhuma dica técnica é fornecida. A intenção é avaliar sua autonomia em ambientes Linux reais.

---

## 📦 Desafio 1 — Falha ao acessar `www.google.com` via `curl`

### Objetivo

Investigar por que o comando abaixo falha:

```bash
curl https://www.google.com
```

Você deverá identificar e justificar a causa do problema.

### Como executar

```bash
docker pull lucasferreira1994/7q:dns-0001
docker run -it --rm lucasferreira1994/7q:dns-0001
```

---

## 📦 Desafio 2 — Acesso SSH negado

### Objetivo

Investigar por que o usuário `suporte01` não consegue acessar o sistema via SSH, mesmo informando a senha correta.

### Como executar

```bash
docker pull lucasferreira1994/7q:ssh-0001
docker run -d -p 2222:22 --name ssh-0001 lucasferreira1994/7q:ssh-0001
```

### Informações de acesso

| Usuário     | Senha      |
|-------------|------------|
| suporte01   | suporte01  |
| suporte02   | suporte02  |

Comandos de teste:

```bash
ssh suporte01@localhost -p 2222
ssh suporte02@localhost -p 2222
```

---

## ✅ O que será avaliado

- Capacidade de troubleshooting.
- Conhecimento sobre ferramentas de diagnóstico Linux.
- Clareza na explicação dos problemas encontrados.
- Raciocínio lógico e domínio técnico.

---

**Importante:** você deverá apresentar os resultados de sua análise, preferencialmente com anotações claras dos testes realizados, arquivos inspecionados e sua explicação técnica sobre o que causava os erros.

Boa sorte e até a entrevista!
