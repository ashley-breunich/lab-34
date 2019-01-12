![CF](http://i.imgur.com/7v5ASc8.png) LAB
=================================================

## Lab 34 - Remote CRUD

### Author: Ashley Breunich

### Links and Resources
* [repo](https://github.com/ashley-breunich/lab-34)
* [codesandbox.io link](https://codesandbox.io/s/2381wz3vkp)

### Modules
#### `index.js`
##### Exported Values and Methods

###### `Main()`
--> App Component

The app component is wrapped in the store allowing the entire program to have access to Redux.


#### `components/app.js`
##### Exported Values and Methods

###### `CLASS App`
--> h2 Component

--> RecordList Component


#### `store/index.js`
##### Exported Values and Methods

###### `store()`
--> createStore() with the reducers


#### `store/middleware/reporter.js`
##### Exported Values and Methods

###### `export default`
<-- store, next, action

--> results || err depending on try catch


#### `components/record/actions.js`
##### Exported Values and Methods

###### `getAll()`
<-- model, dispatch

--> dispatch(runGetAll())

###### `runGetAll()`
<-- payload

--> type: 'GET'

--> payload

###### `postResource()`
<-- model, payload

--> dispatch(runPost())

###### `runPost()`
<-- payload

--> type: 'POST'

--> payload

###### `destroy()`
<-- payload

--> type: 'DELETE'

--> payload

###### `put()`
<-- payload

--> type: 'PUT'

--> payload


#### `components/record/list.js`
##### Exported Values and Methods

###### `CLASS Records`
Sets the state - { id: null }

--> button 

--> ul tag

--> Record Component

###### `componentDidMount()`
Runs when the component loads

--> this.props.model

###### `deleteRecord()`
<-- id

--> this.props.handleDelete()

###### `editRecord()`
<-- id

Sets the state - id 

###### `reset()`
Sets the state - id to null

###### `mapStateToProps()`
<-- state

--> records

###### `mapDispatchToProps()`
<-- dispatch, getState

--> handlePost

--> getAll

--> handleDelete


#### `components/record/record.js`
##### Exported Values and Methods

###### `CLASS Record`
Sets the state - { id: null, schema: {} }

--> h3 

--> Form

###### `componentDidMount()`
This runs when the component loads

Sets the state - { schema: data.body }

###### `resetPlayer()`
<-- id
Sets the state - id to null

###### `handleSubmit()`
<-- form

--> handlePut() || handlePost()

###### `mapStateToProps()`
<-- state

--> records

###### `mapDispatchToProps()`
<-- dispatch, getState

--> handlePost

--> handlePut

--> handlePatch

--> getSchema


#### `components/record/reducers.js`
##### Exported Values and Methods

###### `export default
<-- state, action 

<-- type 

--> appropriate state in some from depending on case


#### Tests
* What assertions were made?
* What assertions need to be / should be made?

#### UML
Link to an image of the UML for your application and response to events
