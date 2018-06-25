## Panel de métricas


*WobblyStore* es una plataforma e-commerce, creada por Wobbly Inc.

*WobblyPanel* es un panel de administración, ofrecido como complemento a WobblyStore.

Se necesita desarrollar el área de _métricas_  para WobblyPanel, y hay ciertos requisitos mínimos a cumplir:

  - Como usuario del panel, puedo visualizar las transacciones realizadas a través de WobblyStore en un gráfico(o gráficos).
  - Como usuario del panel debo de algún modo ver el ticket promedio de las transacciones.
  - Como usuario del panel puedo filtrar los datos mostrados por día/semana/año, o seleccionar un rango de fechas.
  - Como usuario del panel soy capaz de exportar los datos visualizados en algún formato de archivo(excel, csv, etc)

Debido a la naturaleza de estos requerimientos, debes considerar que en el lado del servidor (backend) necesitarás soportar diferentes opciones(filtrado, rangos, exportacion). Y por ello es que tu implementación será puesta a prueba contra un pequeño set de tests para corroborar que todo este funcionando como se espera.


### Estructura de una transacción

```json
{
  "orderId": "order-xyz-1",
  "createdAt": "", // ISO date
  "total": 110.9,
  "transactionItems": [
    {
      "id": "some-item-1",
      "quantity": 2,
      "price": 55.45
    }
  ]
}
```

### Tecnologías/librerías sugeridas para este reto

**Frontend**:
- ReactJs
- Para estilos:
  - CSS, SASS, LESS, etc
  - Styled Components
  - Emotion
  - Radium
- Para manejo de estado:
  - Plain old `setState`
  - Unstated
  - Redux
- Para peticiones de datos:
  - Plain old `fetch`
  - `axios`
  - firebase
- Para bundling/bootstrapping:
  - `create-react-app`
  - `parcel`
  - `webpack`

**Backend:**
- Express
  - body-parser
- Sequelize
- Mongoose
- Firebase


### Recursos
  * WIP

### Tests

Este es un ejemplo muy simple de un test que será ejecutado usando tu API propuesta.

```js
const API = my-awesome-api.now.sh
test('deberia listar todas las transacciones', async () => {
  const fetchResponse = await fetch(`${API}/transacciones`)
  const { transacciones } = await fetchResponse.json()
  expect(transacciones.length).toBe(10)
})
```
