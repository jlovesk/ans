# ans
answers

PROGRAM:(JAVA CODING):

package com.example.changetextcolor;
import android.os.Bundle;
import android.app.Activity;
import android.graphics.Color;
import android.view.Menu;
import android.view.View;
import android.widget.*;
public class MainActivity extends Activity {
	float font =10;
	int i=1;
       @Override
        protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button b1=(Button) findViewById(R.id.button1);
        Button b2=(Button) findViewById(R.id.button2);
        final TextView t1=(TextView) findViewById(R.id.textView1);
        b1.setOnClickListener(new View.OnClickListener() {
		
		@Override
		public void onClick(View arg0) {
			// TODO Auto-generated method stub
			switch(i)
			{
			case 1:
			t1.setTextColor(Color.RED);
			break;
			case 2:
			t1.setTextColor(Color.parseColor("#00FF00"));
			break;
			case 3:
			t1.setTextColor(Color.parseColor("#FF0000"));
			break;
			case 4:
			t1.setTextColor(Color.parseColor("#800000"));
			break;
			}
			i++;
			if(i==5)
			i=1;
			}
			});
      b2.setOnClickListener(new View.OnClickListener() {
		
		@Override
		public void onClick(View v) {
			// TODO Auto-generated method stub
			t1.setTextSize(font);
			font=font+4;
			if(font==30)
			font=10;
			}
	});
	}
	@Override
	public boolean onCreateOptionsMenu(Menu menu) {
		// Inflate the menu; this adds items to the action bar if it is present.
		getMenuInflater().inflate(R.menu.main, menu);
		return true;	} 
 }

PROGRAM:(XML CODING):

<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context=".MainActivity" >
    <TextView
        android:id="@+id/textView1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/hello_world" />
    <Button
        android:id="@+id/button1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/textView1"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="78dp"
        android:text="change color" />
    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button1"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="84dp"
        android:text="change font" />
</RelativeLayout>

==========================================================================================================================
2222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222


<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:paddingBottom="@dimen/activity_vertical_margin"
 android:paddingLeft="@dimen/activity_horizontal_margin"
 android:paddingRight="@dimen/activity_horizontal_margin"
 android:paddingTop="@dimen/activity_vertical_margin"
 tools:context=".MainActivity" >
 <TextView
 android:id="@+id/textView1"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_alignParentTop="true"
 android:layout_centerHorizontal="true"
 android:layout_marginTop="42dp"
 android:textAppearance="?android:attr/textAppearanceMedium" />
 <TextView
 android:id="@+id/textView2"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_alignTop="@+id/textView1"
 android:layout_centerHorizontal="true"
 android:text="User Name"
 android:textAppearance="?android:attr/textAppearanceMedium" />
 <EditText
 android:id="@+id/editText1"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_below="@+id/textView1"
 android:layout_centerHorizontal="true"
 android:layout_marginTop="16dp"
 android:ems="10" >
 <requestFocus />
 </EditText>
 <TextView
 android:id="@+id/textView3"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_centerHorizontal="true"
 android:layout_centerVertical="true"
8
 android:text="Password"
 android:textAppearance="?android:attr/textAppearanceMedium" />
 <EditText
 android:id="@+id/editText2"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_below="@+id/textView3"
 android:layout_centerHorizontal="true"
 android:layout_marginTop="30dp"
 android:ems="10"
 android:inputType="textPassword" />
 <Button
 android:id="@+id/button1"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_alignRight="@+id/textView2"
 android:layout_below="@+id/editText2"
 android:layout_marginTop="51dp"
 android:text="Button" />
</RelativeLayout>
second.xml (For Successful Login)
<?xml version="1.0" encoding="utf-8"?>
<AbsoluteLayout xmlns:android="http://schemas.android.com/apk/res/android"
 android:layout_width="match_parent"
 android:layout_height="match_parent" >
 <TextView
 android:id="@+id/textView5"
 android:text="Successful"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_alignParentTop="true"
 android:layout_centerHorizontal="true"
 android:layout_marginTop="42dp"
 android:textAppearance="?android:attr/textAppearanceMedium" />
