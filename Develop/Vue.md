# Vue

Vue es un framework ligero que se puede utilizar directamente desde su CDN como React o Angular, o tambien instalando y creando un proyecto grande, simplemente se puede añadir la siguiente   dependencia al encabezado html
```HTML
<script src="https://cnd.jsdelivr.net/npm/vue@2"></script>
```
## Estructura

La estructura de vim hasta el momento de desarrollo que se maneja es el siguiente.

archivo.html => base en donde se llamara o tendrá los componentes.
el archivo js en donde tendrá las instrucciones de javascript, esta se puede alojar a una carpeta, /js/init.js, dentro tendra la estructura de Vue (tipo JSON) que es la siguiente, para mas detalle consultar las paginas de cada atributo.

```Vue
let content= new Vue(				=> objeto de vue

components:{					=> componentes a utilizar
},

data(){						=> datos que se esperan obtener, es como un modelo
},

mounted() {					=> afecta al DOM
},

methods:{					=> contiene los metodos o funciones
},

watch:{						=> Observable
}

);
```

