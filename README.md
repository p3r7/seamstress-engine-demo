# seamstress-engine-demo

NB: adjust path according to you own setup. below assumes standard supercollider install on mac os.


## setup

### add norns' engine abstraction to supercollider

    cd ~/Documents/code/monome/
    git clone https://github.com/monome/norns
    ln -s ~/Documents/code/monome/norns/sc/core ~/Library/Application\ Support/SuperCollider/Extensions/monome-norns-core


### register seamstress folder as an engine repo

    ln -s ~/seamstress ~/Library/Application\ Support/SuperCollider/Extensions/seamstress


### clone this repo under seamstress home

    cd ~/seamstress/
    git clone https://github.com/p3r7/seamstress-engine-demo


## usage

start supercollider IDE. you should hear the familiar norns bootup sound.

installing jackd is not required.

then:

    cd ~/seamstress/seamstress-engine-demo/
    seamstress -l 8888 -s engine-demo.lua

This should do a lookup of available engines by asking the supercollider server and load the `Sines` engine provided in the `lib/` folder of this repo.

This works as we change seamstress OSC listen port to 8888 (same as norns for sc interop).

To hear some sound, in the seamstress REPL:

    init_engine_params()
