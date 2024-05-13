package com.example.myapplication4;

import static com.example.myapplication4.R.id.*;

import android.annotation.SuppressLint;
import android.content.Intent;
import android.graphics.Color;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.ImageView;
import android.widget.TextView;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {
    TextView tv1,tv2,tv3;


    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState); //부모 클래스를 먼처 호출 하고 실행.
        setContentView(R.layout.activity_main); //activity_main.xml파일을 액티비티 화면으로 쓰겠다.

        tv1 = (TextView) findViewById(R.id.view1);
        tv2 = (TextView) findViewById(R.id.view2);
        tv3 = (TextView) findViewById(R.id.view3);

    }
    @SuppressLint("NonConstantResourceId")
    public void onClick(View view){
        tv1.setVisibility(View.INVISIBLE);
        tv2.setVisibility(View.INVISIBLE);
        tv3.setVisibility(View.INVISIBLE);

        int id = view.getId();
        if (id == R.id.button1) {
            tv1.setVisibility(View.VISIBLE);
        } else if (id == R.id.button2) {
            tv2.setVisibility(View.VISIBLE);
        } else if (id == R.id.button3) {
            tv3.setVisibility(View.VISIBLE);
        }
    }


}
