==========android manifest.xml=============


<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:background="#673AB7"
    android:padding="20dp">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="MY APP"
        android:textSize="36sp"
        android:textStyle="bold"
        android:textColor="#FFFFFF" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Welcome to our App"
        android:textSize="18sp"
        android:textColor="#FFFFFF"
        android:layout_marginTop="10dp" />

    <Button
        android:id="@+id/btn"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="LOGIN NOW"
        android:layout_marginTop="30dp" />

</LinearLayout>




============main activity.xml==========

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:background="#673AB7"
    android:padding="20dp">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="MY APP"
        android:textSize="36sp"
        android:textStyle="bold"
        android:textColor="#FFFFFF" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Welcome to our App"
        android:textSize="18sp"
        android:textColor="#FFFFFF"
        android:layout_marginTop="10dp" />

    <Button
        android:id="@+id/btn"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="LOGIN NOW"
        android:layout_marginTop="30dp" />

</LinearLayout>





=========mainactivity.java===============





package com.example.splash;

import android.os.Bundle;
import android.content.Intent;
import android.widget.Button;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle b) {
        super.onCreate(b);
        setContentView(R.layout.activity_main);

        Button btn = findViewById(R.id.btn);

        btn.setOnClickListener(v -> {
            Intent i = new Intent(
                    MainActivity.this, LoginActivity.class);
            startActivity(i);
        });
    }
}





===========login_activity.java=======



package com.example.splash;

import android.os.Bundle;
import android.widget.Button;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;

public class LoginActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle b) {
        super.onCreate(b);
        setContentView(R.layout.activity_login);

        Button btn = findViewById(R.id.login);

        btn.setOnClickListener(v -> {
            Toast.makeText(this,
                    "Welcome!",
                    Toast.LENGTH_SHORT).show();
        });
    }
}

=========activity_login.xml============


<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="25dp"
    android:background="#EDE7F6">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="LOGIN"
        android:textSize="32sp"
        android:textStyle="bold"
        android:textColor="#673AB7"
        android:layout_marginBottom="25dp" />

    <EditText
        android:id="@+id/user"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter your name"
        android:inputType="textPersonName" />

    <EditText
        android:id="@+id/pass"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter your password"
        android:inputType="textPassword" />

    <Button
        android:id="@+id/login"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="LOGIN"
        android:layout_marginTop="20dp" />

</LinearLayout># splashscreen-task
