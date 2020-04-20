# Vue template style rules

- Пробелы в интерполяции `{{ var }}`
- У пустого тега пробел перед закрывающим `/>`
- Настройка wrap-а строки в шторме - 150 символов, мониторы у всех уже не 1024х768
- Перенос аттрибутов в теге шаблона, если они не влезают по длинне и перенос закрывающей `>`. Делается для стандартизации строк, можно удалить любую или добавить в конце и без добалвения лишнего диффа.
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
