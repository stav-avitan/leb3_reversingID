# leb3_reversingID

## First try
I ran the command "strings ./prog".
I did not find an optional password after going through the entire list received.

### Terminal

![srtings](https://user-images.githubusercontent.com/120071641/236434201-b7d5edcc-272c-424d-9572-79d4d53cd6e9.png)


## Second try 
I ran the command "strace ./prog".
From here I understood that it is not possible to use debuggers.

### Terminal

![ltrace](https://user-images.githubusercontent.com/120071641/236436029-fcae43bb-8ac6-4877-b840-c764f7cfa5b9.png)

## Third try
I ran the command "objdump -d ./prog".
I noticed that there is an array of size 6.
After continuing to review the resulting output I noticed the "not" command.
I did a "not" on the array characters and got an ASCII code.
The translation of the ASCII code was ORACLE.
This was the password.


### Terminal

![objdumpF](https://user-images.githubusercontent.com/120071641/236437497-0700df92-2c0d-4da0-982f-5065ab69f949.png)
![Array](https://user-images.githubusercontent.com/120071641/236437629-522e1f26-2401-404a-bb85-cccc911054a8.png)
![not](https://user-images.githubusercontent.com/120071641/236438891-c67ff48e-0bd7-4039-9db9-783ac81862c4.png)
![The_password](https://user-images.githubusercontent.com/120071641/236439406-dadb9769-e408-452a-a6be-79b53cffa596.png)
