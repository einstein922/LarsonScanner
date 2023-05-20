# LarsonScanner
# Code for Knight Rider's Larson Scanner
# C++ code
int led[]={2,3,4,5,6};
int sizeled=0;
int count=0;

void setup(){
  int i;
  for (i=0;i<sizeof(led);i+=1)
    pinMode(led[i], OUTPUT);
  sizeled=sizeof(led)-1;
}

void loop(){
  digitalWrite(led[0], HIGH);
  digitalWrite(led[1], HIGH);
  digitalWrite(led[2], HIGH);

  delay(1000);
  digitalWrite(led[0], LOW);
  digitalWrite(led[1], LOW);
  digitalWrite(led[2], LOW);

  delay(1000);
int i;
  for (i=0;i<3;i+=1){
    digitalWrite(led[i],HIGH);
    delay(600);
    digitalWrite(led[i],LOW);
    delay(100);
  }
}
