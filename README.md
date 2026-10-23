# Oficina Mecânica – Sistema Desktop

Sistema desktop em **Python (Tkinter)** com banco **MySQL** para cadastro e
gerenciamento de **donos, carros e procedimentos**, com login e sessão com
tempo de expiração.

## 1. Estrutura dos arquivos

```
oficina_db.sql            -> Entrega 03 (criação e população do banco)
oficina_diagrama.sql      -> somente a estrutura, para gerar o DER (Entrega 02)
README.md
sistema/                 -> Entregas 04 a 08 (código-fonte)
├── main.py              -> ponto de entrada (troca de telas + vigia da sessão)
├── config.py            -> conexão MySQL, chave de criptografia, tempo da sessão
├── database.py          -> acesso ao banco (queries parametrizadas)
├── seguranca.py         -> hash de senha, validação de CPF/celular/placa
├── sessao.py            -> sessão do usuário com expiração
├── login.py             -> Entrega 04: login
├── principal.py         -> Entrega 05: tela principal
├── dono.py              -> Entrega 06: gerenciamento de dono (com busca)
├── carro.py             -> Entrega 07: gerenciamento de carro
├── procedimento.py      -> Entrega 08: procedimentos (filtro Dia/Mês/Ano)
├── icone.png / icone.ico -> ícone (engrenagem e chave) das janelas
└── requirements.txt
```

### 1.2 Configurar o sistema

Abra **`sistema/config.py`** e altere a senha do MySQL em `DB_CONFIG`:

```python
"password": os.getenv("SAEP_DB_PASSWORD", "SUA_SENHA_AQUI"),
```

Se mudar `host`, `port` ou `user`, ajuste também no mesmo bloco.

### 1.3 Instalar a dependência e executar

Abra um terminal na pasta `sistema/` e rode:

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python main.py
```


