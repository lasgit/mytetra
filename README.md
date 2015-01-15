Создание репозитария с данными MyTetra
Итак, переходим в директорию /data и даем следующие команды:

Перво-наперво нужно создать новый пустой репозитарий в системе GitHub mytetra
git init
git add .

git commit -a -m "first commit"
git remote add origin git@github.com:lasgit/mytetra.git --для ssh
или
git remote add origin https://github.com/lasgit/mytetra.git --для https
git push -u origin master

SSH ключи

    ВНИМАНИЕ! Для того, чтобы при использовании ключа не запрашивался логин/пароль, нужно обращаться к удаленному репозилорию по shh, а не по https. Для примера, это адрес https https://github.com/<Username>/<Project>.git, а это ssh git@github.com:<Username>/<Project>.git

$ ssh-keygen -t rsa -C "your_email@example.com"
$ clip < ~/.ssh/id_rsa.pub или  открываем id_rsa.pub sublime копируем его
На Github: Accout setting -> SSH Keys -> add -> paste -> Add key Проверяем:

ssh -T git@github.com

 # start the ssh-agent in the background
$ eval "$(ssh-agent -s)"
# Agent pid 59566 -ответ
$ ssh-add ~/.ssh/id_rsa

после каждго коммита
git push для переноса на github
