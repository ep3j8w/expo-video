# expo-video-metadata

Provides a function that let you get some metadata from video files, like the duration, width, height, fps, codec, hasAudio, orientation, audioChannels, audioCodec, audioSampleRate etc. Check the exported types for more information. Web support is not available yet but it is planned.

# Installation in bare React Native projects

This package needs **Expo SDK 50** or **higher**, as it uses FileSystem APIs that were added in that version. This package adds native code to your project and does not work with Expo Go. Please use a custom dev client or build a standalone app.

For bare React Native projects, you must ensure that you have [installed and configured the `expo` package](https://docs.expo.dev/bare/installing-expo-modules/) before continuing (SDK 50+). This just adds ~150KB to your final app size and is the easiest way to get started and it works with and without Expo projects.

### Add the package to your npm dependencies

```
npx expo install expo-video-metadata
```

### Configure for iOS

Run `npx pod-install` after installing the npm package.

### Configure for Android

No additional set up necessary.

# API

```ts
import { getVideoInfoAsync } from 'expo-video-metadata';

/**
 * Gets metadata from a video file.
 * @param sourceFilename An URI of the video, local or remote.
 * @return Returns a promise that resolves to a `VideoInfoResult` object.
 */
const videoInfo = await getVideoInfoAsync(sourceFileName: string): Promise<VideoInfo>;

```

# Info

I am planning to add more metadata to the result object. If you need something specific, please open an issue or a PR.