</AbsoluteLayout>
third.xml (For Login Failed)
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
9
 android:orientation="vertical" >
 <TextView
 android:id="@+id/textView6"
 android:text="Login Failed"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_alignParentTop="true"
 android:layout_centerHorizontal="true"
 android:layout_marginTop="42dp"
 android:textAppearance="?android:attr/textAppearanceMedium" />
</LinearLayout>
JAVA CODE
package com.example.signin;
import android.os.Bundle;
import android.app.Activity;
import android.view.Menu;
import android.view.View;
import android.view.View.OnClickListener;
import android.widget.Button;
import android.widget.EditText;
public class MainActivity extends Activity {
EditText A,B,G;
Button C;
String E,F;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
A= (EditText)findViewById(R.id.editText1);
B= (EditText)findViewById(R.id.editText2);
C= (Button)findViewById(R.id.button1);
C.setOnClickListener(new OnClickListener() {
@Override
public void onClick(View v) {
// TODO Auto-generated method stub
E=A.getText().toString();
F=B.getText().toString();
if(E.equals("Admin")&& F.equals("admin")){
setContentView(R.layout.second);
}
else {
10
setContentView(R.layout.third);
}
}
});
}
@Override
public boolean onCreateOptionsMenu(Menu menu) {
// Inflate the menu; this adds items to the action bar if it is present.
getMenuInflater().inflate(R.menu.main, menu);
return true;
}
}

=====================================================================================================================
333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333333


<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent" >
 <ImageView
 android:id="@+id/imageView1"
 android:layout_width="wrap_content"
 android:layout_height="match_parent"
 android:layout_alignParentLeft="true"
 android:layout_alignParentRight="true"
 android:layout_alignParentTop="true"
 android:src="@drawable/ic_launcher" />
</RelativeLayout>
JAVA CODE
package com.example.graphical_primitives;
import android.app.Activity;
import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.os.Bundle;
import android.view.Display;
import android.view.MotionEvent;
import android.view.View;
import android.view.View.OnTouchListener;
import android.widget.ImageView;
public class MainActivity extends Activity implements OnTouchListener {
 ImageView imageView;
 Bitmap bitmap;
 Canvas canvas;
 Paint paint;
 float downx = 0, downy = 0, upx = 0, upy = 0;
 @Override
 public void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 imageView = (ImageView) this.findViewById(R.id.imageView1);
 Display currentDisplay = getWindowManager().getDefaultDisplay();
 float dw = currentDisplay.getWidth();
 float dh = currentDisplay.getHeight();
 bitmap = Bitmap.createBitmap((int) dw, (int) dh,
14
 Bitmap.Config.ARGB_8888);
 canvas = new Canvas(bitmap);
 paint = new Paint();
 paint.setColor(Color.MAGENTA);
 imageView.setImageBitmap(bitmap);
 imageView.setOnTouchListener(this);
 }
 public boolean onTouch(View v, MotionEvent event) {
 int action = event.getAction();
 switch (action) {
 case MotionEvent.ACTION_DOWN:
 downx = event.getX();
 downy = event.getY();
 break;
 case MotionEvent.ACTION_MOVE:
 break;
 case MotionEvent.ACTION_UP:
 upx = event.getX();
 upy = event.getY();
 canvas.drawLine(downx, downy, upx, upy, paint);
 imageView.invalidate();
 break;
 case MotionEvent.ACTION_CANCEL:
 break;
 default:
 break;
 }
 return true;
 }
}


=================================================================================================================
44444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444


<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
17
 android:orientation="vertical"
 android:gravity="center_vertical" >
 <Button
 android:id="@+id/buttonSignIN"
 android:layout_width="fill_parent"
 android:layout_height="wrap_content"
 android:text="Sign In"
 android:onClick="signIn"/>
 <Button
 android:id="@+id/buttonSignUP"
 android:layout_width="fill_parent"
 android:layout_height="wrap_content"
 android:text="Sign Up" />
