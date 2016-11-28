
SilkySignature
========

A smooth and silky signature pad for android.

![app screenshot](signature.png)

Download
--------

Download SilkySignature or grab via Gradle:

```groovy
compile 'com.williamww:silky-signature:0.0.2'
```

Example
--------

Add this to layout file
```xml

<com.williamww.silkysignature.views.SignaturePad
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
android:id="@+id/signature_pad"
android:layout_width="match_parent"
android:layout_height="match_parent"
app:penColor="@android:color/black"
/>
```

Control in code
```java

mSignaturePad = (SignaturePad) findViewById(R.id.signature_pad);
mSignaturePad.setOnSignedListener(new SignaturePad.OnSignedListener() {
@Override
public void onSigned() {
//Event triggered when the pad is signed
}

@Override
public void onClear() {
//Event triggered when the pad is cleared
}
});
```
To get signature image
* `getSignatureBitmap()` - A signature bitmap with a white background.
* `getTransparentSignatureBitmap()` - A signature bitmap with a transparent background.
* `getSignatureSvg()` - A signature Scalable Vector Graphics document.

SilkySignature requires at minimum Java 7 or Android 4.0.
