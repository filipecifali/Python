while True: 
    option  = input ('Insert your option:  ')
    
    if option.isdigit() and option!='1' and option!='2':
        print ('''<<Your NUMBER OPTIONS ARE: (1:'HYPOTENUSE',2:'CATHETUS') >>\n<<<<   Insert your option again and press <<Enter>   >>>>\n''')
    elif option.isalpha() and option!='1' and option!='2':
        print (''''<<ERROR>>Your options are NUMBERS!!!\n\n<<Your NUMBER OPTIONS ARE: (1:'HYPOTENUSE',2:'CATHETUS') >>\n<<<<   Insert your options again and press <<Enter>   >>>>\n''')
    elif not option.isalnum():
        print (''''<<ERROR>>Your options are NUMBERS!!!\n\n<<Your NUMBER OPTIONS ARE: (1:'HYPOTENUSE',2:'CATHETUS') >>\n<<<<   Insert your options again and press <<Enter>   >>>>\n''')            
    else: 
        while True:
            numbs = input('Insert your two sides value separated by the <<space>>:')               
            if numbs.isdigit():
                try:
                    if '' in numbs:                                                         
                        numbs = numbs.split()
                        if numbs[0].isalnum() and numbs[1].isalnum():
                            print('Two numbers are necessart foloowi by the space')
                            break
                        elif numbs[0].isalpha() and numbs[1].isalpha():
                            print('LETTERare necessart foloowi by the space')
                            break
                        else: 
                            numbs[0] = float(numbs[0])
                            numbs[1] = float(numbs[1])
                            hypotenuse = ((numbs[0]**2) + (numbs[1]**2))**(1/2)
                            print('<<<<<    The hypotenuse value is: %.2f    >>>>>'%(hypotenuse))
                            pass
                    else: break
                except:
                    print('need space')
            else: break                                                                   
        else:pass
else: 
    print('done')
