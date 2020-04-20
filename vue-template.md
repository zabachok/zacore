# Vue template style rules

1. Пробелы в интерполяции `{{ var }}`
1. Настройка wrap-а строки в шторме - 150 символов, мониторы у всех уже не 1024х768
1. Перенос аттрибутов в теге шаблона, если они не влезают по длинне
Пример:
```html
<div class="relative-tags" :id="'relative-tags-' + sectionKey">
  <router-link
    :to="{name: 'EventList', params: {tagId: tag.id}}"
    v-for="(tag, tagKey) in section.tagLinks"
    :key="tag.id"
    :id="'relative-tag-' + sectionKey + '-' + tagKey"
    class="btn btn-light"
  >
    {{ tag.name }}
  </router-link>
</div>
```
1. У пустого тега пробел перед закрывающим `/>`
