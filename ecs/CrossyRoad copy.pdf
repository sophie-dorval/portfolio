int score;
int lives;
Bluecar bc;
Bluecar b2;
Chicken ch;
Greencar gc;
Greencar g2;
Redcar rc;
Redcar r2;

void setup() {
  size(800, 500);
  score = 0;
  lives = 3;
  ch = new Chicken(40, height/2);
  bc = new Bluecar(90, 15);
  rc = new Redcar(210, 100);
  gc = new Greencar(330, 300);
  b2 = new Bluecar(450, 250);
  g2 = new Greencar(570, 400);
  r2 = new Redcar(690, 160);
}

void draw() {
  background(0, 77, 0);
  drawBG();
  scoreBoard();
  bc.display();
  bc.move();
  gc.display();
  gc.move();
  rc.display();
  rc.move();
  r2.display();
  r2.move();
  g2.display();
  g2.move();
  b2.display();
  b2.move();
  ch.display();
  if (dist(ch.x, ch.y, bc.x, bc.y)<30) {
    lives = lives - 1; //hitting car
    ch.x = 40;
    ch.y = height/2;
    //score = score + 1 //coins
  }
    if (dist(ch.x, ch.y, rc.x, rc.y)<30) {
    lives = lives - 1; //hitting car
    ch.x = 40;
    ch.y = height/2;
  }
      if (dist(ch.x, ch.y, r2.x, r2.y)<30) {
    lives = lives - 1; //hitting car
    ch.x = 40;
    ch.y = height/2;
  }
      if (dist(ch.x, ch.y, gc.x, gc.y)<30) {
    lives = lives - 1; //hitting car
    ch.x = 40;
    ch.y = height/2;
  }
      if (dist(ch.x, ch.y, g2.x, g2.y)<30) {
    lives = lives - 1; //hitting car
    ch.x = 40;
    ch.y = height/2;
  }
      if (dist(ch.x, ch.y, b2.x, b2.y)<30) {
    lives = lives - 1; //hitting car
    ch.x = 40;
    ch.y = height/2;
  }
  if (lives < 1) {
    fill(0);
    rectMode(CORNER);
    rect(0, 0, width, height);
    fill(255);
    text("GAME OVER", 200, 400);
    noLoop();
  }
  if (ch.x > 790 ) {
    score = score + 100;
    ch.x = 40 ;
    ch.y = height/2;
  }
  //if (keyPressed) {
  //  if (key == 'w' || key == 'W') {
  //    ch.move('w');
  //  } else if (key == 's' || key == 'S') {
  //    ch.move('s');
  //  } else if (key == 'a' || key == 'A') {
  //    ch.move('a');
  //  } else if (key == 'd' || key == 'D') {
  //    ch.move('d');
  //  }
  //}
}

void drawBG() {
  fill(120);
  rect(60, 0, 60, height);
  rect(180, 0, 60, height);
  rect(300, 0, 60, height);
  rect(420, 0, 60, height);
  rect(540, 0, 60, height);
  rect(660, 0, 60, height);
}

void scoreBoard() {
  fill(127);
  rect(0, 0, width, 30);
  fill(0);
  text("Score:" + score + "Lives:" + lives, 10, 20);
}
void keyPressed() {
  if (key == CODED) {
    if (keyCode == UP) {
      ch.move('w');
    } else if (keyCode == DOWN) {
      ch.move('s');
    } else if (keyCode == LEFT) {
      ch.move('a');
    } else if (keyCode == RIGHT) {
      ch.move('d');
    }
  }
}
