# ApkBuilder V.1

Required :

Download All File On Library Folder

How To Use :

Put Code onCreate
ApkBuilder.init(this);

Example AAPT Usage :

```ApkBuilder.AAPT.setMinSdkVersion(minSdkVer);
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

Example ECJ Usage :

```ApkBuilder.ECJ.setSourceVersion("1.7);
ApkBuilder.ECJ.setTargetVersion("1.7");
ApkBuilder.ECJ.setClassesDir(path_classes_folder);
ApkBuilder.ECJ.addJarFile(path_dependencies_jar_file);
ApkBuilder.ECJ.addSourceDir(path_src_dir);
ApkBuilder.ECJ.compile();

Example D8 Usage :

```ApkBuilder.D8.setDebugMode(true);
ApkBuilder.D8.setClassPathFile("/storage/emulated/0/Classpath/rt.jar");
ApkBuilder.D8.setLibraryFile("/storage/emulated/0/Classpath/android.jar");
ApkBuilder.D8.setJava8Mode(false);
ApkBuilder.D8.setOutputDir(path_bin_folder);
ApkBuilder.D8.setInputDir(path_classes_folder);
ApkBuilder.D8.compile();

Example ApkMaker Usage :

```ApkBuilder.Maker.setDebugMode(true);
ApkBuilder.Maker.addFile(dex_file_path, dex_name);
ApkBuilder.Maker.setResourceApk(apk_res_file_path);
ApkBuilder.Maker.setOutputApk(apk_unsigned_path);
ApkBuilder.Maker.addSourceFolder(file_res_path);
ApkBuilder.Maker.addNativeLibraries(file_native_path);
ApkBuilder.Maker.create();

Example ApkSigner Usage :

```ApkBuilder.Signer.setAlias(alias);
ApkBuilder.Signer.setPassword(password);
ApkBuilder.Signer.setInputApk(apk_unsigned_path);
ApkBuilder.Signer.setOutputApk(apk_signed_path);
ApkBuilder.Signer.sign();


Changelog V.1 :
- added AAPT V1
- added ECJ
- added DX 1.16
- added R8 2.0.88
- added SDKLIB 26
- added APKSIGNER
