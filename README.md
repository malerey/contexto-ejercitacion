# Contexto - ejercitación

Para practicar Contexto, haremos una aplicacion muy sencilla que imite a instagram. 


![img](https://www.robinwieruch.de/static/611b371f42ff49efaad46bc4464f7341/a9a89/stylagram.webp)

1. Crear un proyecto nuevo de create-react-app
2. Crear tres componentes (como mínimo: si necesitan mas, haganlo!): 
  * Barra de navegacion
  * Informacion de perfil
  * Seccion con las fotos
  
3. No es necesario el estilado

4. Para la foto de perfil, usen una imagen de su computadora. Recuerden las diferencias entre trabajar con imagenes locales y con imagenes sacadas de internet en React :) 
  
5. Las fotos deben hacerse recorriendo el siguiente array de objetos. Como ven, hay mucha informacion en los objetos que por ahora no usaremos (por ahora solo usamos las imagenes). Eso es normal trabajando con data de un fetch. Ignoren toda la info que no necesiten. 

```js
const feedsource = [
  {
    source: 'https://www.viajejet.com/wp-content/viajes/una-laguna-unica-en-jamaica-650x366.jpg',
    likes: '43',
    comments: '3',
    id: 0,
  },
  {
    source: 'https://www.viajejet.com/wp-content/viajes/los-arrecifes-de-coral-de-bunaken-indonesia-650x366.jpg',
    likes: '313',
    comments: '10',
    id: 1,
  },
  {
    source: 'https://www.viajejet.com/wp-content/viajes/paisaje-nevado-en-el-parque-nacional-deogyusan-corea-del-sur-650x366.jpg',
    likes: '29',
    comments: '2',
    id: 2,
  },
  {
    source: 'https://www.viajejet.com/wp-content/viajes/un-paisaje-de-vertigo-en-ronda-malaga-espana-650x366.jpg',
    likes: '18',
    comments: '2',
    id: 3,
  },
  {
    source: 'https://www.viajejet.com/wp-content/viajes/El-increible-paisaje-de-Semuc-Champey-Guatemala-650x366.jpg',
    likes: '30',
    comments: '4',
    id: 4,
  },
];
```


6. Una vez hecha la aplicacion, queremos agregar debajo de cada foto un boton para "dar like".

7. Para dar like, un usuario debe estar logueado. Agreguemos en la barra de navegacion un boton que diga "Iniciar sesion". 

8. Si el usuario inicio sesion, veremos un nombre cualquiera en la barra de navegacion. Si el usuario esta logueado, vera la cantidad de likes que tiene una foto. Si no esta logueado, esa informacion permanece oculta. Cuando el usuario de like a una foto, el contador subira 1 para esa foto. 

9. Si el usuario no inició sesión, el boton de "dar like" se sigue mostrando, pero al hacerle click debe aparecer un error en forma de modal que diga "Para dar like, iniciá sesión". 

La informacion sobre si el usuario esta logueado o no debe estar guardada en un estado global con Contexto. Debe ser consumida tanto por las fotos - para mostrar los likes - como por la barra de navegacion. Todo el resto de la informacion puede estar en un estado local. 
