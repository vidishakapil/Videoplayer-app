# Videoplayer-app
package com.example.harrytube;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.MediaController;
import android.widget.VideoView;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        VideoView nature=findViewById(R.id.nature);
        nature.setVideoPath("android.resource://"  +  getPackageName() + "/" +R.raw.clip);
        MediaController mediaController=new MediaController(this);
        nature.setMediaController(mediaController);
        mediaController.setAnchorView(nature);
        nature.start();
    }
}
