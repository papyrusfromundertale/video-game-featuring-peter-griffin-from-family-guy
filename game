import pygame
from random import randint

pygame.init()

display_width = 800
display_height = 600

fat = 76
height = 110

white = (255,255,255)

gameDisplay = pygame.display.set_mode((display_width,display_height))
pygame.display.set_caption('shabalais gutta')

clock = pygame.time.Clock()
peter = pygame.image.load('gifin2.png')


def petergrifon(x,y):
    gameDisplay.blit(peter,(x,y))


def game_loop():
    x = (randint(0,800 - fat))
    y = (randint(0,600 - height))

    x_change = 3
    y_change = 3


    gameExit = False
    while not gameExit:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                gameExit = True

        if x > display_width - fat or x < 0:
            x_change = x_change * -1
        if y > display_height - height or y < 0:
            y_change = y_change * -1
        
        x += x_change
        y += y_change
    
        gameDisplay.fill(white)
        petergrifon(x,y)
        pygame.display.update()
        clock.tick(60)

game_loop()
pygame.quit()
quit()
