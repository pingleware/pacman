# pacman
HTML5 version of pacman using p5js

![()](https://www.youtube.com/watch?v=AuoH0vz3Mqk)

# Pacman Sound Library
Thanks to https://www.classicgaming.cc/classics/pac-man/sounds

Sound effects added, but must press the ENTER/RETURN key to play the intro sound before pressing the arrow keys.
Only intro, chomp and death sounds added.

# Audio Looping
See https://stackoverflow.com/questions/3273552/html5-audio-looping

    var myAudio = new Audio('someSound.ogg'); 
    myAudio.addEventListener('ended', function() {
        this.currentTime = 0;
        this.play();
    }, false);
    myAudio.play();

or

    bgSound = new Audio("sounds/background.mp3");
    bgSound.loop = true;
    bgSound.play();

and

    myAudio = new Audio('someSound.ogg'); 
    if (typeof myAudio.loop == 'boolean')
    {
        myAudio.loop = true;
    }
    else
    {
        myAudio.addEventListener('ended', function() {
            this.currentTime = 0;
            this.play();
        }, false);
    }
    myAudio.play();

