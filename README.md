# frontend-task
Тестовое задание

## Описание

Представьте, что вам пришел заказ от очень популярной мини-игры в достаточно 
большой социальной сети. Название игры - "Гоночки". Суть игры заключается в том,
что пользователи выполняют заезды стараясь пройти одну и ту же дистанцию за
максимально короткий промежуток времени. Стоит заметить, что игра присутствует 
только в мобильном виде, то есть разработана специально для мобильных устройств 
по размерам, начиная с iPhone 5S и заканчивая iPad Pro. 

Количество пользователей в данный момент превышает 4 миллиона.

## Задача
Ваша задача заключается в том, что в этом приложении необходимо отобразить 
рейтинговую таблицу с пользователями. Нет необходимости что-либо 
действительно подгружать с каких-либо серверов, эти данные можно просто 
замокать и имитировать подгрузку данных отображением лоадера.

Ко всему прочему, список пользователей необходимо сгенерировать самостоятельно.
Тип данных пользователя можно взять [отсюда](#типы-данных). Менять эти типы
данных **запрещено**.

В качестве выполненной работы необходимо выложить проект на GitHub и 
предоставить ссылку для просмотра исходников.

## Требования к технологиям
- React **без использования классовых компонентов**
- React Hooks
- Минимальная ширина экрана - 320px. Максимальная 1920px

## Требования к визуалу
- При первичной загрузке необходимо отображать 50 первых пользователей
- Приложение не должно тормозить даже когда на экране более 1000 пользователей
- Осуществлять lazy load подгрузку когда скролл приближается к нижней границе
экрана. Подгрузка осуществляется по 50 пользователей
- Если имя человека не помещается в границы экрана, обрезаем его многоточием
- Все аватарки пользователей в любой момент времени должны быть на одном 
вертикальном уровне. После подгрузки новых пользователей и в случае, когда их
аватарки находятся правее предыдущих, аватарки предыдущих пользователей 
необходимо **плавно** разместить на уровень с новыми 
- Кликом на пользователя мы можем выделить его фиолетовым цветом
- Выполненная работа должна быть визуально приближенной к [макету](#макет) указанному 
ниже. Поле штрафное время реализовывать не нужно
- В качестве изображения пользователя необходимо показать шлем с цветом, 
который он когда-то выбрал. SVG-изображение шлема имеется в репозитории

## Сдача работы
- В качестве выполненной работы необходимо выложить проект на GitHub и предоставить ссылку для просмотра исходников.
- Развернуть это приложения для визуального просмотра

## Типы данных
```typescript
// Список возможных цветов
enum Color {
  RED, 
  GREEN, 
  BLUE
}

// Пользователь. Позиция в рейтинговой таблице определяется позицией в 
// массиве пользователей
interface User {
  // Любимый цвет
  color: Color;
  // Полное имя
  name: string;
  // Скорость выполнения заезда
  speed: number;
  // Время заезда. Выражено в миллисекундах
  time: number;
}
```

## Макет
![image](https://user-images.githubusercontent.com/34907325/76761753-d2b26380-67b1-11ea-9e81-c59cce69a67f.png)
