# Unified DevTools Plugin Registry

Official community plugin registry for **React Native Desktop DevTools** and **react-native-unified-devtools**.

## Supported Plugins

| Plugin | ID | Mobile Export | Description |
|---|---|---|---|
| **React Native MMKV** | `mmkv` | `@archie-dev/react-native-core/plugin-mmkv` | Live key-value viewer and modifier for `react-native-mmkv` |
| **AsyncStorage Explorer** | `async_storage` | `@archie-dev/react-native-core/plugin-async-storage` | Serialized storage explorer for `@react-native-async-storage/async-storage` |

---

## Quick Usage in React Native

Pass your storage instance into `initDevTools`:

```typescript
import { initDevTools } from '@archie-dev/react-native-core';
import { mmkvPlugin } from '@archie-dev/react-native-core/plugin-mmkv';
import { asyncStoragePlugin } from '@archie-dev/react-native-core/plugin-async-storage';
import { MMKV } from 'react-native-mmkv';
import AsyncStorage from '@react-native-async-storage/async-storage';

const storage = new MMKV();

initDevTools({
  plugins: [
    mmkvPlugin(storage),
    asyncStoragePlugin(AsyncStorage),
  ],
});
```

---

## Contributing a Plugin

1. Create a directory under `plugins/<plugin-id>/`
2. Add a `plugin.json` defining table `columns` and `actions`
3. Add your plugin entry to `registry.json`
4. Submit a Pull Request
