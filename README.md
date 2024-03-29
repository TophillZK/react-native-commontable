
# React Native Common Table

<p align="center">
  <img src ="https://github.com/TophillZK/react-native-commontable/blob/master/Example.png" />
</p>

## Getting started
```bash
yarn add react-native-commontable
```

## Usage
```javascript
import React from "react";
import {
  View,
  StyleSheet
} from "react-native";

import CommonTable from 'react-native-commontable';

export default class App extends React.Component {
  constructor(props) {
    super(props);

    this.backSourceHeader = ['Name', 'Sex', 'Age'];
    this.backSourceData = [
      ['Jack', 'Male', '24'],
      ['Rose', 'Female', '22']
    ];
  }

  render() {
    return (
      <View style={styles.container}>
        <CommonTable tableHeader={this.backSourceHeader} tableData={this.backSourceData}/>
        <CommonTable tableHeader={this.backSourceHeader} tableData={this.backSourceData}
            tableHeaderStyle={{backgroundColor:'#677ca0'}}
            textHeaderStyle={styles.normalTextWhite}
            tableDataStyle={{backgroundColor:'#d4d8e9'}}
            textDataStyle={styles.middleText}
        />
        <CommonTable tableHeader={this.backSourceHeader} tableData={this.backSourceData} tableWidth={300}/>
        <CommonTable tableHeader={this.backSourceHeader} tableData={this.backSourceData} columnsWidth={[150,100,50]}/>
        <CommonTable tableHeader={this.backSourceHeader} tableData={this.backSourceData} borderWidth={3} borderColor='red'/>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff'
  },
  normalTextWhite: {
    color: '#FFFFFF',
    fontSize: 18
  },
  middleText: {
    color: '#121917',
    fontSize: 18
  },
});
```
### Component props
| Prop | Required | Type | default | description |
| ---- | ---- | ----| ---- | ---- |
| tableHeader | YES | array | none | Table header array |
| tableData | YES | array | none | Table data array,two-dimensional array [[]] |
| columnsWidth | NO | array | none | Column width,if set,tableWidth does not work |
| tableWidth | NO | number | none | Table width,if columnsWidth and tableWidth is null,Table width=screen width |
| tableHeaderStyle | NO | array or object | none | |
| textHeaderStyle | NO | array or object | none | |
| tableDataStyle | NO | array or object | none | |
| textDataStyle | NO | array or object | none | |
| borderWidth | NO | number | 1 | |
| borderColor | NO | string | #121917 | |
