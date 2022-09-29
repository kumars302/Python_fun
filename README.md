# Python_fun
import random
def rand1(num):
    res = []

    for j in range(num):
        res.append(random.randint(0,81))
def gme_sudoku() :
 a1 = [0] * 82
 i1=0
 fl=0
 a12345 = []
 for i1234 in range(81):
     a12345.append([])
 def sdku(i,fl):
    if fl==1 :
        a1[i]=0
        a1[i+1]=0
        print("yes")
    s={1,2,3,4,5,6,7,8,9}
    a11 = set()
    row = int(i / 9)
    for j in range(0, 9):
        a11.add(a1[(row * 9 + j)])
    col = (i % 9)
    for k in range(0, 9):
        a11.add(a1[col + 9 * k])
    if row < 3 and col < 3:
        a11.add(a1[0])
        a11.add(a1[1])
        a11.add(a1[2])
        a11.add(a1[9])
        a11.add(a1[10])
        a11.add(a1[11])
        a11.add(a1[18])
        a11.add(a1[19])
        a11.add(a1[20])
    if row < 3 and 2 < col < 6:
        a11.add(a1[3])
        a11.add(a1[4])
        a11.add(a1[5])
        a11.add(a1[12])
        a11.add(a1[13])
        a11.add(a1[14])
        a11.add(a1[21])
        a11.add(a1[22])
        a11.add(a1[23])
    if row < 3 and 5 < col < 9:
        a11.add(a1[6])
        a11.add(a1[7])
        a11.add(a1[8])
        a11.add(a1[15])
        a11.add(a1[16])
        a11.add(a1[17])
        a11.add(a1[24])
        a11.add(a1[25])
        a11.add(a1[26])
    if 2 < row < 6 and col < 3:
        a11.add(a1[27])
        a11.add(a1[28])
        a11.add(a1[29])
        a11.add(a1[36])
        a11.add(a1[37])
        a11.add(a1[38])
        a11.add(a1[45])
        a11.add(a1[46])
        a11.add(a1[47])
    if 2 < row < 6 and 2 < col < 6:
        a11.add(a1[30])
        a11.add(a1[31])
        a11.add(a1[32])
        a11.add(a1[39])
        a11.add(a1[40])
        a11.add(a1[41])
        a11.add(a1[48])
        a11.add(a1[49])
        a11.add(a1[50])
    if 2 < row < 6 and 5 < col < 9:
        a11.add(a1[33])
        a11.add(a1[34])
        a11.add(a1[35])
        a11.add(a1[42])
        a11.add(a1[43])
        a11.add(a1[44])
        a11.add(a1[51])
        a11.add(a1[52])
        a11.add(a1[53])
    if 5 < row < 9 and col < 3:
        a11.add(a1[54])
        a11.add(a1[55])
        a11.add(a1[56])
        a11.add(a1[63])
        a11.add(a1[64])
        a11.add(a1[65])
        a11.add(a1[72])
        a11.add(a1[73])
        a11.add(a1[74])
    if 5 < row < 9 and 2 < col < 6:
        a11.add(a1[57])
        a11.add(a1[58])
        a11.add(a1[59])
        a11.add(a1[66])
        a11.add(a1[67])
        a11.add(a1[68])
        a11.add(a1[75])
        a11.add(a1[76])
        a11.add(a1[77])
    if 5 < row < 9 and 5 < col < 9:
        a11.add(a1[60])
        a11.add(a1[61])
        a11.add(a1[62])
        a11.add(a1[69])
        a11.add(a1[70])
        a11.add(a1[71])
        a11.add(a1[78])
        a11.add(a1[79])
        a11.add(a1[80])
    for x in a12345[i] :
        a11.add(x)
    for y in range(i+1,80) :
        a12345[y]=[]
    if set(a12345[i])==s-a11 :
         a12345[i]=[]
    if fl==1 :
        print(a1[0:9])
        print(a1[9:18])
        print(a1[18:27])
        print(a1[27:36])
        print(a1[36:45])
        print(a1[45:54])
        print(a1[54:63])
        print(a1[63:72])
        print(a1[72:81])
        print("hi a")
        print(i)
        print(a1[i])
        print(s-a11)
        print(fl)
    if len(s-a11)>0 :
        fl=0
        a1[81]=i
        print(s-a11)
        return (s-a11)
    elif len(s-a11)==0 :
        print("hi")
        fl=1
        print(fl)
        print(i-1)
        return sdku((i-1),fl)
 while i1<81:
        i1=a1[81]
        print(i1)
        a123=list(sdku(i1, fl))
        i1=a1[81]
        a1[i1]=random.choice(a123)
        a12345[i1].append(a1[i1])
        print(a1[i1])
        i1=i1+1
        a1[81]=i1
 return a1
def sdku_table(b1) :
    print(b1[0:9])
    print(b1[9:18])
    print(b1[18:27])
    print(b1[27:36])
    print(b1[36:45])
    print(b1[45:54])
    print(b1[54:63])
    print(b1[63:72])
    print(b1[72:81])

b13=gme_sudoku()
sdku_table(b13)
