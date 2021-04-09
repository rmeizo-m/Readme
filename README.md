# Как запустить
npm start
## Команды запуска проекта

###### `npm i`
###### `npm start`

Откройте http://localhost: 3000, чтобы просмотреть его в браузере.

###### `npm run build`

Собирает приложение для производства в папку `build`. \
Он связывает React в производственном режиме и оптимизирует сборку для достижения максимальной производительности.

## Библиотеки:
###### socket.io-client для работы с сокетами на клиенте
###### node-sass препроцессор для стилизации
###### redux хранилище даныых
###### classnames  библиотека для простого условного объединения имен классов
###### redux-toolkit джентельменский набор для Redux

## Структура проекта
### Компоненты-контейнеры и презентационные компоненты.

>чистая функция — это функция, которая: \
+ является детерминированной; 
+ не обладает побочными эффектами.


компоненты-контейнеры содержат исходные данные и работают с состоянием
Состояние передается презентационным компонентам как свойство и затем рендерится в представление.




## Пример как работает Websocket + Redux + Hook

<code>
    import { socket } from 'socketUtil.js'; \
    import { useDispatch } from 'react-redux';\
</code>

<code>
const ChatRoomComponent = () => {
    const dispatch = useDispatch();

    useEffect(() => {
        socket.on('event://get-message', payload => {
            // update messages
            useDispatch({ type: UPDATE_CHAT_LOG }, payload)
        });
        socket.on('event://user-joined', payload => {
            // handling a new user joining to room
        });
    });
    // other implementations
  }
</code>

###### http://webdesign.ru.net/article/pravila-oformleniya-fayla-readmemd-na-github.html



