# Заметка по настройке и синхронизации Git


### сделаем гит по умолчанию мэйном

git config --global init.defaultBranch main

### создал new-project в папке dev

C:\Users\Дмитрий\dev  - это на компе

а это в консоли путь

cd ~/dev/

### создаем

mkdir new-project

### перешли в нужную папку

cd ~/dev/new-project

### создали репозиторий

git init

---
###### ЕСЛИ что то пошло не так надо ее разГИТить:

###### перешли в папку

###### cd <папка с репозиторием> 

###### удалили подпапку .git 

###### rm -rf .git 
---

после проверяем все ли ОКЕЙ

git status

### Создали там файл тхт например или код

### Редачим, потом запоминаем новое состояние так

git add git inf.txt

или 

git add .


### Делаем первый коммит так

git commit -m 'Мой первый коммит в НОВОМ проекте!'


// Сначала вы просите друзей встать в ряд — это команда git add. И только после того, как все заняли свои места, поправили волосы и улыбнулись, вы нажимаете кнопку и делаете снимок — это команда git commit


### Логи смотрим так

git log


### НА САЙТЕ 
https://github.com/new


имя даем new-project

ридми не создаем

Create repository ЖМЕМ внизу


### Осталось связать удалённый репозиторий с локальным

### *ген-ем SHH ключ (скип если имеется)

ssh-keygen -t ed25519 -c "erouwe@yandex.ru"  //или вашу почту гита

Программа запросит кодовую фразу

скипаем 2 раза Enter

ls -a ~/.ssh чекаем тут наличие ключа

выводим ключ на экран

cat ~/.ssh/id_rsa.pub

или

cat ~/.ssh/id_ed25519.pub

в настрйоках ГИтХаба находим  SSH and GPG keys

там New SSH key

В поле Key скопируйте ваш ключ из буфера обмена

ЧЕК на правильность ключа

ssh -T git@github.com


### Надо привязать удалённый репозиторий к локальному

в консоли ввели

cd ~/dev/new-project

затем 

git remote add origin git@github.com:Erouwez/new-project.git

ЧЕК что все связано норм

git remote -v

### Отправить изменения на удалённый репозиторий
 
git push -u origin main

### Далее для отправки всегда

git push


### создаем README

cd ~/dev/new-project

touch README.md

## Схема такая в итоге

```
$ git add .

$ git commit -m 'Правка N такая то'

$ git push

```




