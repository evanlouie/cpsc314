Lab 0
======
Name:	Evan Louie
CSID:	m6d7
SID:	72210099

p0 changes:

	openglDemo.cpp:38
	------------------
		glRotatef(gAngle, 1.0,0.0,0.0)

p1 Debugging:
	
	Bug 1: list.hpp:68
		size==MaxSize fails
	-----------------------
		Cause:
			mSize++ is called twice in the case the else clause is executed in the function list<Elem>::append(Elem *elem)
		Fix:
			Move the mSize++ from in append() to the if section of the the if statement.

	Bug 2: ListIterator.hpp:110
		function getNext() not found
	---------------------------------
		Cause:
			this->getNext() not defined.
		Fix:
			Change 'this' to 'mNode'.

	Bug 3: list.hpp:141
		Head of the list isn't being set properly
	----------------------------------------------
		Cause:
			Setting the next head of the list isn't being set because the line is commented out.
		Fix:
			Uncomment the line.

	Animal.h:19
		Improper deconstructor is being used
	----------------------------------------
		Cause:
			Animal deconstructor is being called instead of the Cow deconstructor.
		Fix:
			add the virtual keyword to the deconstructor


"I have read and understood the cheating policies at http://www.ugrad.cs.ubc.ca/~cs314/Vjan2013/cheat.html".