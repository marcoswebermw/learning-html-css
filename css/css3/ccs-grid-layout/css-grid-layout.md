## Css Grid Layout
  
Permite criar layouts de forma fácil.  

### Html
  
```html
<!DOCTYPE html>
<html lang="en">
<head>    
    <title>Document</title>
</head>
<body>
    <header class="o-cabecalho">Cabeçalho</header>
    <aside class="o-lateral">Lateral</aside>
    <main class="o-centro">Centro</main>
    <footer class="o-rodape">Rodapé</footer>
</body>
</html>
```   
  
### Indicando que o grid vai ficar no `body`

```css
body{
    display:grid;
}
```  
  
### Posicionando as tags com o `css-template-areas`
  
```css
body{display:grid;
        grid-template-areas:
        "header header header"
        "aside main main"
        "footer footer footer";        
}
```  
  
### Indicando onde os elementos devem ficar
  
```css
.o-cabecalho {
grid-area: header;
}

.o-lateral {
grid-area: aside;
}

.o-centro {
grid-area: main;
}

.o-rodape {
grid-area: footer;
}
```  
  
### Definindo as cores das áreas
  
```css
.o-header, .o-aside, .o-main, .o-footer {
    background: #BC20E2;
    color: #FDFDFD;
}
```  
  
### Espaçamento entre elementos
  
```css
body {
    grid-gap: 1rem;
}
```  
  
### Definindo o tamanho dos elementos

```css
body {
    grid-template-columns: auto auto auto;
    grid-template-rows: auto 100vh auto;
}
```    

### Referências
  
* [Alura](http://blog.alura.com.br/criando-layouts-com-css-grid-layout/)  
* [grid-template-columns](https://developer.mozilla.org/pt-BR/docs/Web/CSS/grid-template-columns)  
* [grid-template-rows](https://developer.mozilla.org/pt-BR/docs/Web/CSS/grid-template-rows)