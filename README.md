# <project>

Descrição

## Como desenvolver?

1. Clone o repositório.
2. Crie um virtualenv com Python 3.9.
3. Ative o virtualenv.
4. Instale as dependências.
5. Configure a instância com o .env.
6. Execute os testes.

```console
git clone git@github.com:niltonpimentel02/<project>.git <project>
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp contrib/env-sample .env
pytest
```

## Como fazer deploy?

1. Crie uma instância Heroku.
2. Envie as configurações para o Heroku.
3. Defina uma SECRET_KEY segura para a instância.
4. Defina DEBUG=False.
5. Configure o serviço de email.
6. Envie o código para o Heroku.

```console
heroku create <project>
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`  
heroku config:set DEBUG=False  
# configuro o email  
git push heroku master --force  
```
