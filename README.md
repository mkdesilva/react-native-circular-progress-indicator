# react-native-circular-progress-indicator

![platforms](https://img.shields.io/badge/platforms-Android%20%7C%20iOS-brightgreen.svg?style=flat&colorB=191A17)
[![Version](https://img.shields.io/npm/v/react-native-circular-progress-indicator.svg)](https://www.npmjs.com/package/react-native-circular-progress-indicator)
[![NPM](https://img.shields.io/npm/dm/react-native-circular-progress-indicator.svg)](https://www.npmjs.com/package/react-native-circular-progress-indicator)

A simple and customizable React Native circular progress indicator component. 

![](demo.gif)
![](demo2.gif)
![](demo3.gif)

## Prerequisites

This component has a peer dependency on react-native-svg to draw the countdown circle. react-native-svg has to be installed and linked into your project.
Follow [react-native-svg](https://www.npmjs.com/package/react-native-svg#installation) to install the dependency.

## Installation

 Supported version: react-native >= 0.59.0

  ```
  npm install react-native-circular-progress-indicator
  ```
  
  or
  
  ```
  yarn add react-native-circular-progress-indicator
  ```
  
## Example
```
import CircularProgress from 'react-native-circular-progress-indicator';

....

<CircularProgress value={58} />
<CircularProgress
 value={60}
 radius={120}
 strokeWidth={15}
 duration={2000}
 color={'#2ecc71'}
 textColor={'#ecf0f1'}
 maxValue={200}
/>
<CircularProgress
 value={60}
 strokeWidth={12}
 textColor={'#ecf0f1'}
/>

// with value prefix/siffix

<CircularProgress
  value={90}
  color={'#2ecc71'}
  valuePrefix={'$'}
/>

<CircularProgress
  value={85}
  color={'#2ecc71'}
  textColor={'#fff'}
  valueSuffix={'%'}
/>


// with callback function

<CircularProgress
  value={90}
  color={'#2ecc71'}
  textColor={'#fff'}
  valueSuffix={'%'}
  onAnimationComplete={() => { alert('callback') }}
/>

```
## Props
| Prop          | Description   | Type   | Default | Required |
| :-----------: |:-------------:| :-----:| :-----: | :-----: |
| value     | progress value  | Number | 0 | true |
| radius     | progress circle radius  | Number | 60 | false |
| strokeWidth     | progress circle stroke width  | Number | 10 | false |
| duration     | progress animation duration  | Number | 500 | false |
| color     | progress color | String | '#e74c3c' | false |
| delay     | progress animation delay | Number | 0 | false |
| textColor     | progress value text color | String |  | false |
| maxValue     | progress maximum value. Percentage calculation is based on the maximum value provided | String | 100 | false |
| fontSize     | progress value text font size | Number |  | false |
| outerCircleOpacity  | progress outer circle opacity value | Number | 0.2  | false |
| strokeLinecap  | progress stroke line cap | 'round' or 'butt' or 'square' | 'round' | false |
| onAnimationComplete  | callback when animation is completed. | Function | ()=>{} | false |
| valuePrefix  | prefix value | String | '' | false |
| valueSuffix  | suffix value | String | '' | false |

## License
This project is licenced under the MIT License.