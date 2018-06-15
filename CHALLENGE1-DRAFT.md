## Metrics Panel


You are in charge of developing a brand new _metrics_ area as part of a dashboard(WobblyPanel) offered by your company as companion to their main product, an e-commerce site(WobblyStore).


This new area main requirements are:

- [ ] It should display a `<graphic>` based on the transactions made through WobblyStore.
  - This should include the average ticket amount.
  - Should allow viewing data per day/month/year
- [ ] It should support changing the range from which the graphics data is generated.
- [ ] It should allow to export those graphics as (excel || json || csv) files.

On the server side, you'll need to support several options to provide the frontend with the info it requires. For that, we'll provide a set of [tests](#tests) that we will run against your proposed API.


### Transaction structure


orderId|productId|total|paymentMethodId|createdAt|deletedAt
---|---|---|---|---|---
1|PR001|102.50|2|timestamp|timestamp

### Suggested technologies to approach this challenge

**Frontend**:
- ReactJs
- For styling:
  - CSS, SASS, LESS, etc
  - Styled Components
  - Emotion
  - Radium
- For state management:
  - Plain old `setState`
  - Unstated
  - Redux
- For data fetching:
  - Plain old `fetch`
  - `axios`
  - firebase
- For bundling:
  - `create-react-app`
  - `parcel`
  - `webpack`

**Backend:**
- Express
  - body-parser
- Sequelize
- Mongoose
- Firebase


### Resources
  * WIP

### Tests

This is an example of a test that will be run against your API.

```js
describe('Orders', () =>
  it('should list all orders', async () => {
  const fetchResponse = await fetch(API)
  const { orders } = await fetchResponse.json ()
  
  expect(orders.length).toBe(100)
  })
})
```
