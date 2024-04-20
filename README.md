package com.example.fodasse

import android.annotation.SuppressLint
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.Image
import androidx.compose.foundation.layout.Column
import androidx.compose.foundation.layout.ColumnScope
import androidx.compose.foundation.layout.Row
import androidx.compose.material3.ExperimentalMaterial3Api
import androidx.compose.material3.Scaffold
import androidx.compose.material3.Text
import androidx.compose.material3.TopAppBar
import androidx.compose.runtime.Composable
import androidx.compose.ui.res.painterResource
import androidx.compose.ui.tooling.preview.Preview
import androidx.compose.ui.unit.Dp
import androidx.compose.ui.unit.dp
import com.example.fodasse.ui.theme.FodasseTheme

class MainActivity : ComponentActivity() {
    @OptIn(ExperimentalMaterial3Api::class)
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            FodasseTheme {
                // A surface container using the 'background' color from the theme
                Home()
            }
        }
    }
    @SuppressLint("UnusedMaterial3ScaffoldPaddingParameter")
    @OptIn(ExperimentalMaterial3Api::class)
    @Composable
    @Preview
    fun Home() {
        Scaffold(
            topBar = {
                TopAppBar(title = {
                    Text("Teste")
                })
            }
        ){
        Row {
                Column {
                    Image(painterResource(R.drawable.ic_launcher_background),"Folha")
                    Text("Fodasse essa merda")

                }
                Column (verticalArrangement = 16.dp){
                    Text("Tesntando")
                }
            }
        }

        }

    private fun Column(verticalArrangement: Dp, content: ColumnScope.() -> Unit) {
        TODO("Not yet implemented")
    }
}

