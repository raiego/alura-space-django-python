# Alura Space

Uma aplicação web construída em Django que permite criar uma galeria de fotos integrada com armazenamento em AWS S3.

##  Tecnologias utilizadas
- Django
- S3 via `django-storages`
- Python
- HTML / CSS / Bootstrap

##  Funcionalidades
- Upload, listagem e exclusão de fotos.
- Autenticação de usuários.
- Integração com AWS S3 para armazenamento de imagens.

##  Como executar localmente

```bash
# Clone o repositório
git clone https://github.com/raiego/alura-space-django-python.git
cd alura-space-django-python

# Crie e ative a venv
python -m venv .venv
.\.venv\Scripts\activate

# Instale as dependências
pip install -r requirements.txt

# Configure o .env com suas chaves AWS
cp .env.example .env
# Edite o .env com: SECRET_KEY, AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, AWS_STORAGE_BUCKET_NAME

# Rode migrations
python manage.py migrate

# Crie um superusuário (opcional)
python manage.py createsuperuser

# Execute o servidor
python manage.py runserver
```
Testado em produção
A configuração do storages para uso com Django 5.2+ (usando o dicionário STORAGES) foi implementada com sucesso.

O comando collectstatic enviou os arquivos estáticos corretamente para o bucket S3.

