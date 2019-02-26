# [vikingfacer.github.io](https://vikingfacer.github.io)


[bs-repo]:https://github.com/vikingfacer/C-BattleShip
[rusty-repo]:https://github.com/vikingfacer/rusty_bot
[julia-repo]:https://github.com/vikingfacer/JuliaSerial


## Current Projects

* Raylib Games 
	* [Battleship][bs-repo] - the child's game about war. In this project the raylib game library is used to create the game of Battleship. The goal of this project is to build a retro style arcade game modeled after Battleship. Cheesy sound bits, Central Asia National Anthem background music, simple graphics and splash screens. This game is not yet complete but is close to an alpha. 


* Rust Robotics 
	* [Alexa Jones][rusty-repo] - a robot themed with conspiracy theory. Alexa Jones is a robotics project that started out named rustybot. This is because The main language chosen for the project was/is Rust. The robot design to targeted at cheap and easy, Raspberry Pi (Main board) and an Arduino (peripheral board). This project has expained during development to include a controller, peripheral controls, and board to board communication system. 


## Past Projects
* [Julia Serial Device][julia-repo]
	* JuliaSerial - is a small wrapper that allows a user to connect with a serial device in the Julia programming language. This is done using a shared C library and Julia's foreign function interface. The motive for this project was necessity at the time there was no standard way to connect to a serial device in Julia so I wrote a basic wrapper for a POSIX serial device. 


# [Battleship][bs-repo]
### Basic BattleShip game build with raylib 

## Screen Shots

![Game Intro](Battleship/screenshot5.png)

![Game Splash Screen](Battleship/screenshot4.png)

![Unfilled Ship Graveyard](Battleship/screenshot0.png)

![Illegal Move](Battleship/screenshot2.png)

![Filled Ship Graveyard](Battleship/screenshot1.png)

![Shooting](Battleship/screenshot3.png)


# [Rust Robotics][rusty-repo]

* Writings on the Project - The writings for this project are intended to be fun and informational. This is so people with no techinical experience can enjoy them. Even if its just for the jokes and bad analogies.  

[Alexa Jones - Making a Robot](https://medium.com/@jacobmontpetit/alexa-jones-45b2187083fa)

[Alexa Jones — Why Two Boards?](https://medium.com/@jacobmontpetit/alexa-jones-why-two-boards-4b9e28f1b3de)

[![In Action](http://img.youtube.com/vi/BS0gs7bHyYM/0.jpg)](http://www.youtube.com/watch?v=BS0gs7bHyYM "Alexa Jones In Action")


# [Julia Serial][julia-repo]

* This is a basic library that opens closes reads, writes. It can sets the mincount, and the speed.

Once the device is open it can read or write
```julia 
port = serial.open_port("/dev/ttyUSB0")
serial.set_attrs(port, 1152000)

function test()
    for i=1:10
    	@show serial.swrite(port, "Hello\n")
    	sleep(.5)
    	@show serial.sread(port)
    end
    serial.close_port(port)
end 

test()
```

