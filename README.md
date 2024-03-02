Ссылка на демо  https://alarma1.github.io/vue-mib-demo/#/  
Ссылка на исходники https://github.com/Alarma1/vue-mib
# Компонент **ControlElement**

Этот компонент представляет собой кнопку, которая может менять своё состояние (активное/неактивное).
## Использование

```sh
<template>
    <div>
        <ControlElement :quatrainData="data" @eventButtonClick="handleButtonClick"/>
    </div>
</template>

<script>
import ControlElement from './components/ControlElement.vue';

export default {
    components: {
        ControlElement
    },
    data() {
        return {
            data: {
                id: 1,
                hide: false
            }
        }
    },
    methods: {
        handleButtonClick(id) {
            console.log('Нажата кнопка с id:', id);
        }
    }
};
</script>
```

## Props

**quatrainData**  
Тип: **Object**  
Описание: Данные, используемые для отображения и управления состоянием кнопки.  
Поля:  
**id**: Идентификатор элемента.  
**hide**: Флаг, указывающий текущее состояние кнопки (активное/неактивное).
  
# Компонент **PoemText**

Этот компонент отображает текст четверостишия.

## Использование

```sh
<template>
    <div>
        <PoemText :quatrain="quatrain"/>
    </div>
</template>

<script>
import PoemText from './components/PoemText.vue';

export default {
    components: {
        PoemText
    },
    data() {
        return {
            quatrain: "Текст четверостишия..."
        }
    }
};
</script>
```

## **Props**

**quatrain**  
Тип: **String**  
Описание: Текст четверостишия.

# Инструкции для создания продакшена vue3+vite

## 1. Сборка проекта:
- Запустите сборку вашего приложения с помощью команды: npm run build
Это создаст собранную версию приложения в папке `dist`.

## 2. Развертывание на сервере:
- Перенесите содержимое папки `dist` на сервер.

## 3. Настройка маршрутизации:
- Все запросы необходимо маршрутизировать на фаил `index.html`.


