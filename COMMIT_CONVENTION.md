# Convenção de Commits

## Formato da Mensagem de Commit

Cada mensagem de commit consiste em um **header**, um **body** e um **footer**.

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Header

O header é obrigatório e deve seguir o formato:

```
<type>(<scope>): <short summary>
```

#### Type

- **feat**: Nova funcionalidade
- **fix**: Correção de bug
- **docs**: Alterações na documentação
- **style**: Formatação, faltando ponto e vírgula, etc; Sem alteração de código
- **refactor**: Refatoração de código
- **test**: Adicionando testes, refatorando testes; Sem alteração de código
- **chore**: Atualizando tarefas de build, configurações de pacotes, etc; Sem alteração de código

#### Scope

O scope pode ser qualquer coisa especificando o local da alteração do commit. Por exemplo:
- ui
- forms
- animations
- pdf
- api
- docs

#### Subject

O subject contém uma descrição sucinta da mudança:
- Use o imperativo: "change" não "changed" nem "changes"
- Não capitalize a primeira letra
- Sem ponto final (.)

### Body

O body deve incluir a motivação para a mudança e contrastar com o comportamento anterior.

### Footer

O footer deve conter qualquer informação sobre **Breaking Changes** e também é o lugar para referenciar issues do GitHub que este commit fecha.

**Breaking Changes** devem começar com `BREAKING CHANGE:` com um espaço ou duas linhas. O resto da mensagem do commit é então usado para explicação.

## Exemplos

```
feat(forms): add payment method selection

- Add credit card option
- Add PIX option
- Add bank slip option

Closes #123
```

```
fix(animation): correct popup display timing

The welcome popup was appearing too quickly, not allowing
the page to fully load. Added a 500ms delay to ensure
proper display.

Closes #456
```

```
docs(readme): update installation instructions

- Add development setup section
- Update technology stack
- Add contribution guidelines
```

## Referências

- [Conventional Commits](https://www.conventionalcommits.org/)
- [Angular Commit Message Guidelines](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#commit)