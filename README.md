Подробная инструкция
Создаем директорию для проекта
mkDir ForGit

Проверяем статус
git status

Создаем главную ветку
git init

Создаем файл
touch README.md

Перед коммитом готовим файл
git add README.md 

Создаем коммит с сообщением
git commit -m 'Первый коммит в проекте'

Просмотреть коммиты
git log

Создаем SSH ключ
ls -la .ssh/ # вывели список созданных ключей 

Генерация пары
ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" 
Или
ssh-keygen -t rsa -b 4096 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" 

Проверить
ls -a ~/.ssh 

# скопировать содержимое ключа в буфер обмена:
$ pbcopy < ~/.ssh/id_rsa.pub
# для ed25519:
$ pbcopy < ~/.ssh/id_ed25519.pub 

Перейдите на GitHub и выберите пункт Settings в меню аккаунта.
В меню слева нажмите на пункт SSH and GPG keys.
В открывшейся вкладке выберите New SSH key
В поле Title напишите название ключа. Например, Personal key
В поле Key type должно быть Authentication Key
В поле Key скопируйте ваш ключ из буфера обмена.
Нажмите на кнопку Add SSH key
Проверьте правильность ключа с помощью следующей команды.
$ ssh -T git@github.com

Связать локальный и удаленный репозитория
Создать репозитория на гитхаб
Взять там ssh url
git remote add origin git@github.com:Alexey-zygankov/first-project.git

Убедиться, что репозитория созданы
git remote -v

Отправить изменения на удаленный репозиторий
git push -u origin main
