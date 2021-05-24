# IP-Project - Smart LawnMower

## Report

[Link to the report](https://docs.google.com/document/d/1ekEJ68WdXmRyTiaCg41fwwrMgc1ySL53ycX0po5wwiU/edit)

## Getting started

Git clone this project to your machine.

### Prerequisites
- C++ compiler capable of building projects using C++ 17 or up.
- Pistache build 002 from 20210409 or up.
- Due to Pistache's current OS support a device running MacOS or Linux is required. We ran the code on an Linux VM hosted on Parallels Desktop.
- Curl for POST and GET requests.
 
Pistache can be easily installed using the following commands:
```
$ sudo add-apt-repository ppa:pistache+team/stable
$ sudo apt update
$ sudo apt install libpistache-dev
```
 
## Building
Build tested on Ubuntu 20.04.

- Go to the repository's location on your machine
- Run this command in terminal: 

  - g++ lawnmower.cpp -o lawnmower -lpistache -lcrypto -lssl -lpthread -std=c++17
  
- Run this command after: 

  - ./lawnmower

## App's functionalities

- Do the initial setup of the current yard:
  - lungime: defines the length of the yard. 
  - latime: defines the width of the yard.
  - matrice: defines the matrix representation of the yard:

    Example of yard matrix:
    ```    
    00000
    01120
    01100    where 0 = grass zone, 1 = house zone, 2 = charging station
    00000 
    00000
    ```

- Initialize the current battery level (0-100%).
- Build the road that the lawnmower will take to cut the grass.
- Read the informations defined above.
- Tell the lawnmower to go to the charging station. After this operation, the battery will be charged to 100%.
- Define the state of the device:
  - Start => Starts the mowing process (checks if the battery level is enough to do this operation)
  - Stop => Stops the process
  - Resume => Resumes the process

## Membrii echipei

- Buzoi Bianca-Nicoleta
- Gavril Bogdan Mircea
- Necula Florin-Alexandru
- Oanea Ana-Malina
- Samoilescu Camelia
