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
  </div>
   <div class="containercolumn">
       <div class="containerrow">
  <div class="box box4">Caixa 4</div></div></div>

<style>.container {
  display: flex;
  flex-direction: row; /* organiza em linha */
  align-items: flex-start;
  height: 600px;
  background: #222;
  padding: 10px;
  gap: 10px;
}

.containerrow {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  height: 600px;
  width: 100%;
  background: #222;
  padding: 10px;
  gap: 10px;
}

.containercolumn {
  display: flex;
  flex-direction: column; /* organiza em coluna */
  align-items: flex-start;
  height: 600px;
  background: #333;
  padding: 10px;
  gap: 10px;
}

.box {
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 6px;
  font-weight: bold;
  flex: 1;          /* cada box ocupa espaço proporcional */
  min-width: 0;     /* evita overflow do conteúdo */
}

.box1 { background: crimson; }
.box2 { background: teal; }
.box3 { background: goldenrod; }
.box4 { background: purple; } /* ocupa toda largura disponível */
</style>
