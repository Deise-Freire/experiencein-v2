# Python on Replit

This is a template to get you started with Python on Replit. It's ready to go so you can just hit run and start coding!

## Running the repl

1. Setup a new secret environment variable (the lock icon) where the key is `SECRET_KEY` and the value is
   a randomly generated token of 32 bits of randomnese. To generate such a token type this into the shell and hit Enter:
```
python
import secrets
secrets.token_urlsafe(32)
```
2. Hit run!

See this 1 minute video for a walkthrough: [https://www.loom.com/share/ecc4e738149f4d1db3bcff01758b3e71](https://www.loom.com/share/341b5574d12040fb9fcbbff150777f1c)

## Installing packages

To add packages to your repl, you can just import directly in the file you want to use the package in, and it will automatically be installed when you press the run button. Like below:
```python
import math
import pandas as pd
```

You could also install packages by using the Replit packager interface in the left sidebar.

## Help

If you need help you might be able to find an answer on our [docs](https://docs.replit.com) page. Feel free to report bugs and give us feedback [here](https://replit.com/support).

## Parte 1 (back-end API)

https://docs.google.com/document/d/1q2Q0z3VX69jPx4CuvBceaq2V84TvHyFD8K6-QFWCKIs/edit

## ExperienceIn API (Parte 1)
https://www.youtube.com/watch?v=RjP4W2OEXt0

## ExperienceIn API (Parte 2)
https://www.youtube.com/watch?v=fUxCwHP8j6c

## ExperienceIn API (Parte 3)
https://www.youtube.com/watch?v=qJCtoMM-QZI

## ExperienceIn API (Parte 4)
https://youtu.be/Mr3oHC02nYE

## ExperienceIn API (Parte 5)
https://youtu.be/DdWoKIdf4ac

## github
code <repositório>

## console
git clone <repositório>

git branch
> master
git branch api
git branch
> api
> master
git checkout api
git branch
> api
> master

## Ativar ambiente virtual
virtualenv venv
source venv/bin/activate
clear

pip3 install djangorestframework
settings.py

INSTALLED_APPS = [
    'rest_framework',
    'rest_framework.authtoken',
    'corsheaders',
]

# experiencein > perfis > serializers.py

# experiencein > perfis > views.py
from django.shortcuts import render, redirect
from perfis.models import Perfil, Convite
from django.contrib.auth.decorators import login_required

from rest_framework import viewsets
from rest_framework.permissions import AllowAny

class PerfilViewSet(viewsets.ModelViewSet):
    queryset = Perfil.objects.all()
    serializer_class = None

    def get_serializer_class(self):
        if self.request.method == 'GET':
            return None
        return super().get_serializer_class()

    def get_permissions(self):
        if self.request.method == 'POST':
            return (AllowAny(),)
        return super().get_permissions()


# Parte 2 (front-end)
https://docs.google.com/document/d/173g-H_pYKYBQHZjItRzAdN4BZE7zrhwS_FFYib7Uazk/edit#heading=h.fvu0diog16wu

# ExperienceIn front-end com React (Parte 1)
https://www.youtube.com/watch?v=urluEm7UHsE


python3 manage.py migrate --fake
python3 manage.py makemigrations
python3 manage.py migrate

## Criando perfis no banco

python manage.py shell 
>>> from perfis.models import Perfil
>>> perfil = Perfil(nome='Oswaldo', email='oswaldo@oswaldo.com', telefone='n/a', nome_empresa='IFB')
>>> perfil.save()
>>> perfil_encontrado = Perfil.objects.get(id=1)
>>> perfil_encontrado.nome = 'Oswaldo Alterado'
>>> perfil_encontrado.save()
>>> perfil_encontrado = Perfil.objects.get(id=1)
>>> perfil_encontrado.nome
>>> perfil = Perfil.objects.create(nome='Steve', email='steve@minecraft.com', telefone='n/a', nome_empresa='IFB')
>>>
## Buscando perfis

python manage.py shell
>>> from perfis.models import Perfil
>>> p = Perfil.objects.get(id=1) #Perfil 1 deve existir
>>> p.nome
>>> p = Perfil.objects.get(nome='Steve') #Steve deve existir
>>> p.id

## Filtrando perfis
python manage.py shell
>>> from perfis.models import Perfil
>>> perfis = Perfil.objects.filter(email__contains='s')
>>> perfis = Perfil.objects.filter(email__contains='s')
>>> perfis = Perfil.objects.filter(email__icontains='s')
>>> perfis = Perfil.objects.filter(email__startswith='s')

## Selecionando perfis de uma lista

python manage.py shell

>>> from perfis.models import Perfil
>>> perfil1 = Perfil(nome='Fábio Henrique', email='fabio.oliveira@ifb.edu.br', telefone='n/a', nome_empresa='IFB')
>>> perfil1.save()

>>> perfil2 = Perfil(nome='Tiago Henrique', email='tiago.segato@ifb.edu.br', telefone='n/a', nome_empresa='IFB')
>>> perfil2.save()
>>>
>>>
yarn add express 

