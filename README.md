# pokecode
'''Código para calcular a probabilidade de captura no pokemon platina'''

'''Code to calculate the probability of capture on pokemon platinum'''


    hp_max = int(input("HP_max: "))
    hp_current = int(input("HP_current: "))
    rate = int(input("rate: "))
    bonus_ball = float(input("Bonus_ball: "))
    bonus_status = float(input("Bonus_status: "))

    a = ((3 * hp_max - 2 * hp_current) * rate * bonus_ball / (3 * hp_max)) * bonus_status
    if a >= 255: 
        print("100%")
    else: 
        b = 65535 * (a/255)**0.25

        p = ((b+1)/65535)**4

        print("%.2f"%a)
        print("%.0f"%b)
        print(p)
        print("capture probability:%.2f%%" %(p * 100))
    