</LinearLayout>
JAVA CODE
package com.example.sqliteform;
import android.app.Activity;
import android.app.Dialog;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;
public class MainActivity extends Activity
{
Button btnSignIn,btnSignUp;
LoginDataBaseAdapter loginDataBaseAdapter;
@Override
protected void onCreate(Bundle savedInstanceState)
{
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 // create a instance of SQLite Database
 loginDataBaseAdapter=new LoginDataBaseAdapter(this);
 loginDataBaseAdapter=loginDataBaseAdapter.open();
 // Get The Refference Of Buttons
 btnSignIn=(Button)findViewById(R.id.buttonSignIN);
 btnSignUp=(Button)findViewById(R.id.buttonSignUP);
18
 // Set OnClick Listener on SignUp button
 btnSignUp.setOnClickListener(new View.OnClickListener() {
public void onClick(View v) {
// TODO Auto-generated method stub
/// Create Intent for SignUpActivity abd Start The Activity
Intent intentSignUP=new
Intent(getApplicationContext(),SignUPActivity.class);
startActivity(intentSignUP);
}
});
}
// Methos to handleClick Event of Sign In Button
public void signIn(View V)
 {
final Dialog dialog = new Dialog(MainActivity.this);
dialog.setContentView(R.layout.login);
 dialog.setTitle("Login");
 // get the Refferences of views
 final EditText
editTextUserName=(EditText)dialog.findViewById(R.id.editTextUserNameToLogin);
 final EditText
editTextPassword=(EditText)dialog.findViewById(R.id.editTextPasswordToLogin);
Button btnSignIn=(Button)dialog.findViewById(R.id.buttonSignIn);
// Set On ClickListener
btnSignIn.setOnClickListener(new View.OnClickListener() {
public void onClick(View v) {
// get The User name and Password
String userName=editTextUserName.getText().toString();
String password=editTextPassword.getText().toString();
// fetch the Password form database for respective user
name
String
storedPassword=loginDataBaseAdapter.getSinlgeEntry(userName);
// check if the Stored password matches with Password
entered by user
if(password.equals(storedPassword))
{
Toast.makeText(MainActivity.this, "Congrats:
Login Successfull", Toast.LENGTH_LONG).show();
19
dialog.dismiss();
}
else
{
Toast.makeText(MainActivity.this, "User Name or
Password does not match", Toast.LENGTH_LONG).show();
}
}
});
dialog.show();
}
@Override
protected void onDestroy() {
super.onDestroy();
 // Close The Database
loginDataBaseAdapter.close();
}
}


==============================================================================================
5555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555


activity_main.xml
Add the following code in an activity_main.xml file.
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/a
pk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
21
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context="example.javatpoint.com.androidnotification.MainActivity">
 <TextView
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="ANDROID NOTIFICATION"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintLeft_toLeftOf="parent"
 app:layout_constraintRight_toRightOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.091"
 android:textAppearance="@style/Base.TextAppearance.AppCompat.Medium"/>
 <Button
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:id="@+id/button"
 android:layout_marginBottom="112dp"
 android:layout_marginEnd="8dp"
 android:layout_marginStart="8dp"
 android:text="Notify"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintStart_toStartOf="parent" />
 </android.support.constraint.ConstraintLayout>
Create an activity named as activity_notification_view.xml and add the following code. This
activity will be launched on clicking the notification. TextView is used to display the notification
message.
activity_notification_view.xml
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/a
pk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context="example.javatpoint.com.androidnotification.NotificationView">
 <TextView
 android:id="@+id/textView2"
 android:layout_width="fill_parent"
 android:layout_height="wrap_content"
 android:gravity="center"
 android:text="your detail of notification..."
 android:textAppearance="@style/Base.TextAppearance.AppCompat.Medium" />
22
 <TextView
 android:id="@+id/textView"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_marginBottom="8dp"
 android:layout_marginEnd="8dp"
 android:layout_marginStart="8dp"
 android:layout_marginTop="8dp"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.096"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toBottomOf="@+id/textView2"
 app:layout_constraintVertical_bias="0.206"
 android:textAppearance="@style/Base.TextAppearance.AppCompat.Medium"/>
</android.support.constraint.ConstraintLayout>
JAVA CODE
package example.com.androidnotification;
import android.app.NotificationManager;
import android.app.PendingIntent;
import android.content.Context;
import android.content.Intent;
import android.support.v4.app.NotificationCompat;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
public class MainActivity extends AppCompatActivity {
 Button button;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 button = findViewById(R.id.button);
 button.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 addNotification();
 }
 });
 }
 private void addNotification() {
 NotificationCompat.Builder builder =
 new NotificationCompat.Builder(this)
 .setSmallIcon(R.drawable.messageicon) //set icon for notification
23
 .setContentTitle("Notifications Example") //set title of notification
 .setContentText("This is a notification message")//this is notification message
 .setAutoCancel(true) // makes auto cancel of notification
 .setPriority(NotificationCompat.PRIORITY_DEFAULT); //set priority of
notification
 Intent notificationIntent = new Intent(this, NotificationView.class);
 notificationIntent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
 //notification message will get at NotificationView
 notificationIntent.putExtra("message", "This is a notification message");
 PendingIntent pendingIntent = PendingIntent.getActivity(this, 0, notificationIntent,
 PendingIntent.FLAG_UPDATE_CURRENT);
 builder.setContentIntent(pendingIntent);

 // Add as notification
 NotificationManager manager = (NotificationManager)
getSystemService(Context.NOTIFICATION_SERVICE);
 manager.notify(0, builder.build());
 }
}
NotificationView.java
The NotificationView.java class receives the notification message and is displayed in TextView.
This class is invoked while taping the notification.
package example.com.androidnotification;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.TextView;
import android.widget.Toast;
public class NotificationView extends AppCompatActivity {
 TextView textView;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_notification_view);
 textView = findViewById(R.id.textView);
 //getting the notification message
 String message=getIntent().getStringExtra("message");
 textView.setText(message);
 }
} 


