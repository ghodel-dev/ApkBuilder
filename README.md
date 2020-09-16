# ApkBuilder V.1

## Required :

Download All Files On `Library Folder`

## How To Use :

Put Code `onCreate`
```groovy
ApkBuilder.init(this);
```

Example AAPT Usage :

```groovy
ApkBuilder.AAPT.setMinSdkVersion(minSdkVer);
ApkBuilder.AAPT.setMaxSdkVersion(targetSdkVersion);
ApkBuilder.AAPT.setVerCode(verCode);
ApkBuilder.AAPT.setVerName(verName);
ApkBuilder.AAPT.setPathAndroidJar(path_android_jar);
ApkBuilder.AAPT.setPathManifest(path_android_manifest);
ApkBuilder.AAPT.addDirResource(path_res_folder);
ApkBuilder.AAPT.setPathBinDir(path_bin_folder);
ApkBuilder.AAPT.setPathGenDir(path_gen_folder);
ApkBuilder.AAPT.setPathApkRes(path_apk_res_output);
ApkBuilder.AAPT.compile();
```

Example ECJ Usage :

```groovy
ApkBuilder.ECJ.setSourceVersion("1.7");
ApkBuilder.ECJ.setTargetVersion("1.7");
ApkBuilder.ECJ.setClassesDir(path_classes_folder);
ApkBuilder.ECJ.addJarFile(path_dependencies_jar_file);
ApkBuilder.ECJ.addSourceDir(path_src_dir);
ApkBuilder.ECJ.compile();
```

Example D8 Usage :

```groovy
ApkBuilder.D8.setDebugMode(true);
ApkBuilder.D8.setClassPathFile("/storage/emulated/0/Classpath/rt.jar");
ApkBuilder.D8.setLibraryFile("/storage/emulated/0/Classpath/android.jar");
ApkBuilder.D8.setJava8Mode(false);
ApkBuilder.D8.setOutputDir(path_bin_folder);
ApkBuilder.D8.setInputDir(path_classes_folder);
ApkBuilder.D8.compile();
```

Example ApkMaker Usage :

```groovy
ApkBuilder.Maker.setDebugMode(true);
ApkBuilder.Maker.addFile(dex_file_path, dex_name);
ApkBuilder.Maker.setResourceApk(apk_res_file_path);
ApkBuilder.Maker.setOutputApk(apk_unsigned_path);
ApkBuilder.Maker.addSourceFolder(file_res_path);
ApkBuilder.Maker.addNativeLibraries(file_native_path);
ApkBuilder.Maker.create();
```

Example ApkSigner Usage :

```groovy
ApkBuilder.Signer.setAlias(alias);
ApkBuilder.Signer.setPassword(password);
ApkBuilder.Signer.setInputApk(apk_unsigned_path);
ApkBuilder.Signer.setOutputApk(apk_signed_path);
ApkBuilder.Signer.sign();
```


## Changelog V.1 :
- _added AAPT V1_
- _added ECJ V.4.6.1_
- _added DX V.1.16_
- _added R8 V.2.0.88_
- _added SDKLIB V.26_
- _added APKSIGNER V.0.9_
