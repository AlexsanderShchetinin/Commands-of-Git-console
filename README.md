## **Commands console Git**

| **Command** | **Translate**                      | **Remark**                                 | **По Русски**                                                       |
|-------------|------------------------------------|--------------------------------------------|---------------------------------------------------------------------|
| cd (*)      | change directory                   | (*) - name of directory                    | Переход по папкам, пишем cd и через пробел имя папки куда переходим |
| cd ..       | come back in last directory        |                                            | Переход к предыдущей папке                                          |
| ls          | list                               |                                            | Осмотреться (команда показывает все файлы в текущей директории)     |
| pwd         | Print working directory            |                                            | Показывает текущую папку                                            |
| cd ~        | Return at home directory           |                                            | перейти в домашнюю директорию                                      |
| touch (*)   | Create a new file                  | (*) - name of creating file with extension | создать файл                                                        |
| mkdir (*)   | Make directory                     | (*) - name of new directory                | Создание новой папки в текущей                                      |
| cat (*)     | read file                          | (*) - name of file                         | чтение файла <br/>(имя файла писать вместе с расширением)           |
| rmdir (*)   | Remove directory (if dir is empty) | (*) - name of remove directory             | Удаление папки, если она пустая                                     |
        

			

### Статусы untracked/tracked, staged и modified

каждый файл помечается каким-либо статусом.

![img.png](img.png)

1. Файл только что создали. Git ещё не отслеживает его содержимое. Состояние: untracked.
2. Файл добавили в staging area с помощью git add. Состояние: staged(+ tracked).
a. Возможно, изменили файл ещё раз. Состояния: staged, modified(+ tracked). 
Обратите внимание: staged и modified у одного файла, но у разных его версий.
b. Ещё раз выполнили git add. Состояние: staged(+ tracked).
3. Сделали коммит с помощью git commit. Состояние: tracked.
4. Изменили файл. Состояние: modified(+ tracked).
5. Снова добавили в staging area с помощью git add. Состояния: staged(+ tracked).
6. Сделали коммит. Состояния: tracked.
7. Повторили пункты 4−7 много-много раз.


   • untracked (Untracked files) - неотслеживаемый 
Когда созданный новый файл еще не добавлен для отслеживания командой git add …

![img_1.png](img_1.png)

• staged (Changes to be committed в выводе git status) - подготовленный
Такой статус после того, как файл стал отслеживаемым (теперь он готов к коммиту)

![img_2.png](img_2.png)

• modified (Changes not staged for commit) - измененный
Когда после того как закоммитили файл, в него внесли правки.

![img_3.png](img_3.png)

Если после этого добавить измененный файл в staging area командой git add, 
то новый статус git status будет указывать что файл уже изменен (а не новый созданный) 
об этом указывает "modifided" перед именем файла.

![img_4.png](img_4.png)
			
