instalar os pacotes para o tutorial app funcionar(forms,banco de dados)
$ pip install flask-wtf
$ pip install email_validator
$ pip install flask-sqlalchemy
$ pip install flask-login
$ pip install flask-bcrypt
$ pip install pillow

Apos projeto criado, antes de executar, setar a seguinte variavel
$ set FLASK_APP=flaskblog.py
$ flask run
# Se utilizar o comando python nomeprojetoflask.py não é necessário criar a variável

para gerar chaves/tokens com o pacote secrets
$python
>> import secrets
>> secrets.token_hex(16)
'chavede32bits'

secrets.randbelow(100) retora um numero randomido entre 0-100

url_for('home') home é o nome do método e não o nome do endpoint(@app.route)

Banco de dados
------------------------
criar as classes de dominio. Executar comando python para criar o db
>> from nomepacote import db
>> from pacote.models import ClasseDominio1, ClasseDominio2
>> db.create_all()

$ objeto_1 = ClasseDominio1(atributo='valor', atributo2='valor2')
$ db.session.add(objeto_1)
$ db.session.commit()
$ ClasseDominio1.query.all()
$ ClasseDominio1.query.first()
$ ClasseDominio1.query.filter_by(atributo='valor').all() | first()

deletar todo o banco
$ db.drop_all()
para criar
$ db.create_all()

Comando do git
git init
git add .
git commit -m "commit initial"
(git branch -M "main")
git remote add origin <urlgit>
git branch -M main
git push -u origin main

push an existing repository from the command line
git remote add origin <project url>
git branch -M main
git push -u origin main