====================================================================================================
666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666666

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 android:layout_width="fill_parent"
 android:layout_height="fill_parent"
 >
 <RelativeLayout
 android:id="@+id/firstlayout"
 android:layout_width="fill_parent"
 android:layout_height="wrap_content"
 android:gravity="center"
26
 android:layout_marginTop="80dp">
 <TextView
 android:id="@+id/display"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="@string/hello_world"
 android:textSize="19sp" />
 </RelativeLayout>
 <RelativeLayout
 android:id="@+id/secondlayout"
 android:layout_width="fill_parent"
 android:layout_height="wrap_content"
 android:layout_below="@+id/firstlayout"
 android:gravity="center">
 <TextView
 android:id="@+id/timer"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:gravity="center_horizontal"
 android:text="@string/timer"
 android:layout_marginTop="80dp"
 android:textSize="36sp"/>
 </RelativeLayout>
 <RelativeLayout
 android:id="@+id/thirdlayout"
 android:layout_width="fill_parent"
 android:layout_height="wrap_content"
 android:layout_below="@+id/secondlayout"
 android:gravity="center">
 <Button
 android:id="@+id/clickme"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="@string/button"
 android:visibility="invisible"
 android:layout_marginTop="100dp"/>
 </RelativeLayout>
</RelativeLayout>
JAVA CODE
package com.example.multithread;
import android.app.Activity;
import android.os.Bundle;
import android.os.Handler;
import android.widget.Button;
import android.widget.TextView;
27
public class MainActivity extends Activity {
Handler hand = new Handler();
Button clickme;
TextView timer;
@Override
public void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
timer = (TextView) findViewById(R.id.timer);
clickme = (Button) findViewById(R.id.clickme);
hand.postDelayed(run, 1000);
}
Runnable run = new Runnable() {
@Override
public void run() {
updateTime();
}
};
public void updateTime() {
timer.setText("" + (Integer.parseInt(timer.getText().toString()) - 1));
if (Integer.parseInt(timer.getText().toString()) == 0) {
clickme.setVisibility(0);
} else {
hand.postDelayed(run, 1000);
}
}
}


===========================================================================================================
8888888888888888888888888888888888888888888888888888888888888888888888888888888888888888888888888888888888

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
34
 android:orientation="vertical"
 android:layout_width="fill_parent"
 android:layout_height="fill_parent"

>
 <Button
 android:layout_width="fill_parent"
 android:layout_height="wrap_content"
 android:text="Click To Upload File"
 android:id="@+id/uploadButton"
 />
 <TextView
 android:layout_width="fill_parent"
 android:layout_height="wrap_content"
 android:text=""
 android:id="@+id/messageText"
 android:textColor="#000000"
 android:textStyle="bold"
 />
