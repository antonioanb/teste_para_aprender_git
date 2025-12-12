# BRANCHES (RAMIFICAÇÕES) NO GIT
a função de branch permite que se trabalhe em múltiplas versões do mesmo projeto simultaneamente.

## O QUE SÃO BRANCHES?
Analogia: Árvore de Decisões

Pense em branches como ramos de uma árvore:

- Tronco principal (main/master): Versão estável

- Ramos (feature, bugfix): Experimentos, novas funcionalidades

- Você pode crescer ramos e depois juntá-los ao tronco

## Definição Técnica:

Uma branch é um ponteiro móvel para um commit específico. Cada branch tem seu próprio histórico de commits.

## vantagens de usar branches
- Isolamento: Trabalhar em features sem afetar a versão estável

- Experimentos: Testar ideias sem medo de quebrar tudo

- Colaboração: Múltiplas pessoas podem trabalhar em paralelo

- Organização: Separação clara entre: features/bugs/releases

## comandos basicos
 Ver branches existentes
``` bash
git branch           # Lista branches locais
git branch -a        # Lista TODAS (locais + remotas)
git branch -v        # Lista com último commit de cada
```
## criar novas
```bash
git branch nome-da-branch      # Cria mas NÃO muda
git checkout -b nome-da-branch # Cria E muda (mais comum)
# Ou (Git 2.23+):
git switch -c nome-da-branch
```
 
## Mudar de branch (checkout/switch)

``` bash
git checkout nome-da-branch    # Método tradicional
git switch nome-da-branch      # Método novo (Git 2.23+)
``` 

## Deletar branch

```bash
git branch -d nome-da-branch   # Deleta local (se mergeado)
git branch -D nome-da-branch   # Deleta FORÇADO (não mergeado)
```

## renomear

```bash
git branch -m novo-nome        # Renomeia branch atual
git branch -m antigo novo      # Renomeia branch específica
```