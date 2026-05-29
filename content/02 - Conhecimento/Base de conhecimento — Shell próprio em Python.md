
## Python básico

- Variáveis, condicionais e loops — a lógica é a mesma do JS, só a sintaxe muda
- Funções com `def`
- Listas e dicionários (dicionário = objeto do JS)
- Importar módulos com `import`
- Tratamento de erros com `try/except` (equivalente ao `try/catch`)

## Python específico para o projeto

- Módulos da biblioteca padrão: `os`, `subprocess` e `shlex`
    - Não precisa decorar — só saber que existem e consultar a documentação quando precisar
- O que é `if __name__ == "__main__"` — como o Python identifica o ponto de entrada do programa

## Conceitos de sistema operacional

- O que é um processo
- O que são variáveis de ambiente (como o `$PATH`)
- O que são permissões de arquivo

## Lógica do shell

- Como funciona um loop REPL (Read → Parse → Execute → Print → repete)
- Diferença entre built-ins e programas externos
    - Built-ins: `cd`, `exit` — executados pelo próprio shell
    - Externos: `ls`, `sudo`, `apt-get` — programas que vivem em `/usr/bin/`
- O que é um exit code — todo programa termina com um número (`0` = sucesso, qualquer outro = erro)

---

## Organização de pastas

```
meu-shell/
├── main.py          # ponto de entrada, o loop principal
├── parser.py        # lê e separa o comando digitado
├── executor.py      # executa os comandos
├── builtins.py      # comandos especiais (cd, exit, help...)
└── README.md        # explica o projeto no GitHub
```

## Bibliotecas necessárias

Nenhuma externa — tudo já vem com o Python:

|Módulo|Para que serve|
|---|---|
|`os`|Interagir com o sistema de arquivos e o OS|
|`sys`|stdin, stdout, stderr|
|`subprocess`|Executar programas externos|
|`shlex`|Parsear a linha de comando corretamente|

## Diferenças JS → Python para lembrar

|JavaScript|Python|
|---|---|
|`{}` para blocos|Indentação|
|`;` no fim da linha|Sem `;`|
|`let` / `const` / `var`|Só o nome da variável|
|`function`|`def`|
|`null`|`None`|
|`console.log()`|`print()`|
|`===`|`==`|
|`.push()`|`.append()`|
|`try/catch`|`try/except`|
