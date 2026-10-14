# Biblioteca Fácil — projeto Python para análise no SonarQube Cloud

Projeto de porte médio para demonstrar análise estática de código Python no SonarQube Cloud. É um sistema simples de gerenciamento de livros e empréstimos, organizado em módulos e acompanhado de testes automatizados.

## Requisitos
- Python 3.10 ou superior
- `pip`

## Executar localmente
No terminal, dentro desta pasta:

```bash
python main.py
```

O programa abre um menu no terminal para cadastrar/listar livros e registrar/devolver empréstimos.

## Executar os testes
```bash
python -m pip install -r requirements.txt
python -m unittest discover -s tests -v
```

## Publicar no GitHub
1. Crie um repositório no GitHub.
2. Envie **a pasta do projeto inteira**, mantendo a estrutura de diretórios.
3. No SonarQube Cloud, importe/conecte o repositório.
4. Configure o método de análise indicado pelo SonarQube Cloud (GitHub Actions ou análise automática, conforme a configuração disponível na organização).
5. Se o Sonar solicitar propriedades do projeto, confira `sonar-project.properties`.

Não é necessário enviar cada arquivo individualmente. O Git registra os arquivos e subpastas que você adicionar e confirmar (`commit`/`push`). Evite enviar `.venv`, `__pycache__` e outros arquivos temporários.

## Estrutura
```text
projeto_biblioteca_sonar/
├── main.py
├── requirements.txt
├── sonar-project.properties
├── README.md
├── biblioteca/
│   ├── __init__.py
│   ├── catalogo.py
│   ├── emprestimos.py
│   ├── modelos.py
│   └── relatorios.py
└── tests/
    ├── test_catalogo.py
    ├── test_emprestimos.py
    └── test_relatorios.py
```

## Observação sobre a análise
Este projeto foi escrito para servir de exemplo didático. O SonarQube pode apontar problemas diferentes conforme o perfil de qualidade, a versão do analisador e as regras habilitadas. Os testes ajudam a verificar o comportamento, mas não substituem a análise estática.
