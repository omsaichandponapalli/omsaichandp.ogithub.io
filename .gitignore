from tkinter import *
from PIL import Image,ImageTk
cricket=Tk()
cricket.configure(bg="white")
text_Input=StringVar()
total_runs=StringVar()
overall=StringVar()
six_balls=StringVar()
r=0
i=0
no_of_balls=0
count=0
opera=""
n=1.7
path = "/storage/emulated/0/Download/Virat.jpg" 
image = Image.open(path)
W,H = image.size
newW = int(W*n)
newH=int(H*n)
image = image.resize((newW, newH))
img = ImageTk.PhotoImage(image)

l=Label(bg="white",image=img)
title=Label(text="SCOREBOARD",font=('arial',20,'underline','bold'),fg="royal blue",bg="white")
title.place(x=120,y=30)

def six_balls_runs():
	global opera,k
	k=runs_label.get()
	if count==1 or count%6==2 or count%6==3 or count%6==4 or count%6==5 or count%6==0:
		if k=="No Ball":
			k="nb"
			opera+=str(k)+"   "
			six_balls.set(str(opera))
		elif k=="Wide":
			k="wd1"
			opera+=str(k)+"   "
			six_balls.set(str(opera))
		elif k=="Wicket":
			k="wc"
			opera+=str(k)+"   "
			six_balls.set(str(opera))
		elif k=="" or k==" " or k=="   ":
			six_balls.set(str(opera))
		else:
			opera+=str(k)+"   "
			six_balls.set(str(opera))
	elif count%6==1:
		opera=""
		opera+=str(k)+"   "
		six_balls.set(str(opera))
	else:
		pass
			
	
def runs_enter(item):
	global operator
	operator=str(item)
	text_Input.set(operator)

	
def overs_fun():
	global overs,no_of_balls,count
	overs=""
	k=runs_label.get()
	if k in ["0","1","2","3","4","5","6","7"]:
		no_of_balls+=1
		count+=1
		if no_of_balls<6:
			overs=(no_of_balls/10)
		elif no_of_balls%6==0:
			overs=no_of_balls//6
		else:
			overs=((no_of_balls%6)/10+(no_of_balls//6))
		overall.set(str(overs))
	elif k=="No Ball":
		no_of_balls=no_of_balls-2
		count=count-2
		if no_of_balls<6:
			overs=(no_of_balls/10)
		elif no_of_balls%6==0:
			overs=no_of_balls//6
		else:
			overs=((no_of_balls%6)/10+(no_of_balls//6))	
		overall.set(str(overs))
	else:
		pass
		
		
def runs_calculate():
	global operator,i
	global r
	k=runs_label.get()
	if k in ["0","1","2","3","4","5","6","7"]:
		r+=int(k)
		total_runs.set(str(r)+"-"+str(i))
	elif k=="Wicket":
		i+=1
		total_runs.set(str(r)+"-"+str(i))
	elif k=="Wide":
		r+=1
		total_runs.set(str(r)+"-"+str(i))
	else:
		pass


def back_space():
	text_Input.set("")
	
		
				
Runs=Label(cricket,text="RUNS",fg="green",font=('arial',14),bg="white")
Runs.place(x=150,y=668)

runs_label=Entry(textvariable=text_Input,relief=SUNKEN,width=6,bg="spring green",font=(None,14),fg="orange")
runs_label.place(x=290,y=663)

runs_calculator=Label(text="TOTAL SCORE",fg="red",font=('arial',14),bg="white")
runs_calculator.place(x=55,y=262)

overs_cal_lab=Label(text="OVERS",font=('arial',14),bg="white",fg="red")
overs_cal_lab.place(x=228,y=360)

overs_calculator=Label(textvariable=overall,relief=SUNKEN,width=6,bg="spring green",font=(None,14),fg="orange")
overs_calculator.place(x=400,y=350)

runs_scored=Label(textvariable=total_runs,relief=SUNKEN,width=6,bg="spring green",font=(None,14),fg="orange")
runs_scored.place(x=400,y=255)

btnz=Button(text="0",relief=RAISED,padx=26,pady=26,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter(0)]).place(x=150,y=750)
btno=Button(text="1",relief=RAISED,padx=26,pady=26,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter(1)]).place(x=250,y=750)
btntwo=Button(text="2",relief=RAISED,padx=26,pady=26,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter(2)]).place(x=350,y=750)
btnthree=Button(text="3",relief=RAISED,padx=26,pady=26,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter(3)]).place(x=450,y=750)
btnfour=Button(text="4",relief=RAISED,padx=26,pady=26,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter(4)]).place(x=150,y=870)
btnfive=Button(text="5",relief=RAISED,padx=26,pady=26,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter(5)]).place(x=250,y=870)
btnsix=Button(text="6",relief=RAISED,padx=26,pady=26,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter(6)]).place(x=350,y=870)
btnseven=Button(text="7",relief=RAISED,padx=26,pady=26,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter(7)]).place(x=450,y=870)
btnwide=Button(text="wide",relief=RAISED,padx=16,pady=16,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter("Wide")]).place(x=150,y=990)
btnwicket=Button(text="wicket",relief=RAISED,padx=16,pady=15,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter("Wicket")]).place(x=272,y=991.5)
btnno_ball=Button(text="NoBa",relief=RAISED,padx=16,pady=16,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_enter("No Ball")]).place(x=420,y=990)
this_over=Label(text="THIS OVER",fg="green",bg="white",font=(None,14))
this_over.place(x=0,y=455)
this_over_label=Label(textvariable=six_balls,bg="spring green",font=(None,10),width=21).place(x=265,y=460)


btnenter=Button(text="Enter",relief=RAISED,padx=150,pady=16,bd=13,bg="spring green",activebackground="spring green",command=lambda: [runs_calculate(), overs_fun(),six_balls_runs()]).place(x=150,y=1090)
btnback_space=Button(text="Backspace",relief=RAISED,padx=113,pady=11,bd=12,bg="spring green",activebackground="spring green",command=lambda: [back_space()]).place(x=150,y=1190)

cricket.mainloop()
