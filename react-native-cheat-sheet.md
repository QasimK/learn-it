# React Native Cheat Sheet

## Stateless Components

This demonstrates an ES6-React stateless component which has specified `propTypes`, `defaultProps`, child components with style specified.

```jsx
import React, { PropTypes } from 'react';
import {
  Text,
  View,
  Image,
} from 'react-native';


export const Blocky = ({
  secondtext='Indeed-ee-oh',
  pic={
    uri: 'https://upload.wikimedia.org/wikipedia/commons/d/de/Bananavarieties.jpg',
  },
}) => (
  <View>
    <Text>
      Yep that is me
    </Text>
    <Text>
      {secondtext}
    </Text>
    <Image source={pic} style={{width: 193, height: 50}}/>
  </View>
);

Blocky.propTypes = {
  secondtext: PropTypes.string,
  pic: PropTypes.string,
};
```

Usage

```
<Blocky></Blocky>
<Blocky secondtext="Yeah2"></Blocky>
```


## Appendix

- [**Stateless Components**, Redux, Testing](https://camjackson.net/post/9-things-every-reactjs-beginner-should-know)
- [Stateful Components](http://egorsmirnov.me/2015/06/14/react-and-es6-part2.html)
- [Higher Order Components (Mixins)](http://egorsmirnov.me/2015/09/30/react-and-es6-part4.html)
