<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">

    <Button
        android:id="@+id/btn_second"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Buka activity 2" />
    <Button
        android:id="@+id/btn_third"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Buka Activity 3"/>
    </LinearLayout>
    </RelativeLayout>

    package com.example.secondactivity;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

1.

package com.example.secondactivity;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {
    private Button secondButton, thirdButton;
    private String NAME ="nama"

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        secondButton = findViewById(R.id.btn_second);
        thirdButton = findViewById(R.id.btn_third);

        secondButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v){
                Intent createPackageContext;
                Intent intent = new Intent(createPackageContext: MainActivity.this, second_activity.class);
                intent.putExtra(NAME, value:"GIRABERLIAN");
                intent.putExtra(name:"email", value:"contact")
                startActivity(intent);
            }
        });
        thirdButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent createPackageContext;
                Intent intent = new Intent(createPackageContext: MainActivity.this, thirdactivity.class);
                startActivity(intent);
            }
        });
    }
}
2.
package com.example.secondactivity;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

public class second_activity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);
    }
}
3.
package com.example.secondactivity;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

public class thirdactivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_thirdactivity);
    }
}
