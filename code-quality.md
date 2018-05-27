```js
// it works
componentWillReceiveProps (nextProps) {
  if (nextProps.data.isLoading && !this.props.data.isLoading) {
    console.log('let\'s rock!')
  }
}

// it works and it's readable
componentWillReceiveProps (nextProps) {
  const dataIsLoaded = (
    nextProps.data.isLoading &&
    !this.props.data.isLoading
  )
  if (dataIsLoaded) {
    console.log('let\'s rock!')
  }
}
```