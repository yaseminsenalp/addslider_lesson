# addslider_lesson
import controlP5.*;

float x;
float y;
int sr = 20;
int sg = 40;
int sb = 60;
int sa = 80;
int fr = 100;
int fg = 120;
int fb = 140;
int fa = 160;
int rw =180;
int rh = 200;

ControlP5 cp5;
ColorPicker cp;



void setup() {
  size(600,600);
  
  cp5 = new ControlP5(this);
  
  //x pos slider
  cp5.addSlider("x")
  .setPosition(10,10)
  .setRange(0,width)
  .setSize(200, 20);
  
  //y pos slider
  cp5.addSlider("y")
  .setPosition(10,30)
  .setRange(0,height)
  .setSize(200, 20);
  
  //color slider
  cp = cp5.addColorPicker("picker")
  .setPosition(300,10)
  .setColorValue(color(0,0,0,255));
  
  //width slider
   cp5.addSlider("rw")
  .setPosition(10,50)
  .setRange(0,width)
  .setSize(200, 20);
  
  //height slider
  cp5.addSlider("rh")
  .setPosition(10,70)
  .setRange(0,height)
  .setSize(200, 20);
  
}

void draw () {
  
  //x = width*0.5;
  //y = height*0.5;
  
  background(255);
  stroke(sr,sg,sb,sa);
  rectMode(CENTER);
  fill(cp.getColorValue());
  rect(x,y,rw,rh);
}
  
