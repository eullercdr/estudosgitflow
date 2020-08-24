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
git flow finish feature <namefeature>
```
- Após a finalização da feature o branch será excluido localmente e será mesclado em dev

## Branch Feature
- Define uma nova funcionalidade
- Prefixo padrão FEATURE/*
- **Toda feature inicia-se em develop**
- **Toda feature termina em develop**

```php
git flow feature start <namefeature>
git flow feature finish <namefeature>
git flow feature publish  <namefeature>
```
- Após a finalização da feature o branch será excluido localmente e será mesclado em dev
