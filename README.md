# CollectNewsPaperKarel
Stanford Computer Science Department (CS106A). 
/*
 * File: CollectNewspaperKarel.java
 * --------------------------------
 * At present, the CollectNewspaperKarel subclass does nothing.
 * Your job in the assignment is to add the necessary code to
 * instruct Karel to walk to the door of its house, pick up the
 * newspaper (represented by a beeper, of course), and then return
 * to its initial position in the upper left corner of the house.
 */
/* Created by BRYAN PACHECO This is the first assignment in the stanford course, the solution to the problem is as follows:*/

import stanford.karel.*;

public class CollectNewspaperKarel extends Karel {
	
	// You fill in this part
	public void run () {
		bringNewspaper();
		
		
		
	}
	
	/* the following is the algorithm for Karel to get to the Beeper and return it 
	 * and end up facing the same way it started*/
	private void bringNewspaper() {
		move();
		move();
		turnRight();
		move();
		turnLeft();
		move();
		pickBeeper();
		turnAround();
		move();
		turnRight();
		move();
		turnLeft();
		move();
		move();
		turnAround();
	}
	
	/* this is the new method i created so that Karel can understand
	 *  turnRight without having to type turnleft 3x.*/
	private void turnRight() {
		turnLeft();
		turnLeft();
		turnLeft();
	}
	/* this shows how instead of writing turnLeft twice 
	 *its better to create a turnAround command with two turnLefts*/
	
	private void turnAround() {
		turnLeft();
		turnLeft();
	}
}