</LinearLayout>
JAVA CODE
package com.androidexample.uploadtoserver;
import java.io.DataOutputStream;
import java.io.File;
import java.io.FileInputStream;
import java.net.HttpURLConnection;
import java.net.MalformedURLException;
import java.net.URL;
import android.app.Activity;
import android.app.ProgressDialog;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.view.View.OnClickListener;
import android.widget.Button;
import android.widget.TextView;
import android.widget.Toast;
public class UploadToServer extends Activity {
 TextView messageText;
 Button uploadButton;
 int serverResponseCode = 0;
 ProgressDialog dialog = null
;
 String upLoadServerUri = null
;

 /********** File Path *************/
 final String uploadFilePath = "/mnt/sdcard/";
35
 final String uploadFileName = "service_lifecycle.png";

 @Override
 public void onCreate(Bundle savedInstanceState) {

 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_upload_to_server);

 uploadButton = (Button)findViewById(R.id.uploadButton);
 messageText = (TextView)findViewById(R.id.messageText);

 messageText.setText("Uploading file path :- '/mnt/sdcard/"+uploadFileName+"'");

 /************* Php script path ****************/
 upLoadServerUri = "http://www.androidexample.com/media/UploadToServer.php";

 uploadButton.setOnClickListener(new OnClickListener() {
 @Override
 public void onClick(View v) {

 dialog = ProgressDialog.show(UploadToServer.this, "", "Uploading file...", true);

 new Thread(new Runnable() {
 public void run() {
 runOnUiThread(new Runnable() {
 public void run() {
 messageText.setText("uploading started.....");
 }
 });

 uploadFile(uploadFilePath + "" + uploadFileName);

 }
 }).start();
 }
 });
 }
 public int uploadFile(String sourceFileUri) {
 String fileName = sourceFileUri;
 HttpURLConnection conn = null;
 DataOutputStream dos = null;
 String lineEnd = "\r\n";
 String twoHyphens = "--";
 String boundary = "*****";
 int bytesRead, bytesAvailable, bufferSize;
 byte[] buffer;
36
 int maxBufferSize = 1 * 1024 * 1024;
 File sourceFile = new File(sourceFileUri);

 if (!sourceFile.isFile()) {

 dialog.dismiss();

 Log.e("uploadFile", "Source File not exist :"
 +uploadFilePath + "" + uploadFileName);

 runOnUiThread(new Runnable() {
 public void run() {
 messageText.setText("Source File not exist :"
 +uploadFilePath + "" + uploadFileName);
 }
 });

 return 0;

 }
 else
 {
 try {

 // open a URL connection to the Servlet
 FileInputStream fileInputStream = new FileInputStream(sourceFile);
 URL url = new URL(upLoadServerUri);

 // Open a HTTP connection to the URL
 conn = (HttpURLConnection) url.openConnection();
 conn.setDoInput(true); // Allow Inputs
 conn.setDoOutput(true); // Allow Outputs
 conn.setUseCaches(false); // Don't use a Cached Copy
 conn.setRequestMethod("POST");
 conn.setRequestProperty("Connection", "Keep-Alive");
 conn.setRequestProperty("ENCTYPE", "multipart/form-data");
 conn.setRequestProperty("Content-Type", "multipart/form-data;boundary=" +
boundary);
 conn.setRequestProperty("uploaded_file", fileName);

 dos = new DataOutputStream(conn.getOutputStream());

 dos.writeBytes(twoHyphens + boundary + lineEnd);
 dos.writeBytes("Content-Disposition: form-data;
name=\"uploaded_file\";filename=\""
 + fileName + "\"" + lineEnd);
37

 dos.writeBytes(lineEnd);

 // create a buffer of maximum size
 bytesAvailable = fileInputStream.available();

 bufferSize = Math.min(bytesAvailable, maxBufferSize);
 buffer = new byte[bufferSize];

 // read file and write it into form...
 bytesRead = fileInputStream.read(buffer, 0, bufferSize);
 while (bytesRead > 0) {
 dos.write(buffer, 0, bufferSize);
 bytesAvailable = fileInputStream.available();
 bufferSize = Math.min(bytesAvailable, maxBufferSize);
 bytesRead = fileInputStream.read(buffer, 0, bufferSize);

 }

 // send multipart form data necesssary after file data...
 dos.writeBytes(lineEnd);
 dos.writeBytes(twoHyphens + boundary + twoHyphens + lineEnd);

 // Responses from the server (code and message)
 serverResponseCode = conn.getResponseCode();
 String serverResponseMessage = conn.getResponseMessage();

 Log.i("uploadFile", "HTTP Response is : "
 + serverResponseMessage + ": " + serverResponseCode);

 if(serverResponseCode == 200){

 runOnUiThread(new Runnable() {
 public void run() {

 String msg = "File Upload Completed.\n\n See uploaded file here :
\n\n"
 +" http://www.androidexample.com/media/uploads/"
 +uploadFileName;

 messageText.setText(msg);
 Toast.makeText(UploadToServer.this, "File Upload Complete.",
 Toast.LENGTH_SHORT).show();
 }
 });
 }
38

 //close the streams //
 fileInputStream.close();
 dos.flush();
 dos.close();

 } catch (MalformedURLException ex) {

 dialog.dismiss();
 ex.printStackTrace();

 runOnUiThread(new Runnable() {
 public void run() {
 messageText.setText("MalformedURLException Exception : check
script url.");
 Toast.makeText(UploadToServer.this, "MalformedURLException",
Toast.LENGTH_SHORT).show();
 }
 });

 Log.e("Upload file to server", "error: " + ex.getMessage(), ex);
 } catch (Exception e) {

 dialog.dismiss();
 e.printStackTrace();

 runOnUiThread(new Runnable() {
 public void run() {
 messageText.setText("Got Exception : see logcat ");
 Toast.makeText(UploadToServer.this, "Got Exception : see logcat ",
 Toast.LENGTH_SHORT).show();
 }
 });
 Log.e("Upload file to server Exception", "Exception : "
 + e.getMessage(), e);
 }
 dialog.dismiss();
 return serverResponseCode;

 } // End else block
 }
}

