Question 1 :
        16000 of rows donot have v2_total = v1_total.
        this information is not relevant as almost every order shows some tiny diffrence which is mainly as the code was reordered internally which causes penny level rounding diffrence on nearly every order and the books prices was changed on purpose.
        so these are harmless noise and intentional change
Question 2 :
        985 orders are affected by the real bug.
        They have 'Express = True' and 'Category=Fragile' as common,
        all the orders having express and fragile are affected no other order is,
        on express orders are totally fine
Question 3 :
        19779.14 was overcharged, All of the orders were overcharged, 
        every affected order was charged more, none were charged less
Question 4 :
        Average diff for unaffected and non book orders is 0.0023
        The Q2 is real as there is a huge clean gap, normal orders differ by 1-2 cents but the affected 985 orders diff by $5 which creates a lap gap instead of a smooth curve or increase, which proves that affected is a seperate issue
Question 5 :
        The Express and fragile orders are being affected , therefore It can be assumed that the express and fragile orders sur charge which is apllied is calculated incorrectly
        
        