# Circuit-for-connecting-and-disconnecting-the-electric-current-for-the-motors
# Code 
#include <Servo.h>

Servo servol;
Servo servo2;

int f=0;

void setup()
{
 servol.attach(3);
 servo2.attach (4) ;
 pinMode (9, INPUT) ; 
}

void loop()
{
  if (digitalRead (9) == 1) 
  {
    for (f=0; f <= 180; f += 1)
    {
      servol.write (f);
      servo2.write (f);
    }
  }
  
  else
  {
    servol.write(0);
    servo2.write (0) ;
  }
  
}
