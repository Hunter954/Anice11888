# Site Anice 11888

Projeto em Python/Flask preparado para publicação no GitHub e no Railway.

## Estrutura

- `app.py`: aplicação Flask
- `templates/index.html`: página principal
- `static/style.css`: responsividade
- `static/images/desktop.png`: fundo para desktop
- `static/images/mobile.png`: fundo para celular
- `requirements.txt`: dependências
- `Procfile`: comando de inicialização no Railway

## Executar localmente

```bash
python -m venv .venv
```

### Windows

```bash
.venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

### Linux/macOS

```bash
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

Abra `http://localhost:5000`.

## Publicar no Railway

1. Envie esta pasta para um repositório no GitHub.
2. No Railway, crie um novo projeto.
3. Selecione **Deploy from GitHub repo**.
4. Escolha o repositório.
5. O Railway detectará o Python e usará o comando do `Procfile`.
6. Gere um domínio em **Settings > Networking > Generate Domain**.

A rota `/health` pode ser usada para verificação de saúde da aplicação.


## Correção do deploy

O arquivo `runtime.txt` com a versão exata `3.12.8` foi removido porque o Railpack
não conseguiu validar o artefato dessa versão. O projeto agora usa `.python-version`
com `3.12`, permitindo que o Railway selecione uma versão de correção compatível.
