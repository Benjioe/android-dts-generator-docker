# What is android-dts-generator-docker ?
Android-dts-generator-docker is a docker image to extract method signatures from jar files and create a TypeScript definition (.d.ts) file.
It's use [NativeScript android-dts-generator](https://github.com/NativeScript/android-dts-generator) version 2.

# Usage
## Linux (Ubuntu)
Create a directory with some Jar file inside. 
```Shell
mkdir ~/jarFolder
# !!!!!!!!!!! COPY SOME Jar FILES INSIDE !!!!!!! 
```

Launch the image and map this directory to /usr/src/jarFolder. 
```Shell
sudo docker run -v ~/jarFolder:/usr/src/jarFolder android-dts-generator-docker
```

The generate html is saved in ~/jarFolder/dts, open it in a browser. 
```Shell
cat ~/jarFolder/dts/android.d.ts
```

## Windows (Powershell)
Create a directory with some JavaScript file inside.
```Powershell
mkdir D:\jarFolder
# !!!!!!!!!!! COPY SOME Jar FILES INSIDE !!!!!!! 
 
```

Launch the image and map this directory to */usr/src/app*.
```Powershell
docker run -v D:\jarFolder:/usr/src/jarFolder android-dts-generator-docker
```

The generate html is saved in *D:\jsdoc\out*, open it in a browser.
```Powershell
notepad D:\jarFolder\dts\android.d.ts`
```
# Configure
You can replace the default android-dts-generator parameters with your own by putting them a the end of the docker command line: 
```Shell
sudo docker run -v ~/jarFolder:/usr/src/jarFolder android-dts-generator-docker YOUR_PARAMETERS`
```

All parameters are describe in the [android-dts-generator documentation](https://github.com/NativeScript/android-dts-generator).