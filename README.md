### Проект собирается с таким compose:
```yml
services:
  postgres:
    image: postgres:latest
    container_name: postgres_db
    environment:
      POSTGRES_USER: student
      POSTGRES_PASSWORD: student
      POSTGRES_DB: mydb
    ports:
      - "5432:5432"
```
![](images/1.png)
### После чего заполянется рандомными данными.
![](images/2.png)
### Но после удаления контейнеров и повторного подключения к базе данных, появляется ошибка о том что таблица *users* не найдена [скрин забыл сделать :( ]. И это очень даже $make\;sense$, потому что мы не прописывали никакие *Volume*.

### Если же это изменить и прописать заветные *Volume*, и запустить такой же контейнер
![](images/3.png)
### Заполнить его всеми нужными рандомными данными 
![](images/4.png)
###  После чего удалить отключить и удалить контейнер и заново его запустить
![](images/5.png)
### То, чудо, все данные остались
![](images/6.png)
# Предыдущие задания
![](images/7.png)
![](images/8.png)
![](images/9.png)