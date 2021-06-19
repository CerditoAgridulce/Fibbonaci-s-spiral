# Warning! It works for manim community edition version 0.7.0
# Atención! Funciona para la versión 0.7.0 de manim community edition

from manim import*


"""
Eng:
This is going to be the spiral structure. Every parameter will be explained later but summarizing squares indicates how many squares there are going to be, square_widht is 
the widht of the squares' vertices and scale is an scaling factor which can be changed depending on the number of squares you want to add. Finally, you can set the colors of the
objects here or you can do it later. 


Esp:

Esta será la estructura para la espiral. Cada uno de sus parámetros será explicado mejor más adelante pero en resumen squares indica la cantidad de cuadrados que habrá
square width el ancho que tendrán los vértices de los cuadrados y scale es un factor de escalado que se puede cambiar según el número de cuadrados que se quieran agregar. 
Finalmente, puedes elegir los colores aquí o más adelante. 

"""
def spiral(squares = 11, squares_widht = 1, scale = 0.1, squares_color = WHITE, spirals_color = WHITE) :
	def reorder(mob1,mob2,pos):
		mob1.next_to(mob2, pos, buff = 0)
# squence is the begining of the Fibbonacci's Sequence. In order to automate it's creation, we only add the first 2 items of the list
# sequence es el comienzo de la secuencia de Fibbonacci. Para automatizar su creación, solo añadimos los dos primeros items de la lista. 
	sequence = [1,1]
# You can choose how many squares you want to add by changing the squares parameter. In my opinion, 11 looks very nice with a scale of 0.1.
# Puedes elegir cuantos cuadrados quieres añador cambiando el parámetro squares. En mi opinión, 11 se ven muy bien con un escalado de 0.1. 
	n_squares = squares
	positions = [RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN,RIGHT,UP,LEFT,DOWN]
	angles = [1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,3,0,]



# Eng: 
# Ok, let's explain how this is going to work. 
# 
# First, we are going to create the squares and give each of them a position. For me, it looks nice to put the first square in the center, then the second square
# next to it at it's right, then the next at the top of both, next at left, next bottom and so on. The positions in the "positions" list will be used to choose the directions.
# I know you could do something like cycle data or something, but I am too noob to understand how this works, so this is what you have. 
# 
# Second, we are going to pick 2 opposite vertices from a square and draw an arc between these point. If we do it for every square we get an spiral. The numbers in the "angles" list
# will be used to choose these vertices. I know you could do something like cycle data or something, but I am too noob to understand how this works, so this is what you have.  
# #hen, we will put all this stuff inside a VGroup and return it.
# 
# 
# Esp:
# Venga, vamos a explicar como funciona esto. 
# 
# Primero, crearemos los cuadrados y les daremos una posicion a cada uno de ellos. Creo que se ve muy bien poner el primero al centro, el siguiente a la derecha del primero, 
# el siguiente arriba de esos dos, el siguiente a la izquierda de todos, el siguiente abajo y así sucesivamente. La lista "positions" sirve para elegir estas direcciones automaticamente. 
# Sé que podriamos usar algo como cycle pero soy demasiado novato como para entender como funciona, así que esto es lo que tenemos. 
# 
# Segundo, vamos a elegir 2 vertices opuesto de un cuadrado y dibujaremos un arco entre ellos. Si lo hacemos para cada cuadrado, obtenemos una espiral. Los números en la lista "angles"
# sirve para elegir esas posiciones automáticamente. Sé que podriamos usar algo como cycle pero soy demasiado novato como para entender como funciona, así que esto es lo que tenemos.


	for i in range(n_squares):
		sequence.append(sequence[i+1]+sequence[i])
	scaling = scale
	line_width = squares_widht
	square_1 = Square(stroke_width = line_width).scale(sequence[0]*scaling)
	squares_group = VGroup(square_1)
	square_list = [square_1]
	arcs = VGroup(ArcBetweenPoints(square_1.get_vertices()[1],square_1.get_vertices()[3]))


# Here we automate the creation of squares and spirals. 
# Aquí automatizamos la creación de cuadrados y espirales
	for c in range(squares):
		new_square = Square(stroke_width = line_width).scale(sequence[c+1]*scaling)
		reorder(new_square,squares_group,positions[c])
		new_arc = ArcBetweenPoints(new_square.get_vertices()[angles[c+1]],new_square.get_vertices()[angles[c+3]])
		square_list.append(new_square)
		
		squares_group.add(new_square)
		arcs.add(new_arc)

# Here we make a group with everything, move it to the center and make it colorful.
# Aquí creamos un grupo con todo, lo movemos al centro y le damos colorines
	spiraling = VGroup(squares_group.set_color(squares_color), arcs.set_color(spirals_color)).scale(0.25)
	spiraling.move_to([0,0,0])
	return(spiraling)

# Example 1. Looks nice, right? Using spiral()[1] you can draw just the spiral
# Ejemplo 1. Se ve bien, verdad? Usando spiral()[1] puedes dibujar solo la espiral

class Fibonnacci_white(Scene):
	def construct(self):
		self.wait()
		self.play(Create(spiral()), run_time = 5)
		self.wait()

# Example 2. With a bit of color we can see small gaps between spirals but they are so small that in an animated video you can't notice them
# Ejemplo 2. Con un poco de color podemos ver pequeños espacioes entre las espirales pero son tan pequeños que en un video animado apenas se notan. 


class Fibonnacci_red_green(Scene):
	def construct(self):
		self.wait()
		self.play(Create(spiral(squares_color = RED, spirals_color = GREEN)), run_time = 5)
		self.wait()

rainbow_color = color_gradient([PURPLE, BLUE, GREEN, ORANGE, YELLOW, RED], 6)

# Make it colorfull with different options!
# Hazlo colorido con diferentes opciones
class Fibonnacci_rainbow(Scene):
	def construct(self):
		self.wait()
		self.play(Create(spiral().set_color(rainbow_color), run_time = 5))
		self.wait()



"""
Eng: 

Improvements list:
- Be able to draw the spirals as a rainbow and not every arc as a rainbow itself
- Automate the scale depending on how big the final spiral is. Doing it by hand is booooring.
- Be able to draw each arc or square individually.
- Find a way to remove the gaps. Maybe doing another arc between point using the end and the begining of the arcs may solve. 
- Improve the aesthetics. Looks nice but it could look nicer. 

Esp:

Lista de mejoras:
- Ser capaz de dibujar las espirales como un arcoiris y no cada arco como un arcoiris por si mismo. 
- Automatizar la escala según lo grande que sea la espiral final. Hacerlo a mano es aburriiiiiiiiiiiido
- Ser capaz de dibujar cada arco o cuadrado individualmente.
- Encontrar una manera de eliminar los espacios. Tal vez crear un arco entre el principio y el fin de otro arco lo arregle.
- Mejorar la estetica. Se ve bien, pero se podría ver mejor. 
"""
