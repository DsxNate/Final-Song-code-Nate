# Final-Song-code-Nate

# Welcome to Sonic Pi

#nate and todds song

use_synth :piano
use_bpm 151
#start highest in the room

boom = "c:/users/naythan_ignacio/documents/audacity/[4k edit] bo bo bo boom lebron lebronjames edit nba.wav"




define :notes do | note1,note2,note3,note4|
  play note1, sustain: 2
  sleep 1
  play note2, sustain: 2
  sleep 1
  play note3, sustain: 2
  sleep 1
  play note4, sustain: 2
  sleep 1
end

define :drum do
  sample :drum_cymbal_closed
  sleep 0.5
end
#comes from measure 12-15 piano
define :piano do
  play :r
  sleep  0.5
  play :d3
  sleep  0.5
  play :d3
  sleep  0.5
  play :d3
  sleep  0.5
  play :d3
  sleep  0.5
  play :d3
  sleep  0.5
  play :e3
  sleep  0.5
  play :c3
  sleep  0.5
end
define :piano2 do
  play :d3
  sleep  1
  play :c3, sustain: 1
  sleep 3
  
end
define :piano3 do
  play :r
  sleep  0.5
  play :r
  sleep  0.5
  play :d3
  sleep  0.5
  play :d3
  sleep  0.5
  play :d3
  sleep  0.5
  play :d3
  sleep  0.5
  play :e3
  sleep  0.5
  play :c3
  sleep  0.5
end
define :piano4 do
  play :d3
  sleep 0.5
  play :r
  sleep 0.5
  sleep 2
end
#from measure 18
define :piano5 do
  play :r
  sleep 0.5
  play :a4
  sleep 0.5
  play :a4
  sleep 0.5
  play :a4
  sleep 0.5
  play :c4
  sleep 0.5
  play :a4
  sleep 0.5
  play :g3
  sleep 0.5
  play :f3
  sleep 0.5
end


#guitar music
define :guitar2 do
  use_synth :fm
  play :e5, sustain: 0.5
  sleep 1
  play :c5, sustain: 0.5
  sleep 1
  play :a4, sustain: 0.5
  sleep 1
  play :e5, sustain: 0.5
  sleep 1
  play :c5, sustain: 0.5
  sleep 1
  play :c3, sustain: 0.5
  sleep 1
  play :e5, sustain: 0.5
  sleep 1
  play :c5, sustain: 0.5
  sleep 1
end


#guitar music with double line
define :guitar do
  use_synth :fm
  sleep 2
  play :f5
  sleep 0.5
  play :d5
  sleep 0.5
  play :c5
  sleep 0.5
  play :f5
  sleep 0.5
  play :d5
  sleep 0.5
  play :c5
  sleep 0.5
  play :f5
  sleep 0.5
  play :e5
  sleep 0.25
  play :f5
  sleep 0.25
end

define :bottom do
  #measure 1-6
  #with_fx :hpf do
  play :f3, sustain: 2
  sleep 1
  play :d3, sustain: 2
  sleep 1
  play :a2, sustain: 2
  sleep 1
  play :f3, sustain: 2
  sleep 1
  play :e3, sustain: 2
  sleep 1
  play :c3, sustain: 2
  sleep 1
  play :a2, sustain: 2
  sleep 1
  play :e3, sustain: 2
  sleep 1
end

#start

#sample that plays before the loop should be here 
live_loop:begin do
  #m 1 and 2
  play :d5, sustain: 2
  sleep 1.5
  play :f5, sustain: 2
  sleep 1.5
  play :g5, sustain: 2
  sleep 1.5
  play :e5, sustain: 4
  sleep 3
  play :r
  sleep 0.5
  
  #m 3 and 4
  play :d5, sustain: 2
  sleep 1.5
  play :c5, sustain: 2
  sleep 1.5
  #d5 goes from measure 3 to 4 with the half circle
  play :d5, sustain: 2
  sleep 1.5
  play :b4, sustain: 2
  sleep 3
  play :r
  sleep 0.5
  
  #m 5 and 6
  play :d5, sustain: 2
  sleep 1.5
  play :f5, sustain: 2
  sleep 1.5
  play :g5, sustain: 2
  sleep 1.5
  play :e5, sustain: 2
  sleep 3
  play :r, sustain: 2
  sleep 0.5
  
  
  #m 7 and 8 ( top #1)
  play :d5, sustain: 2
  sleep 1.5
  play :c5, sustain: 2
  sleep 1.5
  play :d5, sustain: 2
  sleep 1.5
  play :b4, sustain: 2
  sleep 3
  play :r, sustain: 2
  sleep 0.5
  
  play :d5, sustain: 2
  sleep 1.5
  play :c5, sustain: 2
  sleep 1.5
  play :d5, sustain: 2
  sleep 1.5
  play :b4, sustain: 2
  sleep 2.5
  play :r, sustain: 2
  sleep 1
  stop
end


#measure 1-6 bottom
#with_fx :hpf do

#paramaterized function

#measure 7 (bottom piano #2)
notes :f3, :d3, :a3, :f3

#measure 8 (bottom piano #2)
notes :e3, :c3, :a3, :e3

#measure 9-10 (top piano #2)

play :d5
sleep 1.5
play :f5
sleep 1.5
play :g5
sleep 1.5
play :e5
sleep 3
play :r
sleep 0.5


#measure 9-10 (bottom piano #2)

#bassclef
play :f3, sustain: 1
sleep 1
play :d3, sustain: 2
sleep 1
play :a2, sustain: 2
sleep 1
play :f3, sustain: 2
sleep 1
play :e3, sustain: 2
sleep 1
play :c3, sustain: 2
sleep 1
play :a2, sustain: 2
sleep 1
play :e3, sustain: 2

sample boom


#guitar measure 9-11
use_synth :fm

guitar

#e5, c5, c3, e5, c5, c3,e5,c5 all sleep time of 1 in case defined do guitar2 dont work

guitar2
guitar

# ask eric about d set 9-11

#piano measure 12-15 #1  bottom

piano
piano2
piano3
piano4

#guitar measure 12-15

guitar2
guitar
guitar
guitar2

#d set measure 12-15 ask eric about it

#measure 16-19 piano

#(measure 16)
piano3

#(measure 17)
piano2

#(measure 18)
piano5

#measure 19
piano4

#measure 16-19 guitar

sleep 4

guitar2
guitar
guitar2
guitar


#measure 16-19 d.set



#measure 20-23 piano

#measure 20 piano
piano

#measure 21 piano
piano2

#measure 22 piano (perfect spot for paramaterized function since its slightly different than measure 18, which is piano5)

#measure 23
piano4

#measure 20-23 guitar
guitar2
guitar
guitar
use_synth :fm

# Starting amplitude
amps = [1.0, 0.9, 0.8, 0.6, 0.5, 0.3, 0.2, 0.1]

notes = [:e5, :c5, :a4, :e5, :c5, :c3, :e5, :c5]

8.times do |i|
  play notes[i], sustain: 0.5, amp: amps[i]
  sleep 1
end

stop

