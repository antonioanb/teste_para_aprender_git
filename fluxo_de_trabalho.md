# fluxo de trabalho no git/GitHub iniciante

```bash
mkdir meu-projeto      # Cria pasta
cd meu-projeto         # Entra na pasta
git init              # Inicializa Git (cria .git/)
```

### configurar (se ainda não fez)

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

 **Editar normalmente....**

```bash
git add .                    # Prepara TODOS os arquivos
# ou
git add README.md app.js    # Prepara arquivos específicos
```

Isso coloca os arquivos ou o arquivo na "área de staging" do Git, selecionados e prontos para commit.

### Criar versão

```bash
git commit -m "Descrição clara do que foi feito"
# Exemplo de comentário: "Adiciona README e função de login"
```

### CONECTAR AO GitHub

```bash
# No GitHub.com: criar repositório vazio (New Repository)
# Copiar URL SSH: git@github.com:usuario/repo.git

git remote add origin git@github.com:usuario/repo.git
```

### Enviar para o GitHub

```bash
git push -u origin main
# -u = "upstream" (salva referência)
```

### FLUXO VISUAL RÁPIDO

```bash
[Seu PC]                                   [GitHub]
   │                                          │
1. git init                                   │
   │───cria .git/────┐                        │
   │                 │                        │
2. Edita arquivos    │                        │
   │                 │                        │
3. git add          │                        │
   │───staging───────┘                        │
   │                                          │
4. git commit                                 │
   │───versão local──┐                        │
   │                 │                        │
5. git remote add    │                        │
   │───conecta───────┼───────────────────────►│
   │                 │                        │
6. git push          │                        │
   │───envia tudo────┼───────────────────────►│
   │                 │                        │
   │                 │   ✅ ARQUIVOS NO GITHUB│
```

### CICLO DIÁRIO (depois do primeiro push)

```bash
# 1. Sempre comece atualizado
git pull

# 2. Trabalhe nos arquivos
# ... edita, cria, deleta ...

# 3. Prepare as mudanças
git add .

# 4. Crie versão local
git commit -m "Mensagem descritiva"

# 5. Envie para o GitHub
git push

# REPITA: pull → trabalhar → add → commit → push
```

### Exemplo de rotina 2

```bash
# Manhã: Começar trabalho
git pull  # Atualiza do GitHub

# Durante o dia: Desenvolver
git status  # Vejo onde estou
git add .   # Preparo mudanças
git commit -m "Implementa feature X"  # Salvo local
git push    # Envio para o GitHub

# Final do dia: Organizar
git log --oneline --since="9am"  # Vejo o que fiz hoje
```