# Loop-in-glowscript

GlowScript 2.7 VPython
# program moves a ball along the x-axis using a simple loop

# initial conditions 
object=sphere(pos=vector(-5,0,0), # initial position (x,y,z)
    radius=0.3, # radius of sphere
    color=color.cyan, # color of sphere
    make_trail=True) # leave a trail as the object moves
move=vector(0.5,0,0) # how much the object will move per step  
t=0 # start time, usually zero

step=1 # size of step, will vary on situation 

while t < 20: # start of while loop with end condition
    rate(50) # how fast to output images, larger = faster
    object.pos=object.pos + move*step # moving the object
    t = t+ step # increment the time, also at end of loop

# output statement for values, useful for debugging
print(object.pos, " m is the final position of the object.") 
print(object.pos.x, " m is the final x position of the object.")
