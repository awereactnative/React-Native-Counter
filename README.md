# React-Native-Counter
# Introduction

Props

Some default props and descriptions.

| PropName   |      Description      |  type |  Default |
|----------|:-------------:|------:|------:|
| minus |  If you are not using minusIcon, it shows directly. | String | - |
| plus |  If you are not using plusIcon, it shows directly. | String | + |
| start |  The starting number | Number | 0 |
| min |    Minus the minimum selected number.   | Number |   0 |
| max | The most selectable number. | Number  | 10 |
| minusIcon | You can use it to change the minusIcon. | Function | null |
| plusIcon | You can use it to change the plusIcon. | Function | null |
| buttonStyle | You can change the types of all buttons. | Object |    {} |
| buttonTextStyle | Minus or plus styles in the button | Object |   {} |
| countTextStyle | styles of increasing number. | Object | {} |

# Demo 
![video](https://user-images.githubusercontent.com/86215353/181424099-b8cbc116-73d7-47ba-bf0b-b06a8a1a1c83.gif)

# Installation
```
This does't required any special installation of dependacies
```

# Example
```js
-
import React from 'react';
import { View, StyleSheet, Text, TouchableOpacity } from 'react-native';

const styles = StyleSheet.create({
  bg: { flex:1, paddingTop: 150, alignItems: 'center', backgroundColor: 'white' },
  less: { fontSize: 25, color: '#4d3398', fontWeight: 'bold' },
  greater: { fontSize: 25, color: '#f3845c', fontWeight: 'bold' },
  button: {
    width: 150,
    height: 50,
    alignItems: 'center',
    paddingTop: 10,
    borderRadius: 10,
    backgroundColor: '#3498db'
  },
  buttonText: {
    fontSize: 25,
    color: '#fff'
  }
});

class Counter extends React.Component {
  state = { count: 0 };

  setCount = () => this.setState(
    prevState => ({ ...prevState, count: this.state.count + 1 })
  )

  render() {
    const { count } = this.state;
    return (
      <View style={[styles.bg]}>
        <View style={{ height: 100 }}>
          <Text style={count < 5 ? styles.less : styles.greater}>You clicked {count} times</Text>
        </View>
        <View style={{ height: 100 }}>
          <TouchableOpacity style={styles.button} onPress={this.setCount}>
            <Text style={styles.buttonText}>Click</Text>
          </TouchableOpacity>
        </View>
      </View>
    );
  }
}

const App = () => (
  <Counter />
);

export default App;

```

# Tutorial

Coming Soon...
