# MyJS

Power Apps キャンバスアプリに JavaScript コードを埋め込むためのコードコンポーネント

---

## Original

- [scottdurow/Canvas-App-Samples](https://github.com/scottdurow/Canvas-App-Samples)
  - [pcfjs](https://github.com/scottdurow/Canvas-App-Samples/tree/master/PCF/pcfjs)

## build

```powershell
npm install
npm install --save-dev typescript@4
npm upgrade

npm run build
npm start watch
```

## Packaging

developer command promptで実行

```powershell
mkdir MyJSSolution
cd .\MyJSSolution\
pac solution init --publisher-name YA --publisher-prefix ya
pac solution add-reference --path ..\
```

マネージドソリューションとして作成する場合は以下のコメントを解除

```xml
  <!-- Solution Packager overrides, un-comment to use: SolutionPackagerType (Managed, Unmanaged, Both) -->
  <PropertyGroup>
    <SolutionPackageType>Managed</SolutionPackageType>
  </PropertyGroup>
  <!-- -->
```

powershell```
# デバッグ構成で作成する場合
msbuild /t:build /restore

# マネージドソリューションとしてリリース構成で作成する場合
msbuild /t:build /restore /p:configuration=Release
```

---

Copyright (c) 2023 YA-androidapp(https://github.com/yzkn) All rights reserved.
