# You should remove all the test cases before submission to examplify


################################################################
#Part 1
def superFibonacciSeqR(t2, n):
    return []

print(superFibonacciSeqR(4,10))
#ans: [1, 4, 5, 10, 20, 40, 80, 160, 320, 640]

sfs1 = superFibonacciSeqR(11,20)
print(sfs1[-3::])
#ans: [393216, 786432, 1572864]

def superFibonacciSeqI(t2, upperbound):
    return []

print(superFibonacciSeqI(4,10))
#ans: [1, 4, 5, 10]

#longone = superFibonacciSeqI(20,10**9876)
#print(longone[-1]%10000000)
#ans: 6179584

def smallestSecondTermSFScontains(n):
    return 1
print(smallestSecondTermSFScontains(2016))
print(smallestSecondTermSFScontains(9876))
print(smallestSecondTermSFScontains(2651336998912))
print(smallestSecondTermSFScontains(23592960))
#ans: 62, 2468, 9876, 44

################################################################
#Part 2
class PizzaShop:
    def __init__(self,pos,name,radius,starthour,endhour):
        self.pos = pos
        self.name = name
        self.radius = radius
        self.starthour = starthour
        self.endhour = endhour
def createZeroMatrix(n,m):
    return [[0 for i in range(m)] for j in range(n)]
def mTightPrint(m):
    for i in range(len(m)):
        line = ''
        for j in range(len(m[0])):
            line += str(m[i][j])
        print(line)

def PDMap(r,c,allPS,currentHour):
    return [[]]

allPS2 = []
allPS2.append(PizzaShop([20,10],'Amazing Pizza',10,8,22))
allPS2.append(PizzaShop([29,30],'Beloved Pizza',10,8,22))
#mTightPrint(PDMap(50,60,allPS2,10))
allPS3 = []
allPS3.append(PizzaShop([20,30],'Amazing Pizza',10,8,22))
allPS3.append(PizzaShop([38,30],'Beloved Pizza',10,8,22))
#mTightPrint(PDMap(50,60,allPS3,10))
allPS = []
allPS.append(PizzaShop([20,10],'Amazing Pizza',12,8,22))
allPS.append(PizzaShop([29,30],'Beloved Pizza',17,8,22))
allPS.append(PizzaShop([41,20],'Cute Pizza',16,14,22))
allPS.append(PizzaShop([45,55],'Delicious Pizza',12,8,22))
allPS.append(PizzaShop([10,58],'Elegant Pizza',12,8,22))
allPS.append(PizzaShop([35,68],'Fancinating Pizza',12,14,22))
allPS.append(PizzaShop([32,60],'Good Pizza',15,8,22))
allPS.append(PizzaShop([30,46],'Ideal Pizza',9,8,14))
#mTightPrint(PDMap(50,80,allPS,10))
#mTightPrint(PDMap(50,80,allPS,14))
allPSsmall = []
allPSsmall.append(PizzaShop([3,3],'Amazing Pizza',3,8,14))
allPSsmall.append(PizzaShop([6,6],'Bear Pizza',4,12,22))
#mTightPrint(PDMap(10,12,allPSsmall,10))
#mTightPrint(PDMap(10,12,allPSsmall,16))
#mTightPrint(PDMap(10,12,allPSsmall,12))
################################################################
# Part 3
def sumTo(str1,ops,n):
    return[]

from pprint import *
pprint(sumTo('199','+',100))
#Answer above should have 1 equation
pprint(sumTo('123456789','+-',100))
#Answer above should have 11 equations
#pprint(sumTo('111111','+-*',100))
#Answer above should have 4 equations
#pprint(sumTo('12345','+-*%',30))
#Answer above should have 2 equations
#pprint(sumTo('11111','+-',100))
#Answer above should have 1 equation
#pprint(sumTo('1234567','+-*/',100))
#Answer above should have 5 equations
#pprint(sumTo('1234567','+-&^',100))
#Answer above should have 6 equations
