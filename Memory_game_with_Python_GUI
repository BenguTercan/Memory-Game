from tkinter import *
import time
import random

def started() :

    count = 5
    button.destroy()    
    printSmt(count)


def printSmt(count):

    def numbers():

        number = random.randint( 0,9 )
        return number

    depola_sayi = ""   

    for x in range ( count ) : 

        canvas = Canvas( width = 900 , height = 600 , bg = 'pink' )
        canvas.pack ( expand = YES , fill = BOTH )

        xloc = random.randint ( 50 , 800 )
        yloc = random.randint ( 50 , 500 )

        ekran_sayi = numbers()

        depola_sayi += str ( ekran_sayi )

        canvas.create_text ( xloc , yloc , text = ekran_sayi , fill = 'steelblue' , font = ( "arial" , 40 , "bold" ) )

        root.update()
        time.sleep( 0.8 )
        canvas.pack_forget()
        root.update()
        time.sleep( 0.5 )
        
    print ( depola_sayi )
    
    def sayi_al(yenisay) :
        
       yenisay.get()

       if yenisay.get() != depola_sayi :
           kutu.pack_forget()
           buton2.pack_forget()

           label_cong = Label ( root , anchor = CENTER , text = "GAME OVER..." , font = ( "Helvetica" , 25 , "bold" ) , 
           bg = 'pink' , fg = 'steelblue' )

           label_cong.pack( expand = 1 , ipadx = "20" , ipady = "15" )
           root.update()
           time.sleep( 1.1 )
           root.quit()


       if yenisay.get() == depola_sayi :

           new_count = count + 1
           kutu.pack_forget()
           buton2.pack_forget()
           
           label_cong2 = Label ( root , anchor = CENTER , text = "CONGRATULATIONS ! Go to next level." , bg = 'pink' , fg = 'steelblue' ,
           font = ( "Helvetica" , 25  ,"bold" ) )

           label_cong2.pack ( expand = 1 , ipadx = "20" , ipady ="15" )

           root.update()
           time.sleep( 1.8 )
           label_cong2.pack_forget()
           
           return printSmt ( new_count )

     
    yenisay = StringVar()

    kutu = Entry ( root, textvariable = yenisay , width = 40 , font = ( "Helvetica" , 20 , "bold" ) , 
    fg = 'HotPink4' ,  bg = 'rosy brown' )

    kutu.pack ( expand = "1" , ipadx = "20" , ipady ="15" )

    buton2 = Button ( root, text = "TRY" , command = lambda : sayi_al ( yenisay ) , 
    bg = 'rosy brown' , fg = "HotPink4" , font = ( "Helvetica" , 15 , "bold" ), 
    relief = RAISED , activebackground ='rosy brown' , activeforeground = "HotPink4")

    buton2.pack ( expand = "1.5" , ipadx = "20" , ipady = "15" )

    
root = Tk()

root.title ( "WELCOME TO THE MEMORY GAME !!" )
root.configure ( background = 'pink' )
root.geometry ( "900x600" )

button = Button ( root , text = "Start GAME" , command = started , bg = 'rosy brown' , fg = "HotPink4" , 
font = ( "Helvetica" , 30 , "bold italic" ) , 
relief = RAISED ,  activebackground = 'rosy brown' , activeforeground = "HotPink4" ) 
button.pack ( expand = "1"  , ipadx = "50" , ipady = "50" )

root.mainloop()
