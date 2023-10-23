# SelectList

`SelectList` - это простой и легко настраиваемый JavaScript класс для создания списков элементов с возможностью выбора активного элемента. Он предоставляет удобный способ управления списками на вашем веб-сайте и позволяет гибко управлять выбором активного элемента.

## Установка

Просто подключите файл `selectlist.js` к вашему проекту:

```html
<script src="selectlist.js"></script>
```

## Использование

1. **Инициализация:**

   Создайте новый экземпляр `SelectList`, передавая ему DOM-элемент, который будет представлять список:

   ```javascript
   const selectListElement = document.getElementById('selectList');
   const selectList = new SelectList(selectListElement, { isRequired: true });
   ```

2. **Добавление элементов:**

   Добавьте элементы к списку, устанавлив свойство `innerHTML`:

   ```javascript
   selectList.innerHTML = `
       <div>Элемент 1</div>
       <div>Элемент 2</div>
       <div>Элемент 3</div>
   `;
   ```

3. **Работа с активным элементом:**

   `SelectList` автоматически определяет активный элемент. Если у вас нет элемента с классом `'.active'`, и `isRequired` установлен в `true`, первый элемент автоматически становится активным. Вы также можете управлять активным элементом программно, устанавливая и снимая класс `'active'`.

## Параметры

- `isRequired` (по умолчанию `true`): Определяет, должен ли быть выбран хотя бы один элемент в списке. Если `false`, пользователь может снять выделение с элемента повторно нажав на него.

## Пример

```html
<div id="selectList" class="select-list"></div>

<script>
    const selectListElement = document.getElementById('selectList');
    const selectList = new SelectList(selectListElement, { isRequired: true });

    selectList.innerHTML = `
        <div class="select-list__item">Элемент 1</div>
        <div class="select-list__item">Элемент 2</div>
        <div class="select-list__item">Элемент 3</div>
    `;
</script>
```

(Добавление классов select-list и select-list__item не обязателно, SelectList может сделать это за вас автоматически)

## Лицензия

Этот проект лицензирован под [GNU General Public License v3.0](LICENSE).

---

Пожалуйста, убедитесь, что описание соответствует функциональности вашего класса. Если есть какие-либо другие особенности или дополнительные параметры, которые стоит упомянуть, пожалуйста, дайте знать!
