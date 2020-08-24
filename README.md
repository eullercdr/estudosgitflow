# Trabalhando com GITFLOW
## Inicialização em novo projeto
```php
git flow init
```

## Inicialização em projeto existente
Deve se executar o comando no branch master do projeto
```php
- git flow init
```
## GIT Flow Feature
- Define uma nova funcionalidade
- Prefixo padrão FEATURE/*
- **Toda feature inicia-se em develop**
- **Toda feature termina em develop**

```php
git flow feature start <namefeature>
git flow feature finish <namefeature>
```
- Após a finalização da feature o branch será excluido localmente e será mesclado em dev

Caso deseje subir a feature para que outros desenvolvedores trabalhem nela utilizar

```php
git flow feature publish  <namefeature>
```
Para trazer uma feature do repositorio remoto para a máquina local , utilizar: 

```php
git flow feature track <namefeature>
```
Cuidado: Não faça merge da feature do repositorio remoto no branch dev, finalize-a sempre localmente

## GIT Flow Release
- Define uma nova versão do software em produção
- Prefixo padrão RELEASE/*


```php
git flow release start 0.0.1 (minor-major-patch)
git flow release finish 0.0.1
```
- Após a finalização da release, deverá ser informado a descrição da tag.
- Release será mesclada em master
- Uma tag será gerada com o nome da release
- O branch dev será atualizado, mesclado do master.

## GIT Flow Hotfix
- Corrige erros de release
- Define um novo branch para correção de erros
- Prefixo padrão HOTFIX/*
- Nome sempre será superior a release escopo
- Será criado apartir do master
- Se mescla com master e develop
- Gerará uma nova versão de software

```php
git flow hotfix start 0.0.3 (Deverá ser sempre superior a ultima tag, suponha que a ultima tag tenha sido 0.0.2, respeitar a semantica de versionamento)
git flow hotfix finish 0.0.3
```
## GIT Flow Bugfix
- Define um novo branch para correção de erros
- Prefixo padrão BUGFIX/*
- Inicia-se no branch Develop
- Mesclado no branch Develop

```php
git flow bugfix start fix_bug_report 
git flow bugfix finish fix_bug_report
```
