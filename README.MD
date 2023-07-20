# Тестовое задание

[Вакансия на HH](https://hh.ru/vacancy/83638236)  
[Репозиторий тестового](https://hh.ru/vacancy/83638236)

## Задание 1

###### Ответ:

Первый фрагмент кода выбросит ошибку, так как стрелочная функция используется до своего объявления.

Во втором фрагменте кода используется синтаксис function declaration.

Function declaration имеет механизм "поднятия" (hoisting).
Это означает, что функция "поднимается" в области видимости и доступна для вызова до своего объявления.

## Задание 2

###### Ответ:

[Решение в песочнице Vue 3 composition api](https://play.vuejs.org/#eNqNUU1v1DAQ/Ssjn0Bq4kI5RQsqoB7gAAg4+hLi2a3b+EPjSbpotf+didNdwtJWlaLYM/M8896bnXqfUj0OqBq1yh25xO9MwG2KxGBx3Q49w84EANty++LlfAcg5IHCIQLo4hC4gdfnc2I/HfKTb6Xv2wKYICGjT33LKGMAjhGM1TrSW6McuDB3MwqaW/w95YwqaMFbNwrUrQtyBa/OpbTbgYP9fqWlOHfViyGLQJ0p5ydllW9TfZNjENVFgnQrhWxUcxBllNgyxUZdM6fcaN3ZIM8s9m6kOiDrkLy+FJgmIew8Vjb6y4v6on4jZDIv0zVmX/2ieJeRpIlRZ4sxWpIjUkUYLBLSc8eePFuOPin9N/6wITGFcxfD2m1OLOmiT65H+prYxfCvNW3fx7vPJcc04FFLd43d7QP5m7ydNX0jLMwW+rmlDcq6p/LVjy+4lfux6KMd+vs1PFL8jjn2w8Rxhn0YghXaC1xh+6ls2IXNz3y1ZQz5IGoiWtwo+LKPj09I/0tX3D66uP8DRC4XFw==)

```vue
<script>
export default {
    data() {
        return {
            count: 20
        }
    }
}
</script>

<template>
    <template v-for="i in count" :key="i">
        <div v-if="i < 10">{{ i }}</div>
    </template>
</template>
```

## Задание 3

###### Ответ:

```js
const resources = [
    {
        id: 1,
        count: 13
    },
    {
        id: 2,
        count: 5
    },
    {
        id: 3,
        count: 24
    },
    {
        id: 4,
        count: 101
    },
    {
        id: 5,
        count: 72
    },
    {
        id: 6,
        count: 64
    },
    {
        id: 7,
        count: 305
    },
    {
        id: 8,
        count: 67
    },
    {
        id: 9,
        count: 95
    },
    {
        id: 10,
        count: 21
    },
    {
        id: 11,
        count: 37
    }
]

/** @param {{id: number, count: number}[]} resources */
function parseResources(resources) {
    if (!resources.length) return

    const result = {}

    for (const { id, count } of resources) {
        result[id] = count
    }

    return result
}

console.dir(parseResources(resources))
```
