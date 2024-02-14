# askui-jest-xray-environment
Jest environment for use with AskUIXRayStepReporter

## 🏗️ Configuration
Configure this `jest-environment` in `jest.config.ts` like this:

```typescript
import type { Config } from "@jest/types";

const config: Config.InitialOptions = {
  preset: "ts-jest",
  setupFilesAfterEnv: ["./helper/askui-helper.ts"], // former `./helper/jest.setup.ts`
  sandboxInjectedGlobals: ["Math"],
  testEnvironment: "@askui/jest-xray-environment",
};

// eslint-disable-next-line import/no-default-export
export default config;
```

## 🧱 Build New Release

```
cd askui-reporters

npm config set scope askui
npm config set access public

npm login

npm run release
```