# Wanilla JS

A easy to use vanilla library to create components like Vue JS and React JS.


```
import component from 'wanilla-js'

function Button() {
  component.call(this,{
    template: 
    `<li class="itemList">
      <span>Hola a todos</span>
    </li>`,
    components: []
  })
}

function Cta() {
  component.call(this,{
    template: 
    `<Button class="container">
      <Button>
      </Button>
      <Button class="rojo">
      </Button>
    </Button>`,
    components: [
      Button
    ]
  })
}

var btnLogin = new Button()
console.log(btnLogin.node)

var btnLogin = new Cta()
console.log(btnLogin.node)
```

Results in console:

Button component:
```
<li class="itemList">
  <span></span>
</li>
```

Cta component:
```
<li class="container itemList">
  <span></span>
  <li class="itemList">
    <span></span>
  </li>
  <li class="itemList">
    <span></span>
  </li>
</li>
```