=============================================================================================
99999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999

<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".BroadcastPhoneStates" >
 <TextView
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_centerHorizontal="true"
 android:layout_centerVertical="true"
 android:text="When new SMS will come it will show a alert message." />
</RelativeLayout>
JAVA CODE
BroadcstNewSms.java
package com.androidexample.broadcastreceiver;
import android.os.Bundle;
import android.app.Activity;
public class BroadcastNewSms extends Activity {
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.androidexample_broadcast_newsms);
}
}
IncomingSms.java
package com.androidexample.broadcastreceiver;
import android.content.BroadcastReceiver;
import android.content.Context;
import android.content.Intent;
import android.os.Bundle;
import android.telephony.SmsManager;
import android.telephony.SmsMessage;
import android.util.Log;
import android.widget.Toast;
public class IncomingSms extends BroadcastReceiver {
// Get the object of SmsManager
final SmsManager sms = SmsManager.getDefault();
public void onReceive(Context context, Intent intent) {
// Retrieves a map of extended data from the intent.
final Bundle bundle = intent.getExtras();
try {
if (bundle != null) {
42
final Object[] pdusObj = (Object[]) bundle.get("pdus");
for (int i = 0; i < pdusObj.length; i++) {
SmsMessage currentMessage =
SmsMessage.createFromPdu((byte[]) pdusObj[i]);
String phoneNumber =
currentMessage.getDisplayOriginatingAddress();
 String senderNum = phoneNumber;
 String message = currentMessage.getDisplayMessageBody();
 Log.i("SmsReceiver", "senderNum: "+ senderNum + "; message: " +
message);

 int duration = Toast.LENGTH_LONG;
Toast toast = Toast.makeText(context, "senderNum: "+
senderNum + ", message: " + message, duration);
toast.show();
} // end for loop
 } // bundle is null
} catch (Exception e) {
Log.e("SmsReceiver", "Exception smsReceiver" +e);
}
}


=============================================================================================
1111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:paddingLeft="20dp"
 android:paddingRight="20dp"
 android:orientation="vertical" >
 <EditText
 android:id="@+id/txtTo"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:hint="To"/>
 <EditText
 android:id="@+id/txtSub"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:hint="Subject"/>
 <EditText
 android:id="@+id/txtMsg"
 android:layout_width="match_parent"
 android:layout_height="0dp"
 android:layout_weight="1"
 android:gravity="top"
 android:hint="Message"/>
 <Button
 android:layout_width="100dp"
 android:layout_height="wrap_content"
 android:layout_gravity="right"
 android:text="Send"
 android:id="@+id/btnSend"/>
</LinearLayout>
JAVA CODE
package com.tutlane.sendmailexample;
import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
public class MainActivity extends AppCompatActivity {
 private EditText eTo;
 private EditText eSubject;
 private EditText eMsg;
 private Button btn;
 @Override
51
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 eTo = (EditText)findViewById(R.id.txtTo);
 eSubject = (EditText)findViewById(R.id.txtSub);
 eMsg = (EditText)findViewById(R.id.txtMsg);
 btn = (Button)findViewById(R.id.btnSend);
 btn.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 Intent it = new Intent(Intent.ACTION_SEND);
 it.putExtra(Intent.EXTRA_EMAIL, new String[]{eTo.getText().toString()});
 it.putExtra(Intent.EXTRA_SUBJECT,eSubject.getText().toString());
 it.putExtra(Intent.EXTRA_TEXT,eMsg.getText());
 it.setType("message/rfc822");
 startActivity(Intent.createChooser(it,"Choose Mail App"));
 }
 });
 }
}


