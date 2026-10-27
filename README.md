# Unified DevTools Plugin Registry

Official community plugin registry for **React Native Desktop DevTools** and **react-native-unified-devtools**.

## Available Plugins

| Plugin | ID | Description |
|---|---|---|
| **MMKV Storage** | `mmkv` | Live key-value viewer and modifier for `react-native-mmkv` |
| **AsyncStorage** | `async_storage` | Serialized storage explorer for `@react-native-async-storage/async-storage` |
| **Feature Flags** | `feature_flags` | Remote feature flags control and A/B variant inspector |

## Adding a Plugin

To contribute a plugin to this registry:
1. Create a directory under `plugins/<plugin-id>/`
2. Add a `plugin.json` defining table `columns` and `actions`
3. Add your plugin entry to `registry.json`
4. Submit a Pull Request
