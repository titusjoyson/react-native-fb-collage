# react-native-fb-collage
A package to make collage for react native.

## Show Cases

| **IOS** | **Android** |
| :---------------------------------- | :------------------------------------ |
| ![](https://raw.githubusercontent.com/meharbhutta/react-native-fb-collage/master/demo/screenshot-ios.png) | ![](https://raw.githubusercontent.com/meharbhutta/react-native-fb-collage/master/demo/screenshot-android.png) |

## Getting Started

### Installation

```bash
npm i react-native-fb-collage --save
```

### Basic Usage

- Install react-native-cli first

```bash
$ npm install -g react-native-cli
```

### Note: [GUIDE](https://facebook.github.io/react-native/docs/getting-started)

- Initialization of a react-native project

```bash
$ react-native init AwesomeProject
```

- Then, edit `AwesomeProject/App.js`, like this:

```typescript
import { View } from 'react-native';
import FBCollage from 'react-native-fb-collage';

export default class App extends React.Component {
    render: function() {
        return (
            <View visible={true} transparent={true}>
                <FBCollage 
                  images={[
                      // static image using require.
                      //require('../assets/image-file.ext')
                      //OR
                      //{uri: 'https://imageURL...'}
                      //for Example
                      { uri: 'https://www.inovex.de/blog/wp-content/uploads/2018/03/react-native-800x450.png' },
                      { uri: 'https://www.inovex.de/blog/wp-content/uploads/2018/03/react-native-800x450.png' },
                      { uri: 'https://www.inovex.de/blog/wp-content/uploads/2018/03/react-native-800x450.png' },
                      { uri: 'https://www.inovex.de/blog/wp-content/uploads/2018/03/react-native-800x450.png' },
                      { uri: 'https://www.inovex.de/blog/wp-content/uploads/2018/03/react-native-800x450.png' },
                      { uri: 'https://www.inovex.de/blog/wp-content/uploads/2018/03/react-native-800x450.png' },
                      { uri: 'https://www.inovex.de/blog/wp-content/uploads/2018/03/react-native-800x450.png' }
                  ]}
                  imageOnPress={() => {}}
                />
            </View>
        )
    }
}
```

### Props

| parameter | type  | required | description | default |
| :--------------------- | :------------------------------------------------------------------------------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------- |
| images | array | yes | The array of image sources of <br> require('../image-file') <br> or <br> { uri: 'imageURL'} <br> or <br> both    |  |
| imageOnPress | function<br>`(index, images) => void` | no | The callback for image on press listener | `() => {}` |
| width | number | no | The width of the view | `357` |
| height            | number                                                                                 | no       | The height of the view                                                                                                                                                                | `200`                                                     |
| borderRadius                  | number                                                                                 | no       | The border radius of the images                                                                                                                                                                                                                 | `12`                                                       |
| spacing        | number                                                  | no       | The spacing between the images and the view                                                                                                                                                                                                                 | auto                                                      |
| resizeMode          | string                                        | no       | [visit me](https://facebook.github.io/react-native/docs/image#resizemode) for resize mode                                                                                                                                                                                    | `cover`                                              |
| style         | object                                              | no       | To override the main view style                                                                                                                                                                                                      | default                                                |
| overlayStyle               | object                                              | no       | To override the text view overlay style                                                                                                                                                                                                              | default                                                |
| textStyle                 | object                | no         |       To override the text style                                                                                             | default      |
## Development pattern

### Step 1, run TS listener

After clone this repo, then:

```bash
npm install
npm start
```

### Step 2, run demo

```bash
cd demo
npm install
react-native run-android (For android)
react-native run-ios (For ios)
```

#### In case of any issue follow the [GUIDE](https://facebook.github.io/react-native/docs/getting-started).