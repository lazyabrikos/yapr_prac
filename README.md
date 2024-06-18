## Основыне команды git

git remote add origin - связать локальный репозиторий с удаленным <br>
git add - добавить файлы <br>
git status - проверить состояние коммитов <br>
git log - посмотреть историю коммитов <br>
git remove -v - посмотреть что репозитории связаны <br>
git push -u origin master - В первый раз эту команду нужно вызвать с флагом -u и параметрами origin (имя удалённого репозитория) и main или master (название текущей ветки). Флаг -u свяжет локальную ветку с одноимённой удалённой. Как вы связывали локальный и удалённый репозитории, так же и здесь нужно дополнительно связать ветки.

HEAD - указатель на последний коммит
git log - отобразить историю коммитов
git log --oneline отобразить истопию коммитов сокращенно

git status - статусы файлов

untracked - неотслеживаемый файл, 
staged - подготовленный, после выполнения команды файл поподает в stagin area, тоесть в список файлов, которые войдут в коммит
tracked - файлы, которые уже были зафиксированы с помощью коммит
modified - git сравнил прошлую версию файла и новую и нашел различия
Для файлов в состояниях staged и modified обычно не указывается, что они также tracked, потому что это состояние подразумевается.
Команда git add добавляет в staging area только текущее содержимое файла. Если вы, например, сделаете git add file.txt, а затем измените file.txt, то новое содержимое файла не будет находиться в staging. Git сообщит об этом с помощью статуса modified: файл изменён относительно той версии, которая уже в staging. Чтобы добавить в staging последнюю версию, нужно выполнить git add file.txt ещё раз.

Дополнить коммит новыми файлами — git commit --amend --no-edit

Дополнить коммит новыми файлами — git commit --amend --no-edit
Изменить сообщение коммита — git commit --amend -m "Новое сообщение"

```mermaid
untracked -- "git add" --> staged
staged -- "git commit" --> tracked (modified)
tracked -- "changes" --> modified
modified -- "git add" --> staged
```
