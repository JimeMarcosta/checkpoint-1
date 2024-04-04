1-
Es como una versión mejorada, donde puedes definir variables para colores,
tamaños... para no tener que andar repitiendo codigo, se puede anidar selectores para que quede mas organizado. 
2-
Definen valores y se definen con $,  es como si quisiera decorar una
sala con pared azul, cojines azules.. y vas a utilizar el mismo azul, pues aqui
escribes una variable de $azul-claro para almacenarlo.
$azul-claro: #add8e6;

.cojines {
    background-color: $azul-claro;
}
.pared {
    background-color: $azul-claro;
}
3-
Esto creo que es lo mas guapo.. bloques de estilo que pueden ser re
utilizados , por ejemplo si quiero poner el mismo borde redondeado para los elementos me ahorraria repetir la misma regla.
@mixin borde-redondeado {
  border-radius: 5px;
}
Luego para reutilizarlo con @include.
.imagen {
  @include borde-redondeado;
}
.boton {
  @include borde-redondeado;
}

4-
Es como si tuviera una foto que no se el tamaño y la quiero dividir en partes iguales, en tres marcos diferentes, si asigno 1fr a cada marco, significa que cada marco recibira una tercera parte de la foto, independientemente del tamaño de la foto. Asi se pueden crear diseños fluidos y adaptables