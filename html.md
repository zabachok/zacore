# Оформление html кода

## Верстка 
1. В html не оставляем пустых строк между блоками  
1. Инъекции php абзацев выделяем пустой строкой перед и после абзаца  
1. Echo вставки `<?= ?>` не выделяем
    
## Пример:

```html
<div class="container">
    <div class="row">
        <div class="col-12">
            <div class="text-muted">
                <div class="btn-group float-right">
                    <div class="btn btn-danger d-none" >
                        <span class="fas fa-times"></span>
                    </div>
                    <div class="btn btn-warning">
                        <i class="fas fa-gavel"></i>
                    </div>
                </div>
                Категория
            </div>
       
            <?php if ($category): ?>
                <?= $category->name ?>
            <?php else: ?>
                <div class="text-danger">
                    Категория не указана
                </div>
            <?php endif; ?>
       
            <div class="text-danger d-none">
                <span class="reason-text"></span>
                <span class="fas fa-times" style="cursor: pointer;"></span>
            </div>
        </div>
    </div>
</div>
```  
