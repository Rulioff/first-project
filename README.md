﻿# Практическая часть курса: "Основы Git" от Яндекс Практикум.


------
## Язык программирования Bash. <br>

```bash
ls -la
```

# Тема 5/8: Навигация по коммитам. Статусы файлов → Урок 1/5.
## Хеш — идентификатор коммита.
В процессе работы с Git вам будет часто встречаться понятие «хеш коммита». Эти странные строчки с бессмысленным (на первый взгляд) набором букв и цифр вы могли видеть, когда вызывали команду git log и выводили историю коммитов.
[Пример истории коммитов.](https://pictures.s3.yandex.net/resources/M2_T5_04-2_1686651606.png)
---
* Git преобразует информацию о коммитах с помощью алгоритма SHA-1 и для каждого из них рассчитывает уникальный идентификатор — хеш.
* Хеш — основной идентификатор коммита и позволяет узнать его автора, дату и содержимое закоммиченных файлов.
* Все хеши, а также таблицу соответствий хеш → информация о коммите Git хранит в папке .git.
# Урок 2 Тема 5. Исследуем лог.
* Можно вызвать не только полный лог, но и сокращённый — это делается командой:

```bash
git log --oneline
```

* В сокращённом логе выводятся сокращённые хеши — их можно использовать точно так же, как и полные.

---
## Урок 3. HEAD — всему голова.
---
* В числе прочих файлов в папке **.git** есть служебный файл **HEAD**. Он указывает на самый свежий коммит.
* Вместо хеша последнего коммита можно написать слово **HEAD** — Git вас поймёт.
---
## Урок 4. Статусы файлов в Git.
---
### [Типичный жизненный цикл файла в Git.](https://pictures.s3.yandex.net/resources/M2_T5_1686651284.png)
* Статусом **untracked** помечается файл, о существовании которого Git знает, но не следит за изменениями в нём. Этот статус — противоположность **tracked**, в который попадают все файлы, отслеживаемые Git.
* Файл переходит в статус **staged** после выполнения **git add**.
* Статус modified означает, что файл был изменён.
* Большинство файлов в проектах «шагает» по следующему циклу: «изменён» → «добавлен в список на коммит» → «закоммичен» → «изменён» → и так далее.
---
