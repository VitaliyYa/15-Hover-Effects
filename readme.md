# 15 вариантов hover эффектов для сайта.
#### Под hover эффектом я подразумеваю анимацию при наведении.
Здесь изменяется цвет текста, его размер, место положения, появляются дополнительные блоки, затемняется или увеличивается фоновое изображение, появляется дополнительный текст и так далее. Каждый эффект выглядит круто.

Очень большой плюс в том, что вся структура верстки этих hover эффектов имеет адаптивную верстку.

Подключаются все эти эффекты одними css файлами. И чтобы эффекты заработали нужно:

Для включения адаптивной верстки в <head> нужно вставить:

```HTML
<meta http-equiv="X-UA-Compatible" content="IE=edge"> 
<meta name="viewport" content="width=device-width, initial-scale=1">
```

Следом подключить css файлы:
```html
<link rel="stylesheet" href="css/normalize.css" />
<link rel="stylesheet" href="css/demo.css" />
<link rel="stylesheet" href="css/component.css" />
```

В самый низ сайта нужно вставить следующий javascript:

```html
  <script>
      [].slice.call( document.querySelectorAll('a[href="#"') ).forEach( function(el) {
          el.addEventListener( 'click', function(ev) { ev.preventDefault(); } );
      } );
  </script>
```

Ну а туда, где вы хотите видеть любой из hover эффектов вставляете html код (например effect-lily):
```html
<div class="container">
  <div class="grid">
    <figure class="effect-lily">
      <img src="img/1.jpg" alt="img01"/>
      <figcaption>
        <h2>Nice
          <span>Lily</span>
        </h2>
        <p>Lily likes to play with crayons and pencils</p>
        <a href="#">View more</a>
      </figcaption>
    </figure>
  </div>
</div>
<!-- /container -->
```
Вот и все, css эффекты подключены, теперь вы можете менять эффекты и смотреть какой подойдет лучше.
