# Виджет новостной ленты

Ссылка на готовую работу https://cyberqostya.github.io/newswidget/  
Поскольку виджет **резиновый** и предполагается, что его вставят на веб-страничку в отдельный, боковой, маленький блок, лучше лицезреть его в режиме разработчика с включенным **device toolbar**.

## Развернуть проект в режиме разработки или произвести сборку

На вашем компьютере должен быть установлен Node.js и любой редактор кода ( я использовал VSCode и Node.js версии 14.15.5 ).

### Режим разработки + локальный сервер
1. Скопировать репозиторий локально командой `git clone https://github.com/cyberqostya/newswidget`;
2. Открыть корневую папку проекта через редактор кода;
3. Установить необходимые зависимости командой `npm install`;
4. (необязательно) Так как в проекте реализована имитация приема данных с сервера, необходимо зайти в директорию **/simpleserver** и запустить простой сервер командой `node server.js`. После успешного запуска в теримнале вы увидите сообщение **Сервер запущен!**;
5. Вернуться в корневую папку и запустить проект в режиме разработчика командой `npm run dev`.

### Сборка проекта
1. п.1 - п.4 *Режима разработки*;
2. Командой `npm run build` произвести сборку. В корне роекта появится папка *dist* со всеми собранными файлами.

### В проекте реализовано:
1. Вёрстка по методологии БЭМ;
2. Соблюдена семантика;
3. Реализована адаптивность (резиновость);
4. Разработка с помощью сборщика webpack;
5. Реализован простой локальный сервер на Node.js(express) для иммитации отдачи файлов.

### Интересные моменты проекта:
1. Новости помечаются **прочитанными** при переходе на них;
2. Большинство отступов в виджете зависят от размера шрифта корневого **root** элемента, поэтому данный блок можно с уверенностью вставлять на страницы разного масштаба;
3. Новости добавляются сначала свежие;
4. Если не развертывать локальный сервер, то проект все равно можно будет просмотреть;
5. Когда все новости просмотрены, счетчик уведомлений исчезает.
6. Виджет добавляется на страницу с помощью JavaScript (в корневой элемент с классом **root** если точно).