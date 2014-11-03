<#include <GL/glut.h>         
void display(void)
{
    glClear(GL_COLOR_BUFFER_BIT); 

	glPointSize(3.0);
	glBegin(GL_POINTS);
	 	glColor3f(1.0,1.0,0.0);
		glVertex2f(-0.5, -0.5);
	 	
		glColor3f(1.0,0.0,0.0);
		glVertex2f(-0.5, 0.5);
		
		glColor3f(0.0,0.0,1.0);
	 	glVertex2f(0.5, 0.5);
		
		glColor3f(0.0,1.0,0.0);
	 	glVertex2f(0.5, -0.5);
	glEnd();

	glFlush(); 
}
void init(){}

int main(int argc, char** argv)
{
	glutCreateWindow("simple"); 
	glutDisplayFunc(display);
	init();
	glutMainLoop();
}
