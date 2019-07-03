# Android Camera2 Barcode NDK Sample
The sample demonstrates how to optimize the [barcode reader demo](https://github.com/yushulx/android-camera2-barcode) by using C++ code. 

## Usage
1. Get a valid [trial license](https://www.dynamsoft.com/CustomerPortal/Portal/Triallicense.aspx) of Dynamsoft Barcode SDK.
2. Download [Dynamsoft Barcode Reader for Android](https://www.dynamsoft.com/Downloads/Dynamic-Barcode-Reader-Download.aspx?edition=android).
3. Extract `libDynamsoftBarcodeReaderAndroid.so` from `DynamsoftBarcodeReaderAndroid.aar` using `7-Zip`, and copy the shared library to `Application/src/main/cpp`.
4. Open the project in `Android Studio`.
5. Set the license in `Camera2BasicFragment.java`:

    ```java
    hBarcode = createBarcodeReader("LICENSE-KEY");
    ```

6. Build and run the app:

    ![Android Camera2 Barcode](https://www.codepool.biz/wp-content/uploads/2019/05/android-camera2-barcode.gif)




