# BEM Guide (БЭМ в проекте)

В этом проекте для организации CSS и компонентов используется методология **БЭМ (Block Element Modifier)**.

Она помогает писать поддерживаемый, переиспользуемый и структурированный CSS.

---

## Основные понятия

### Block (блок)
Независимый компонент интерфейса.

Примеры:
- button
- header
- card
- input

```css
.button {}
.header {}
.card {}
````

---

### Element (элемент)

Часть блока, которая не может существовать отдельно от него.

Формат:
block__element

Примеры:

```css
.button__icon {}
.button__text {}

.card__title {}
.card__image {}
```

---

### Modifier (модификатор)

Состояние или вариант блока/элемента.

Формат:
block--modifier
block__element--modifier

Примеры:

```css
.button--primary {}
.button--disabled {}

.card--large {}
```

---

## Правила использования

### 1. Один блок = одна папка

Каждый компонент хранится отдельно:

```
src/blocks/button/
src/blocks/header/
src/blocks/card/
```

---

### 2. Никакой вложенности блоков

Плохо:

```css
.card .button {}
```

Хорошо:

```css
.card__button {}
```

---

### 3. Не использовать глобальные стили внутри блоков

Избегать:

```css
div {}
h1 {}
button {}
```

Только классы БЭМ:

```css
.button {}
.header {}
```

---

### 4. Максимальная вложенность SCSS — 2 уровня

Плохо:

```scss
.card {
  .card__content {
    .card__title {
      color: red;
    }
  }
}
```

---

## Цель использования БЭМ

* Переиспользуемость компонентов
* Понятная структура проекта
* Простая поддержка кода
* Минимизация конфликтов стилей

---

## Пример полного компонента

```html
<div class="card card--large">
  <img class="card__image" />
  <h2 class="card__title">Title</h2>
  <button class="card__button button button--primary">
    Click
  </button>
</div>
```

---

## Важно запомнить

* Block = независимый компонент
* Element = часть блока
* Modifier = состояние или вариант
