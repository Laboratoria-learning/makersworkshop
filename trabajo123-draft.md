# Editor/Generador de CV's

Trabajo123, la plataforma de empleos mas grande del Perú, ha detectado en sus métricas que el 45% de las personas que postulan a un empleo, lo hacen con un CV en alguna de las siguientes situaciones:
 - está desactualizado
 - está mal organizado
 - contiene información no relevante para las empresas


Por este motivo, se han planteado la creación de un editor/generador de CV's, que tiene las siguientes características:
  - Como usuario puedo cambiar de posición solo aquellos campos que son permitidos (foto, nombre, redes sociales)
  - Como usuario puedo guardar mi CV en mi cuenta.
  - Como usuario puedo editar alguno de los CV guardados en mi cuenta.
  - Como usuario puedo exportar mi CV como imagen, PDF o JSON.
  - Como usuario puedo importar un CV exportado previamente (formato JSON)
  - Como usuario puedo generar múltiples CV's.

### Tecnologias recomendadas para este reto

 - Link a el .md de las tecnologias

### Tests

```js
test('falla cuando el archivo json importado no es el requerido', () => {
  /*
  {
    firstName: 'Linus'
  }
  */
  const fakeImportData = require ('./fake.json')
  
  const expectedKeys = ['fullName', 'email', 'shortBio']
  const actualKeys = Object.keys(fakeImportData)
  
  expect(expectedKeys).toEqual(actualKeys)
})
```
