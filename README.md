# ko2k

#define trig1 2 
#define echo1 3 
#define trig2 6 
#define echo2 7 
#define trig3 4 
#define echo3 5 
#define buzzer 8 #define 
motor 9 
long duration1, distance1, duration2, distance2, duration3, distance3; 
void setup () 
{ 
pinMode (trig1, OUTPUT); 
pinMode (echo1, INPUT); pinMode 
(trig2, OUTPUT); pinMode (echo2, 
INPUT); pinMode (trig3, 
OUTPUT); pinMode (echo3, 
INPUT); pinMode (motor, 
OUTPUT);
pinMode (buzzer, OUTPUT); 
} 
void loop () 
{ 
//For sensor 1 digitalWrite 
(trig1, LOW); 
delayMicroseconds (2); 
digitalWrite (trig1, HIGH); 
delayMicroseconds (10); 
duration1 = pulseIn (echo1, HIGH); 
//For sensor 2 digitalWrite 
(trig2, LOW); 
delayMicroseconds (2); 
digitalWrite (trig2, HIGH); 
delayMicroseconds (10); 
duration2 = pulseIn (echo2, HIGH); 
//For sensor 3 digitalWrite 
(trig3, LOW); 
delayMicroseconds (2); 
digitalWrite (trig3, HIGH); 
delayMicroseconds (10); 
duration3 = pulseIn (echo3, HIGH); 
distance1 = (duration1*0.017); distance2 
= (duration2*0.017); distance3 = 
(duration3*0.017); 
if (distance1 < 20 && distance1 < distance2 && distance1 < distance3 ) 
{ 
digitalWrite (buzzer, HIGH); 
digitalWrite (motor, HIGH); 
delay (300); digitalWrite 
(buzzer, LOW); digitalWrite 
(motor, LOW); delay (300); 
} 
else if (distance2 < 20 && distance2 < distance1 && distance2 < distance3 ) 
{ 
digitalWrite (buzzer, HIGH); 
digitalWrite (motor, HIGH); 
delay (150); digitalWrite
(buzzer, LOW); digitalWrite 
(motor, LOW); delay (150); 
} 
else if (distance3 < 20 && distance3 < distance2 && distance3 < distance2 ) 
{ 
digitalWrite (buzzer, HIGH); 
digitalWrite (motor, HIGH); 
delay (50); digitalWrite 
(buzzer, LOW); digitalWrite 
(motor, LOW); delay (50); 
} 
digitalWrite (buzzer, LOW); 
digitalWrite (motor, LOW); 
} 
