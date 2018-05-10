# miBandExample

Simple example of usage of miBand using the function connect, vibrate and stop vibrate.

For the correct develompemnt of the app I inserted, first of all, in the android manifest the commands for 
controlling the bluetooth: 

                 <uses-permission android:name="android.permission.BLUETOOTH" />
                 <uses-permission android:name="android.permission.BLUETOOTH_ADMIN" />

In the dependecies I also added an implementation for the miBand SDK:

                 implementation 'com.zhaoxiaodan.miband:miband-sdk:1.1.2'

lastly I inserted in the main.java the import for the library used to call the function of miBand

                 import com.zhaoxiaodan.miband.ActionCallback;
                 import com.zhaoxiaodan.miband.MiBand;
                 import com.zhaoxiaodan.miband.listeners.NotifyListener;
                 import com.zhaoxiaodan.miband.model.VibrationMode;

Example of a call of function associated with a button(e.g vibrate function)

                 vibrate.setOnClickListener(new View.OnClickListener() {
                 @Override
                 public void onClick(View v) {
                 miband.startVibration(VibrationMode.VIBRATION_WITH_LED);
                 }
                 });



