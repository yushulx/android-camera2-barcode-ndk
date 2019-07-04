# Android Camera2 Barcode NDK Sample
The sample demonstrates how to optimize the [barcode reader demo](https://github.com/yushulx/android-camera2-barcode) by using C++ code. 

## Usage
1. Get a valid [trial license](https://www.dynamsoft.com/CustomerPortal/Portal/Triallicense.aspx) of Dynamsoft Barcode SDK.
2. Download [Dynamsoft Barcode Reader for Android](https://www.dynamsoft.com/Downloads/Dynamic-Barcode-Reader-Download.aspx?edition=android).
3. Extract files from `DynamsoftBarcodeReaderAndroid.aar` using `7-Zip`, and copy a shared library `DynamsoftBarcodeReaderAndroid.aar\jni\<ARCH>\libDynamsoftBarcodeReaderAndroid.so` to `Application/src/main/cpp`.

    ![Dynamsoft Barcode Reader shared libraries](https://www.codepool.biz/wp-content/uploads/2019/07/dynamsoft-barcode-armeabi.png)
    
    In this project, `armeabi-v7a` is used. If you use other `ABIs`, don't forget to update the corresponding info in `build.gradle`.
    
    ```
    defaultConfig {
        minSdkVersion 21
        targetSdkVersion 27
        ndk {
            abiFilters 'armeabi-v7a'
        }
        externalNativeBuild {
            cmake {
                arguments '-DANDROID_STL=c++_static', '-DANDROID_ABI=armeabi-v7a'
            }
        }
    }
    ```
    
4. Open the project in `Android Studio`.
5. Set the license in `Camera2BasicFragment.java`:

    ```java
    hBarcode = createBarcodeReader("LICENSE-KEY");
    ```

6. Build and run the app:

    ![Android Camera2 Barcode](https://www.codepool.biz/wp-content/uploads/2019/05/android-camera2-barcode.gif)

## Blog
[Using Android NDK to Optimize Barcode Reading Performance](https://www.codepool.biz/android-ndk-optimize-camera2-barcode.html)




