import pygame
import sys
from functions import *
from text import Button

# print(mendel(2,2,2))
# print(calculate_offspring(1,0,0,1,0,1))

print("Mendel's First Law")
print("Input number of individuals that are...")
homo_dom_input = input("Homozygous Dominant: ")
hetero_input = input("Heterozygous: ")
homo_rec_input = input("Homozygous Recessive: ")
print("Input the number of couples that are possessing the following genotypes:")
AAAA_input = input("AA-AA: ")
AAAa_input = input("AA-Aa: ")
AAaa_input = input("AA-aa: ")
AaAa_input = input("Aa-Aa: ")
Aaaa_input = input("Aa-aa: ")
aaaa_input = input("aa-aa: ")

pygame.init()
scr_w = 500
scr_h = 350
screen = pygame.display.set_mode((scr_w, scr_h))
clock = pygame.time.Clock()
SCREEN_UPDATE = pygame.USEREVENT
pygame.time.set_timer(SCREEN_UPDATE, 500)
pygame.display.set_caption("Bioinformatics: Heredity")

#mendel text
mendels = Button(105, 10, 40, 40, text = "Mendel's First Law", text_color = (204,84,96))
homo_dom = Button(110, 45, 40, 40, text = f"Homozygous Dominant: {homo_dom_input}", text_color = (164,212,209))
hetero = Button(72, 75, 40, 40, text = f"Heterozygous: {hetero_input}", text_color = (164,212,209))
homo_rec = Button(132, 125, 0, 0, text = f"Homozygous Recessive: {homo_rec_input}", text_color = (164,212,209))
prob_word = Button(135, 235, 0, 0, text = "Probability of Dominant Allele", text_color = (204,84,96))
prob_perc = Button(135, 280, 0, 0, text = f"{mendel(int(homo_dom_input),int(hetero_input),int(homo_rec_input))}%", text_color = (204,84,96))

#calculating expected offspring
calc = Button(365, 30, 0, 0, text = "Expected Offspring", text_color = (204,84,96))
AAAA = Button(325, 60, 0, 0, text = f"AA-AA: {AAAA_input}", text_color = (164,212,209))
AAAa = Button(325, 85, 0, 0, text = f"AA-Aa: {AAAa_input}", text_color = (164,212,209))
AAaa = Button(325, 110, 0, 0, text = f"AA-aa: {AAaa_input}", text_color = (164,212,209))
AaAa = Button(325, 135, 0, 0, text = f"Aa-Aa: {AaAa_input}", text_color = (164,212,209))
Aaaa = Button(325, 160, 0, 0, text = f"Aa-aa: {Aaaa_input}", text_color = (164,212,209))
aaaa = Button(325, 185, 0, 0, text = f"aa-aa: {aaaa_input}", text_color = (164,212,209))
num1 = Button(365, 235, 0, 0, text = "Number of Offpsring", text_color = (204,84,96))
num2 = Button(365, 250, 0, 0, text = "Displaying Dominant Phenotype", text_color = (204,84,96))
num_off = Button(365, 290, 0, 0, text = str(calculate_offspring(int(AAAA_input),int(AAAa_input),int(AAaa_input),int(AaAa_input),int(Aaaa_input),int(aaaa_input))), text_color = (204,84,96))

while True:
	screen.fill(((46,65,87)))
	mendels.draw(screen, 30)
	homo_dom.draw(screen, 25)
	hetero.draw(screen, 25)
	homo_rec.draw(screen, 25)
	pygame.draw.rect(screen, (244,217,220), (30,220,210,100))
	prob_word.draw(screen, 20)
	prob_perc.draw(screen, 90)
	calc.draw(screen, 30)
	AAAA.draw(screen, 25)
	AAAa.draw(screen, 25)
	AAaa.draw(screen, 25)
	AaAa.draw(screen, 25)
	Aaaa.draw(screen, 25)
	aaaa.draw(screen, 25)
	pygame.draw.rect(screen, (244,217,220), (261,220,210,100))
	num1.draw(screen, 20)
	num2.draw(screen, 20)
	num_off.draw(screen, 80)

	for e in pygame.event.get():
		if e.type == pygame.QUIT:
			pygame.quit()
			sys.exit()

	pygame.display.update()
