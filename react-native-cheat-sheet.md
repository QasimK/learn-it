# React Native Cheat Sheet

## Stateless Components

This demonstrates an ES6-React stateless component which has specified `propTypes`, `defaultProps`, child components with style specified.

```
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
