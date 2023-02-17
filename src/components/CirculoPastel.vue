<script>
function Suma() {

    var checkboxes = form1.checkbox; 
    let dato = checkboxes.length;
    let valor = 100/checkboxes.length;
    let porcentaje = 0;

    for (var x=0; x < checkboxes.length; x++) {
    if (checkboxes[x].checked) {
    porcentaje = porcentaje +valor
    }

    }

    porcentaje=porcentaje.toPrecision(3) //Redondea el resultado


    ValorPantalla.innerText = 'AVANCE: ' + porcentaje + " %";

    var miPastel=function(canvasId,width,height,valores) {
    this.canvas=document.getElementById(canvasId);;
    this.canvas.width=width;
    this.canvas.height=height;
    this.radio=Math.min(this.canvas.width/2,this.canvas.height/2)
    this.context=this.canvas.getContext("2d");
    this.valores=valores;
    this.tamanoDonut=0;

    /**
     * Dibuja un gráfico de pastel
     */
    this.dibujar=function() {
        //his.total=this.getTotal();
        var total=100;
        var valor=0;
        var inicioAngulo=0;
        var angulo=0;

        // creamos los quesos del pastel
        for(var i in this.valores)
        {
        valor=valores[i]["valor"];
        color=valores[i]["color"];
        angulo=2*Math.PI*valor/total;

        this.context.fillStyle=color;
        this.context.beginPath();
        this.context.moveTo(this.canvas.width/2, this.canvas.height/2);
        this.context.arc(this.canvas.width/2, this.canvas.height/2, this.radio, inicioAngulo, (inicioAngulo+angulo));
        this.context.closePath();
        this.context.fill();
        inicioAngulo+=angulo;
        }
    }


    /**
     * Function que devuelve la suma del total de los valores recibidos en el array
     */
    


    }

    // definimos los valores de nuestra gráfica
    var numer=porcentaje
    var numer2=100-porcentaje
    console.log(numer2)

    var valores={
    
    "CON":{valor:numer,color:"blue"},
    "SIN":{valor:numer2,color:"red"}
    }



    // generamos el primer pastel
    var pastel=new miPastel("canvas1",400,400,valores);
    pastel.dibujar();
    pastel.ponerPorCiento("white");
    pastel.ponerLeyenda("leyenda1");

}
</script>

<template>
   <div class="  text-3xl fixed left-1/2 top-20 font-bold">
         <label id="ValorPantalla" for="">AVANCE: 0 %</label> 
        </div>
        <div class="fixed left-1/2 top-40">
          <canvas id="canvas1"></canvas>
          <div><p class="font-bold text-lg">Azul= avance</p></div>
    </div>
    

</template>