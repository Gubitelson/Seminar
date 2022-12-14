# All of GIT, Cmd and Markdown

 ![Git logo](media/30c29ce4cc08523ecc6e1f205bc207d0.jpeg)
## 1. Git 
*Это система контроля ваерсий, позволяющая эффективно управлять историей исходного кода. 
Любые изменения которые ты вносишь в проект могут быть сохранены с помощью Git. 
Ты можешь вернуться к любым ранее сохраненным версиям. 
Без Git пришлось бы создавать копии проекта, что было бы проблемой при увеличении объема кода в приложении*

### 1.1. Основныее команды git
* **git --help** - показывает команды для работы
* **git init** - Позволяет проинициализировать репозиторий в открытой папке (*Разрешает git отслеживать изменения в папке*)
* **git status** - Показывает текущий статус

* **git add "Нужный файл"** - Отслеживает изменения файлов (*Буквально, отслеживает в тот момент когда мы вводим комманду add, не постоянно*)
* **git add .** — добавляет все файлы в папке

* **git commit -m 'message'** — создает коммит с сообщением (*По сути точка сохранения или резервная копия + коммент, что поменялось с прошлого сохранения*).
Если commit срабоатет правильно будет создан уникальный id(ссылка) **bush** по которому можно восстановить точку сохранения 
* **git log** - для нахождения хэша нужного коммита (при использовании достаточно первых 4-х значений)

### 1.2. Работа с ветками в репозитории
* **git branch** — показывает список веток
* **git branch branch-name** — создает новую ветку branch-name
* **git branch -D branch-name** — удаляет ветку branch-name (d - delete)
* **git branch -f main HEAD~3** - Переместит (принудительно) ветку main на три родителя назад от HEAD. (f - forsing)

* **git checkout branch-name** — переключается на последний коммит в ветке branch-name
* **git checkout -b branch-name** — создает и переключается на ветку branch-name (b - branch)

* **git merge branch-name** — совмещает текущую ветку с branch-name (*К примеру решили разделиться чтобы понять чье решение лучше, в конце чье решение лучше обьединяет в себя побочную ветку*)
* **git rebase** - не сосвем слияние, скорее продолжение побочной ветки после разделения. (2 ветки fix и mane*. после воода команды следущий комит после fix станет mane*. вторая ситцация первый комит mane* второй fix после ввода команды, mane перезапишет коммит fix) 

### 1.3. Git конфигурация и настройки
* **git config --global user.name** — Показывает имя пользователя
* **git config --global user.name 'new user'** — Изменяет имя пользователя
* **git config --global user.email** — Показывает email пользователя
* **git config --global user.email 'test@mail.ru'** — Изменяет email пользователя

### 1.4. *GitHub* share
* **git push** - Заливает текущие локальные коммиты в удаленный репозиторий
* **git pull** - Забирает изменения с удаленного репозитория в локальный
* **git clone** - Клонирует проект с удаленного репозитория

### 1.5. Тонкости
* **HEAD** - это символическое имя выбранного коммита — это, по сути, тот коммит, над которым мы в данный момент работаем.
**HEAD** всегда указывает на последний коммит из вашего локального дерева. Большинство команд Git, изменяющих рабочее дерево, начнут с изменения **HEAD**.
Обычно **HEAD** указывает на имя ветки (например, bugFix). Когда вы делаете коммит, статус ветки bugFix меняется и это изменение видно через **HEAD**.

Относительные ссылки ~ и ^
* **^ (каретка)** Перемещение на один коммит назад. (*Когда мы добавляем его к имени ссылки, Git воспринимает это как указание найти родителя указанного коммита. Так что main^ означает "первый родитель ветки main". main^^ означает прародитель (родитель родителя) main*)
* ~<num> Перемещение на несколько коммитов назад 
 
 * Можно прикрепить ветку к коммиту при помощи опции -f. Например, команда:
git branch -f main HEAD~3
Переместит (принудительно) ветку main на три родителя назад от HEAD.
 
## 1.6. Отмена изменений в Git
* **git reset** - отменяет изменения, перенося ссылку на ветку назад, на более старый коммит. Это своего рода "переписывание истории"; git reset перенесёт ветку назад, как будто некоторых коммитов вовсе и не было. Reset отлично работает на локальных ветках, в локальных репозиториях. Но этот метод переписывания истории не сработает на удалённых ветках, которые используют другие пользователи.
* **git revert** - Чтобы отменить изменения и поделиться отменёнными изменениями с остальными. после написания появится новый коммит. Дело в том, что новый коммит C2' просто содержит изменения, полностью противоположные тем, что сделаны в коммите C2. После revert можно сделать push и поделиться изменениями с остальными.
 
 
## 2. Работа с директорией
* **cd путь** - *change directory* смена директории/папки (cd далее полный путь либо путь относительно текущей дериктории/папки)
* **cd ..** - для перехода на уровень выше
* **dir или ls** - содержимое текущей директории
*  **cls или clear** - очистить окно консоли
*  **mkdir имя_папки** - создать папку в текущей директории


## 3. Markdown
*Это простой язык разметки, используемый для создания форматированного текста (например, HTML) с помощью текстового редактора. Он позволяет добавлять к тексту базовое форматирование, используя символы, известные и доступные на всех клавиатурах. Размер шрифта, цвет и другие расширенные параметры недоступны в Markdown.*

### 3.1. Оформление текста

| Синтаксис | Результат |
|------|--------------------|
| # | Заголовок 1 |
| ## | Заголовок 2 |
| ### | Заголовок 3 |
| *  * |	*Курсив* |
| **  **   |	**Жирный** |
| ~~  ~~	| ~~Зачеркнутый~~ |

### 3.2. Таблицы и списки

**Таблицы**

|Столбец 1|Столбец 2|Столбец 3|

|---------|—--------|---------|

|  Слева  |По центру|  Справа |	

**Списки**

Неупорядоченный список "* текст"
* Пункт 1
* Пункт 2
* Пункт 3

Упорядоченый список "1. текст"
1. Пункт 1
2. Пункт 2
3. Пункт 3

### 3.3. Ссылки и изображения

* **Изображение** 
![Текст при отсутвсии файла](/путь/к/изображению.jpg"Текст при наведении")
*Нужно указывать положение изображение относительно репозитория*

 
* **Ссылка**
* [Link] (https://ссылка.com/)

 
* **Внутренний код** 
`https://www.youtube.com/`
*чтобы сделать встроенный код нужно обрамить ссылку апострофом "`"*

 
* **Блок кода**
*три обратных кавычки без пробелов*

## Ссылки на ресурсы в порядке полезности
* https://youtu.be/JfpCicDUMKc видосик сначальными данными
* https://vk.com/@vladilen.minin-git-and-github методичка от чувака с видоса
* https://learngitbranching.js.org/?locale=ru_RU&demo= какая то игра про ветки 
* https://habr.com/ru/post/541258/ пояснялки на святом хабре
* https://habr.com/ru/post/542616/ смотри выше
* https://habr.com/ru/company/ruvds/blog/599929/ еще команды гит
