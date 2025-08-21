# to_do_app_subrat
Simple To Do app - Made by Subrat
package com.subrat.todoapp;

import android.os.Bundle;
import android.widget.ListView;
import androidx.appcompat.app.AppCompatActivity;
import java.util.ArrayList;

public class MainActivity extends AppCompatActivity {
    ListView listView;
    TaskAdapter adapter;
    ArrayList<String> tasks;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        listView = findViewById(R.id.listView);
        tasks = new ArrayList<>();
        adapter = new TaskAdapter(this, tasks);
        listView.setAdapter(adapter);

        tasks.add("Sample Task 1");
        tasks.add("Sample Task 2");
    }
}
