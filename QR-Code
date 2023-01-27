import qrcode as qq
from tkinter import *
# from tkinter import messagebox

def reset():
    webEntry.delete(0,END)
    webEntry.config(bg='white')
    webEntry2.delete(0,END)
    webEntry2.config(bg="white")
   
def QRCode():
    website = webEntry.get()
    website2 = webEntry2.get()
    if len(website)<1:
        messagebox.showinfo('QR Generator','Please Enter text /url /number :)')
    if len(website2)<1:
        messagebox.showinfo('QR Generator','Please Enter file name :)')
    else:

        qr=qq.make(website)
        qr.save(website2+'.png')
        messagebox.showinfo('QR Generator','QR Code is generated Sucessfully :)')
    

root=Tk()

root.geometry("500x440+420+100")
root.config(bg="white")
root.iconbitmap('D:\\Python\\qrcodegenerator\\qr-code.ico')
root.title('QR code generator')

Label(root,text="Enter Your (TEXT/ URL/ NUMBER)",font="arial 20 bold",bg="white",fg="gray").pack(pady=(10,0))

webEntry = Entry(root,fg='black',bg="white",font="arial 16 bold",width=36,relief=GROOVE,bd=5)
webEntry.pack(pady=(30,30),ipady=10)
Label(root,text="           Enter Your QR-NAME",font="arial 20 bold",bg="white",fg="gray").place(x=20,y=170)

webEntry2 = Entry(root,fg='black',bg="white",font="arial 12 bold",width=36,relief=GROOVE,bd=5)
webEntry2.pack(side=BOTTOM,ipady=10,pady=(0,160))
Button(root,text="RESET",font="candara 15 bold",bg="gray",fg="black",width="12",command=reset).place(x=65,y=340)
Button(root,text="GENERATE QR",font="candara 15 bold",bg="gray",fg="black",width="12",command=QRCode).place(x=285,y=340)

root.mainloop()
