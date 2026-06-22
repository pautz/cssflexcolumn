# cssflexcolumn
tutorial css seleciona colum bota flex na coluna 0 os 3 né´, e box4 na colum flex 1

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
