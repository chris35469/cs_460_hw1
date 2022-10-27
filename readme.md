# Homework Instructions

1. Create a **hw2** workspace using notes from [Getting-Started-with-ROS2-TurtleSim-and-Python](https://github.com/htil/Getting-Started-with-ROS2-TurtleSim-and-Python)
2. Copy the `script.py` in your projects workspace
3. Identify 3 combinations of **KP and KD gain terms** that move the turtle to `x = 5.0`
4. Run 5 trials for each Kp gain term. Report the total time for all trials using a graph (see the attached.png graph. Use provided  results.xlsx). You should have a total of 15 trials reported. 
Each trial should run under 40 seconds. 


## Use must implement the following functions

- `mainLoop()`
	- Create a PD controller to update self.u
	- Calculate the derivative term using self.error_prev and the most recent error
	- **This function must:** 
		-  call `self.setLinearVelocity()`
		-  call self.getError()
		-  define derivative variable 'e.g. `dedet = ...` '
		-  assign control value to `self.u` using the formula from our PID lecture
		-  store previous error to `self.error_prev`
- `getError(goalX, robotX)`
	- get the error using `goalX` and `robotX`
- `setLinearVelocity(u)`
	- publish the linear velocity using the publisher (`u`)

## **You must turn in the following deliverables (please read carefully):**
- **hw2_lastname.zip** file containing the following two files
	- **script.py** (your PD controller solution)
	- **hw2\_lastname_graph.png**  (your Kp results. You should have a total of 15 results, 5 for 3 different Kp/KD gain terms)


You **do not** have to turn in your excel file
