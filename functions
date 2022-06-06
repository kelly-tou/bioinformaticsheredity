from structures import *

def mendel(k, m, n):
	i = m * m + 4 * n * n + 4 * m * n - 4 * n - m
	j = 4 * (k + m + n) * (k + m + n - 1)
	probability = round(((1 - float(i) / j) * 100),1)
	return probability

def calculate_offspring(a,b,c,d,e,f):
	offspring = (1*a + 1*b + 1*c + 0.75*d + 0.5*e + 0*f) * 2
	return offspring

def genotype(ancestor1, ancestor2):
	p = {"AA":0.0, "Aa":0.0, "aa":0.0}
	for k1,v1 in ancestor1.items():
		for k2,v2 in ancestor2.items():
			p["AA"] += v1*v2*prob_dict[(k1,k2)][0]
			p["Aa"] += v1*v2*prob_dict[(k1,k2)][1]
			p["aa"] += v1*v2*prob_dict[(k1,k2)][2]
	return p

AA = {"AA":1.0, "Aa":0.0, "aa":0.0}
Aa = {"AA":0.0, "Aa":1.0, "aa":0.0}
aa = {"AA":0.0, "Aa":0.0, "aa":1.0}
