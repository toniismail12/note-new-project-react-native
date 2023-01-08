## create new project react native
<ul>
  <li>Setup React Native CLI</li>
  <li>npx react-native init AwesomeProject</li>
</ul>

## install package

### React Navigation
<ul>
  <li>npm install @react-navigation/native </li>
  <li>npm install react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/masked-view </li>
  <li>npm install @react-navigation/stack</li>
  <li>npm install @react-navigation/bottom-tabs <li/>
</ul>

### react native svg
<ul>
  <li>npm install react-native-svg</li>
  <li>npm install react-native-svg-transformer</li>
</ul>

### update metro.config.js with it

```javascript
const { getDefaultConfig } = require("metro-config");

module.exports = (async () => {
  const {
    resolver: { sourceExts, assetExts }
  } = await getDefaultConfig();
  return {
    transformer: {
      babelTransformerPath: require.resolve("react-native-svg-transformer")
    },
    resolver: {
      assetExts: assetExts.filter(ext => ext !== "svg"),
      sourceExts: [...sourceExts, "svg"]
    }
  };
})();
```

### react native command run project
<ul>
  <li>npx react-native start</li>
  <li>npx react-native run-android</li>
</ul>
