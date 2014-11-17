float x, y, vX, vY, gravity;
int sz = 50;
void setup() {
  size(700, 700);
  x = width/2;
  y = height*.05;
  vX = 5;        
  vY = 0;        
  gravity = .1;     
 
}

void draw() {
  background(0);
  fill(random(255),random(255),random(255));

  ellipse(x, y, sz, sz);      
  vY += gravity;           
  x += vX;                  
  y += vY;                 

  if (y + sz/2 > height) {   
    y = height - sz/2;
    vX *= .9;        
    vY *= -.7;        
  }
  if (x + sz/2 > width || x - sz/2 < 0) {
    vX *=-1;
  }
}

