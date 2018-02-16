## Dialog
  
A partir do html5.2 é possível usar o `dialog` nativamente no html sem o uso de bibliotecas.  

> Só está funcionando no Chrome por enquanto.    
  
Ele fica oculto inicialmente, e pode ser mostrado com o método `show()` para mostrar e o método `close()` para fechar. Ambos executados através do JavaScript.  
  
Também existe o método `showModal()` que mostra o dialogo, porém, todo o fundo do documento fica indisponível para clicarmos.  
  
O `dialog` aceita todos os atributos globais e também o atributo `open` que é um booleano. Se o `open` não estiver omitido, o dialogo será aberto por padrão.  
  
No css temos o pseudo-elemento `::backdrop` para estilizar a parte de trás do modal, que fica inacessível.  
  
### Exemplo
  
```html
<!DOCTYPE html>
<html lang="pt-BR">
<body>
    <dialog open id="cx_dialog">
        <h1>Olá Mundo!!</h1>
        <button id="fechar_modal">Fechar Modal</button>
    </dialog>

    <button id="abrir">Abrir</button>
    <button id="abrir_modal">Abrir Modals</button>
    <button id="fechar">Fechar</button>

    <script>
        const caixa_dialog = document.querySelector("#cx_dialog")

        document.querySelector("#abrir").addEventListener("click", () => {caixa_dialog.show();});
        document.querySelector("#abrir_modal").addEventListener("click", () => {caixa_dialog.showModal();});
        document.querySelector("#fechar").addEventListener("click", () => {caixa_dialog.close();});
        document.querySelector("#fechar_modal").addEventListener("click", () => {caixa_dialog.close();});
    </script>
</body>
</html>
```

### Referências
  
[Treina Web](https://www.treinaweb.com.br/blog/novidades-html-5-2/)
[Microsoft - Andamento do Dialog](https://developer.microsoft.com/en-us/microsoft-edge/platform/status/dialogelementformodals/)
[CanIUse.com - Andamento do Dialog](https://caniuse.com/#feat=dialog)  