====================================================================================================
1122222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222


<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
53
 android:orientation="vertical"
 android:layout_width="fill_parent"
 android:layout_height="fill_parent"
 >
<Gallery
android:id="@+id/Gallery01"
android:layout_width="fill_parent"
android:layout_height="wrap_content"></Gallery>
<ImageView
android:id="@+id/ImageView01"
android:layout_width="wrap_content"
android:layout_height="wrap_content"></ImageView>
</LinearLayout>
JAVA CODE
package com.sai.samples.views;
import android.app.Activity;
import android.content.Context;
import android.content.res.TypedArray;
import android.os.Bundle;
import android.view.View;
import android.view.ViewGroup;
import android.widget.AdapterView;
import android.widget.BaseAdapter;
import android.widget.Gallery;
import android.widget.ImageView;
import android.widget.Toast;
import android.widget.AdapterView.OnItemClickListener;
public class GalleryView extends Activity {
 Integer[] pics = {
 R.drawable.antartica1,
 R.drawable.antartica2,
 R.drawable.antartica3,
 R.drawable.antartica4,
 R.drawable.antartica5,
 R.drawable.antartica6,
 R.drawable.antartica7,
 R.drawable.antartica8,
 R.drawable.antartica9,
 R.drawable.antartica10
 };
 ImageView imageView;
/** Called when the activity is first created. */
54
 @Override
 public void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.main);

 Gallery ga = (Gallery)findViewById(R.id.Gallery01);
 ga.setAdapter(new ImageAdapter(this));

 imageView = (ImageView)findViewById(R.id.ImageView01);
 ga.setOnItemClickListener(new OnItemClickListener() {
@Override
public void onItemClick(AdapterView<?> arg0, View arg1, int arg2,
long arg3) {
Toast.makeText(getBaseContext(),
"You have selected picture " + (arg2+1) + " of
Antartica",
Toast.LENGTH_SHORT).show();
imageView.setImageResource(pics[arg2]);
}

 });

 }


 public class ImageAdapter extends BaseAdapter {
 private Context ctx;
 int imageBackground;

 public ImageAdapter(Context c) {
ctx = c;
TypedArray ta = obtainStyledAttributes(R.styleable.Gallery1);
imageBackground =
ta.getResourceId(R.styleable.Gallery1_android_galleryItemBackground, 1);
ta.recycle();
}
@Override
 public int getCount() {

 return pics.length;
 }
55
 @Override
 public Object getItem(int arg0) {

 return arg0;
 }
 @Override
 public long getItemId(int arg0) {

 return arg0;
 }
 @Override
 public View getView(int arg0, View arg1, ViewGroup arg2) {
 ImageView iv = new ImageView(ctx);
 iv.setImageResource(pics[arg0]);
 iv.setScaleType(ImageView.ScaleType.FIT_XY);
 iv.setLayoutParams(new Gallery.LayoutParams(150,120));
 iv.setBackgroundResource(imageBackground);
 return iv;
 }
 }
}






