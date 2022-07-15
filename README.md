# SCRAP-OTT-progarm.py
import pygame
import time
import sysimport pygame
import time
import sys


pygame.init()

gray = (160, 160, 160)

titleImg = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657859670526.png")
openImg = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657858508688.png")
book01Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657852891625.png")
book02Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657853533884.png")
book03Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657853533775.png")
book04Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657853533520.png")
book05Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657853533636.png")

display_width = 1500
display_height = 750
gameDisplay = pygame.display.set_mode((display_width, display_height))
pygame.display.set_caption("SCRAP")

clock = pygame.time.Clock()



class Button:
    def __init__(self, img_in, x, y, width, height, img_act, x_act, y_act, action = None):
        mouse = pygame.mouse.get_pos()
        click = pygame.mouse.get_pressed()
        if x + width > mouse[0] > x and y + height > mouse[1] > y:
            gameDisplay.blit(img_act,(x_act, y_act))
            if click[0] and action != None:
                time.sleep(0)
                action()
        else:
            gameDisplay.blit(img_in,(x,y))

class Button2:
    def __init__ (self,img_in,x,y,width,height,img_act,x_act,y_act, action=None):
        mouse = pygame.mouse.get_pos()
        click = pygame.mouse.get_pressed()
        if x + width > mouse[0] > x and y + height >mouse[1] > y:
            gameDisplay.blit(img_act,(x_act,y_act))
            
def quitgame():
    pygame.quit()
    sys.exit()


def mainmenu():

    menu = True

    while menu:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                pygame.quit()
                sys.exit()

        gameDisplay.fill(gray)
        book01 = gameDisplay.blit(book01Small_Img,(90,400))
        book02 = gameDisplay.blit(book02Small_Img,(440,400))
        book03 = gameDisplay.blit(book03Small_Img,(800,400))
        book04 = gameDisplay.blit(book04Small_Img,(1150,400))
        book05 = gameDisplay.blit(book05Small_Img,(1500,400))
        titletext = gameDisplay.blit(titleImg, (220,150))
        book01button =Button(openImg,140,900,200,70,openImg,140,900,selectScreen)
        book02button =Button(openImg,490,900,200,70,openImg,490,900,selectScreen)
        book03button =Button(openImg,850,900,200,70,openImg,850,900,selectScreen)
        book04button =Button(openImg,1200,900,200,70,openImg,1200,900,selectScreen)
        book05button =Button(openImg,1550,900,200,70,openImg,1550,90w0,selectScreen)
        pygame.display.update()
        clock.tick(15)
def selectScreen():
    select = True
    
    while select:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                quitgame()
        gameDisplay.fill(gray)
        
        pygame.display.update()
        clock.tick(15)
        
mainmenu()



pygame.init()

gray = (160, 160, 160)

titleImg = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657859670526.png")
openImg = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657858508688.png")
book01Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657852891625.png")
book02Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657853533884.png")
book03Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657853533775.png")
book04Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657853533520.png")
book05Small_Img = pygame.image.load("/storage/emulated/0/Download/NAVER MYBOX/1657853533636.png")

display_width = 1500
display_height = 750
gameDisplay = pygame.display.set_mode((display_width, display_height))
pygame.display.set_caption("SCRAP")

clock = pygame.time.Clock()



class Button:
    def __init__(self, img_in, x, y, width, height, img_act, x_act, y_act, action = None):
        mouse = pygame.mouse.get_pos()
        click = pygame.mouse.get_pressed()
        if x + width > mouse[0] > x and y + height > mouse[1] > y:
            gameDisplay.blit(img_act,(x_act, y_act))
            if click[0] and action != None:
                time.sleep(0)
                action()
        else:
            gameDisplay.blit(img_in,(x,y))

class Button2:
    def __init__ (self,img_in,x,y,width,height,img_act,x_act,y_act, action=None):
        mouse = pygame.mouse.get_pos()
        click = pygame.mouse.get_pressed()
        if x + width > mouse[0] > x and y + height >mouse[1] > y:
            gameDisplay.blit(img_act,(x_act,y_act))
            
def quitgame():
    pygame.quit()
    sys.exit()


def mainmenu():

    menu = True

    while menu:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                pygame.quit()
                sys.exit()

        gameDisplay.fill(gray)
        book01 = gameDisplay.blit(book01Small_Img,(90,400))
        book02 = gameDisplay.blit(book02Small_Img,(440,400))
        book03 = gameDisplay.blit(book03Small_Img,(800,400))
        book04 = gameDisplay.blit(book04Small_Img,(1150,400))
        book05 = gameDisplay.blit(book05Small_Img,(1500,400))
        titletext = gameDisplay.blit(titleImg, (220,150))
        book01button =Button(openImg,140,900,200,70,openImg,140,900,selectScreen)
        book02button =Button(openImg,490,900,200,70,openImg,490,900,selectScreen)
        book03button =Button(openImg,850,900,200,70,openImg,850,900,selectScreen)
        book04button =Button(openImg,1200,900,200,70,openImg,1200,900,selectScreen)
        book05button =Button(openImg,1550,900,200,70,openImg,1550,90w0,selectScreen)
        pygame.display.update()
        clock.tick(15)
def selectScreen():
    select = True
    
    while select:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                quitgame()
        gameDisplay.fill(gray)
        
        pygame.display.update()
        clock.tick(15)
        
mainmenu()
