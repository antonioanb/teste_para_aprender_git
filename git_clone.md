# 📥 GIT CLONE - BAIXANDO REPOSITÓRIOS

O git clone é o comando para baixar um repositório Git completo do GitHub (ou qualquer servidor) para o computador.

 ele faz download de um projeto inteiro, incluindo:

    - Todos os arquivos do projeto

    - Histórico completo de commits

    - Todas as branches

    - Configurações do Git

## Sintaxe Basica
```bash
git clone <URL-do-repositório>
``` 

## tipos de clone

 ## SSH (Recomendado - usa sua chave)
```bash 
SSH (Recomendado - usa sua chave)
```

## HTTPS (Pede senha/token)
```bash
git clone https://github.com/usuario/repositorio.git
```

## GitHub CLI (se tiver instalado)
```bash
gh repo clone usuario/repositorio
```

## Exemplo
## clonando repositorio publico
```bash
# Vamos clonar o Bootstrap (exemplo público)
git clone https://github.com/twbs/bootstrap.git

# Ou com SSH (se configurado):
git clone git@github.com:twbs/bootstrap.git
```
## clonando o proprio repositorio
```bash
# Do SEU GitHub:
git clone git@github.com:antonioanb/teste_para_aprender_git.git
```

## visão geral
```bash
# Antes: Pasta vazia
# Comando:
git clone git@github.com:usuario/projeto.git

# Depois:
# 📁 projeto/          ← Pasta criada automaticamente
#   ├── 📄 README.md   ← Arquivos do projeto
#   ├── 📄 app.js
#   ├── 📁 src/
#   └── 📁 .git/       ← Histórico completo (oculto)
```

## verificar apos clonar
```bash
cd nome-do-repositorio
git remote -v  # Mostra origem
git branch     # Mostra branch local
git log --oneline  # Mostra histórico
```

## opções do git clone

### Especificar nome da pasta

```  bash
# Padrão: cria pasta com nome do repositório
git clone URL  # Cria pasta "repositorio/"

# Personalizado: escolha o nome
git clone URL meu-projeto  # Cria pasta "meu-projeto/"
```

### Clonar sem histórico (shallow clone)
```bash
# Útil para projetos muito grandes
git clone --depth 1 URL  # Apenas último commit
```

### Clonar apenas a branch principal
```bash
# Clona apenas a branch main (mais rápido)
git clone --branch main --single-branch URL 
```