# cssflexcolumn

Tutorial simples de **CSS Flexbox em coluna**.  
Neste exemplo, configuramos o container para usar `flex-direction: column` e controlamos o crescimento das caixas no eixo Y:

- **Box1, Box2 e Box3** → `flex: 0` (não crescem, ficam apenas com a altura do conteúdo).  
- **Box4** → `flex: 1` (cresce e ocupa todo o espaço restante no eixo Y).  

---

## Estrutura HTML

```html
<div class="container">
  <div class="box box1">Caixa 1</div>
  <div class="box box2">Caixa 2</div>
  <div class="box box3">Caixa 3</div>
  <div class="box box4">Caixa 4</div>
</div>

.container {
  display: flex;
  flex-direction: column; /* eixo principal = Y */
  height: 600px;          /* altura total do container */
}

.box {
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}

.box1 { background: crimson; flex: 0; }
.box2 { background: teal; flex: 0; }
.box3 { background: goldenrod; flex: 0; }

.box4 { background: purple; flex: 1; } /* ocupa todo eixo Y */
