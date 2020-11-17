# week5_day2

>
> Axios
>


## Main points: Axios

- <a href="https://www.npmjs.com/package/axios">Axios</a> es una librería que permite gestionar llamadas de AJAX (GET, POST, PUT, DELETE)
- Instalación: mediante Node `npm i axios` o a través de CDN:
  ````html
  <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
- Axios dispone de cuatro métodos para realizar peticiones asíncronas al servidor:
  ````javascript
  axios.get("url")
  axios.post("url", data)
  axios.put("url", data)
  axios.delete("url")
  ````
- Es posible implementar Axios a través de la creación de una app de Axios dotada de un `baseURL` sobre el que aplicar cada verbo con su *endpoint*:
  ````javascript
  const axiosApp = axios.create({baseURL: 'https://www.elservidor.com/api'})
  axiosApp.get('/registros`)      // Realiza petición GET a https://www.elservidor.com/api/registros
  ````
- Todas las peticiones de Axios son resultas mediante promesas que retronan un objeto que almacena la respuesta del servidor bajo su propiedade `data`:
  ````javascript
  axios
    .get("url")
    .then(response => console.log('La respuesta del servidor es ', response.data)
    .catch(err => console.log(err))
  ````

## Main points: formularios asíncronos
El método `.preventDefault()` del objeto `event` permite anular el envío clásico de un formulario para gestionarlo mediante AJAX:
  ````javascript
  formObject.onsubmit = e => e.preventDefault()
  ````


