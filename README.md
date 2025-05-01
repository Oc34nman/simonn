# simonn
import pygame
import random
import math
import winsound

pygame.init()
pygame.display.set_caption("Simon!")
screen = pygame.display.set_mode((800, 800))

xpos = 0
ypos = 0
mousePos = (xpos, ypos)
hasClicked = False
pattern = []
playerpattern = []
playerTurn = True
pi = 3.14159265359
ded = False
pygame.time.wait(800)
game = False
    while game == False:
        event = pygame.event.wait()
        collsion(xpos,ypos)
#gameloop
while True:
    
    event = pygame.event.wait()
    #render section----------


    #game board
    pygame.draw.arc(screen,(155,0,0), (200,200,400,400), 2*pi, pi/2, 100)
    pygame.dra w.arc(screen,(214, 237, 36), (200,200,400,400), pi, (3 * pi / 2), 100)
    pygame.draw.arc(screen,(13, 191, 16), (200,200,400,400), pi/2, pi, 100)
    pygame.draw.arc(screen,(9, 44, 150), (200,200,400,400), 3*pi/2, 0, 100)
    pygame.display.flip()

    #more colors go here!
    
    pygame.display.flip()
    
    #end game loop
    pygame.quit()
    #input section----------------------------------------
    if event.type == pygame.QUIT:
        break
    
    if event.type == pygame.MOUSEBUTTONDOWN:
        hasClicked= True
        print("click")
    
    if event.type == pygame.MOUSEMOTION:
        mousePos = event.pos
        
    #update section----------------
