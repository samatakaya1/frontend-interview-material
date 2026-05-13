[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/frontend-performance/frontend-performance.md)
---

# Что такое Core Web Vitals?

---

Core Web Vitals — это набор метрик, которые помогают оценивать пользовательский опыт страницы: скорость загрузки, отзывчивость и визуальную стабильность.

Эти метрики важны, потому что они описывают не только техническую скорость, но и то, как пользователь воспринимает страницу.

---

#### Пример

```txt
LCP <= 2.5s
INP <= 200ms
CLS <= 0.1
```

---

#### Что важно знать?

- `LCP` показывает, когда загрузился самый крупный видимый элемент.
- `INP` оценивает отзывчивость страницы на действия пользователя.
- `CLS` измеряет неожиданные сдвиги layout во время загрузки.
- На метрики влияют изображения, шрифты, JavaScript, серверный ответ и стабильность размеров элементов.
- Улучшать Core Web Vitals нужно по данным реальных пользователей и лабораторным замерам.

---

#### Итог

Core Web Vitals помогают говорить о производительности через пользовательский опыт: быстро ли виден контент, быстро ли страница реагирует и не прыгает ли интерфейс.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/frontend-performance/frontend-performance.md)
