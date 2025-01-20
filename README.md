# Задание 1

> Выполнены уровни 1-2, уровень 3 не сделан.

## Выбор инструмента для декомпозиции

Принципиальной разницы между Single SPA и Module Federation для текущего проекта нет, можно использовать любой из них. 

Я выбираю Webpack Module Federation т.к.:
+ код проекта написан на React и в микрофронтендах будет использоваться он же. Таким образом, необходимости поддерживать несколько UI-фреймворков нет
+ у меня, как у разработчика, есть опыт работы с данным фреймворком (пусть и минимальный только в рамках курса)

## Структура проекта

Предполагаю, что имеет смысл разбить на микрофронтенды по трем доменам: auth (авторизация, регистрация), profile (информация о пользователе, аватар), posts (список постов с фотографиями и описаниями мест, лайки). Так же необходим управляющий микрофронтент host, собирающий компоненты в общую структуру и регулирующий роутинг.

Распределение компонентов по микрофронтендам:

+ host
  + App - главный компонент. Содержит роутер и связывает логику работы других компонентов
  + Footer - футер всего приложения
  + Header - компонент шапки приложения
  + Main - компонент с основным контентом приложения - списком фото, а так же ссылками на загрузку фото и управлением профайлом
  + ProtectedRoute - определяет отображаемый контент на основе данных об авторизации 

+ auth
  + Login - форма для логина
  + Register - форма для регистрации
  + InfoToolTip - попап с информацией о регистрации

+ profile
  + EditAvatarPopup - попап для редактирования аватара
  + EditProfilePopup - попап для редактирования профиля

+ posts
  + Card - компонент карточки с изображением
  + AddPlacePopup - попап для загрузки фото
  + ImagePopup - попап ля просмотра отдельного изображения

запуск не реализован

# Задание 2

[https://drive.google.com/file/d/1mozoAFKbaaSqgYw0MF4tJm1aEDieezuU/view?usp=sharing] (Ссылка на решение)