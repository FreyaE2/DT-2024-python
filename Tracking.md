# Tracking what I did each day

**26/06** - I started to research easygui, this is what I got from the tutorials:

My code:
![My Code](https://github.com/FreyaE2/DT-2024-python/assets/129448624/980acb91-ba02-4513-b23b-fe5f90fc8899)

Output 1:
![Output 1](https://github.com/FreyaE2/DT-2024-python/assets/129448624/9ef33b32-3dea-4446-b54c-fafb9e4f738e)

Output 2:
![Output 2](https://github.com/FreyaE2/DT-2024-python/assets/129448624/a61ba035-27b8-47a3-ae6a-6fc58102a5fc)

Output 3:
![Output 3](https://github.com/FreyaE2/DT-2024-python/assets/129448624/0399dab3-242f-45a8-adc8-aa6f70d4888f)

Output 4:
![Output 4](https://github.com/FreyaE2/DT-2024-python/assets/129448624/35b1baa8-7ef9-4f71-a3a4-b5a38c86ea97)

Output 5:
![Output 5](https://github.com/FreyaE2/DT-2024-python/assets/129448624/fb495265-c7c1-49a9-a452-9946ab317a48)

Output 6:
![Output 6](https://github.com/FreyaE2/DT-2024-python/assets/129448624/fe841ccb-7f62-4eec-94a2-69b9caa13708)

**31/07** - I have begun to start my actual code, i moved to tkinter as there are more tutorials and through reading I found it easier to use on RepLit. This code is me figuring out design, buttons and placement

![image](https://github.com/user-attachments/assets/645d7f22-57d4-4cbd-8b95-4f290fef1adb)

![image](https://github.com/user-attachments/assets/21bbec7c-4cc1-459f-9ca7-a0fa87c7504f)

(if exit is clicked the program will destroy itself)

![image](https://github.com/user-attachments/assets/8a6cc17c-4e93-4cd8-8770-49f0aee0ae0e)

(The dictionary is a test one at the moment)

**02/08** Just more additions to my code to make it more like my first plan

![image](https://github.com/user-attachments/assets/5f0adc2e-bccd-477d-8fbc-c92d04cf9751)

Code to define when the "in stock" button is clicked

![image](https://github.com/user-attachments/assets/dcb30847-45ac-4d45-8951-43171f73f979)

When it's clicked this is what will show up, I now want to try to change the window colour and make the "in stock" more of a list instead of a row.

![image](https://github.com/user-attachments/assets/52952aad-0965-4563-9e37-534d445e5b5b)

![image](https://github.com/user-attachments/assets/998378c3-5463-4c5e-bba7-f910aafbe5b0)

I have done all the demo's for each button, now I have got to refine them and add real music

![image](https://github.com/user-attachments/assets/639ca45c-30fb-4090-a38e-22c0bb7cd627)

**18/09** Had to debug, the words would dissapear outside the window and wouldnt show, had to figure out how to make a list

Firstly I wanted to change the layout to what I had originally planned (Horizontal) so thats what I did (I used my old tests and research to figure out how to do it)

![image](https://github.com/user-attachments/assets/b1ea50b8-91d4-424e-b9b9-c3f8cac71543)

Code to align buttons (pady and padx is what I was missing)

![image](https://github.com/user-attachments/assets/7c772e65-8064-4e68-807d-e8c0ae019d09)

Button positions now

**20/09** Then I had to sort out how to make my songs into a list, I wanted it to be a dictionary type thing that the program could read from so I found out how to actaully code that and how I could make sure when the window is opened those songs would appear

![image](https://github.com/user-attachments/assets/cf42439b-d9ac-47ef-b69e-195e0d927d0c)

Code for the list (and names for the on loan list (fake names for now))

![image](https://github.com/user-attachments/assets/6575f915-a4e1-42a0-9984-4ca8950d3b32)

Code for reading from the list

![image](https://github.com/user-attachments/assets/a1ef7de8-2b54-4f3d-91c5-849e18d1c1a0)

What it looks like now when the button is pressed

The webpage is finally coming together and it is what i wanted it to look like, I need to tweak a few things and add names now.

**25/09** I started to add the list of songs I wanted into the list but they ended up showing outside the screen

![image](https://github.com/user-attachments/assets/83f70266-cc7c-49ba-ac26-a1dc14927974)

Showing the names being cut off

This made me realise that I would need to add a scroll bar into it

![image](https://github.com/user-attachments/assets/3a81e501-5c81-462c-9818-2def6707e6b2)

First test of the scroll bar (have to edit code later)

![image](https://github.com/user-attachments/assets/36ad7de4-921b-4397-acfe-a9e5c4c31869)

And this is what it ended up like, this meant I could scroll and see all the names

The only issue is that when it's put into full screen it looks weird but for now this is good

![image](https://github.com/user-attachments/assets/2fb4bda3-fc25-4cd8-83b9-3f01ad3e07a3)

When the window is in full screen



**FINAL CODE**
#How I have imported tkinter to use
import tkinter as tk
from tkinter import ttk

# Start the Tkinter main loop
root = tk.Tk()
root.geometry('400x400')
root.resizable(width=False, height=False)
root.title("Welcome")

#---colours to use later---
colour1 = '#ffd3b6'
colour2 = '#dfa3a5'
colour3 = '#c79eb0'
colour4 = '#000000'

#start of my main window
main_frame = tk.Frame(root, bg=colour1, pady=40) #inside colour change
main_frame.pack(fill=tk.BOTH, expand=True)
main_frame.columnconfigure(0, weight=1)
main_frame.rowconfigure(0, weight=1)
main_frame.rowconfigure(1, weight=1)

#In stock list that the in stock button will read from
in_stock_list = ['Kill the Director - The Wombats', 
                 'Angel - Massive Attack', 
                 'Enjoy the Silence - Depeche Mode',
                 'HOT TO GO - Chappell Roan',
                 'Iris - The Goo Goo Dolls'
                ]

#on loan list that the on loan button will read from
on_loan_list = ['Goo Goo Muck - The Cramps (JW)', 
                'Baby Doll- Dominic Fike (HK)', 
                'Change - Deftones (AM)', 
                'California Love - 2Pac (NB)', 
                'Sprinter - Dave (AB)'
               ]
#on loan list that the on loan button will read from
over_due_list = ['Monsoon - Tokio Hotel (3 days, AE)',
                 'Drive By - Train (6 days, JE)',
                 'Baby - Justin Bieber (1 day, LS)',
                 'Cry - CAS (1 week, AK)',
                 'Duvet - BOA (4 days, FE)'
               ]

#Programing the buttons to do something by defining the command
#--- defs---
def instock_clicked():
  window = tk.Tk()
  window.title('Stock')
  window.geometry('300x200')
  #Bold "in stock" at the top of the page
  label1_title = tk.Label(master = window, text = 'In Stock:', font='Calibri 24 bold') 
  label1_title.pack(pady=20)
  #---scroll bar---
  
  #this controls how far I can scroll
  canvas = tk.Canvas(window, width = 300, height = 100,  scrollregion=(0, 0, 300, 200)) 
  #the position of the arrows / scroll bar
  scrollbar = tk.Scrollbar(window, orient="vertical", command=canvas.yview) 
  canvas.configure(yscrollcommand=scrollbar.set)
  #this means that the scroll bar is on the right side and it has a vertical bar 
  scrollbar.pack(side="right", fill="y") 
  canvas.pack(side="left")
  frame = tk.Frame(canvas)
   #position of the frame and ensures all the text can be read 
  canvas.create_window((0, 0), window=frame, anchor="nw") 
  for i in in_stock_list: #how it reads from the 'in stock' list
    label_instock = tk.Label(master = frame, text = i, font='Calibri 10')
    label_instock.pack(pady=5) #the padding between each one
  

#when the button is clicked it will open a new window
def onloan_clicked():
  window2 = tk.Tk()
  window2.title('On Loan') #new window title
  window2.geometry('300x200') #new window size
  label2_title = tk.Label(master = window2, text = 'On Loan:', font='Calibri 24 bold')
  label2_title.pack(pady=20)
  canvas = tk.Canvas(window2, width = 300, height = 100,  scrollregion=(0, 0, 300, 200))
#---scroll bar---
  
  scrollbar = tk.Scrollbar(window2, orient="vertical", command=canvas.yview)
  canvas.configure(yscrollcommand=scrollbar.set)
  scrollbar.pack(side="right", fill="y")
  canvas.pack(side="left")
  frame = tk.Frame(canvas)
  canvas.create_window((0, 0), window=frame, anchor="nw")
  for i in on_loan_list: #how it reads from the 'on loan' list
    label_onloan = tk.Label(master = frame, text = i, font='Calibri 10')
    label_onloan.pack(pady=5) #the padding between each one

def overdue_clicked():
  window3 = tk.Tk()
  window3.title('Overdue')
  window3.geometry('300x200')
  label3_title = ttk.Label(master = window3, text = 'Over Due', font='Calibri 24 bold')
  label3_title.pack(pady=20)
  canvas = tk.Canvas(window3, width = 300, height = 100,  scrollregion=(0, 0, 300, 200))
  #--- scroll bar ---
  
  scrollbar = tk.Scrollbar(window3, orient="vertical", command=canvas.yview)
  canvas.configure(yscrollcommand=scrollbar.set)
  scrollbar.pack(side="right", fill="y")
  canvas.pack(side="left")
  frame = tk.Frame(canvas)
  canvas.create_window((0, 0), window=frame, anchor="nw")
  for i in over_due_list: #how it reads from the 'on loan' list
    label_overdue = tk.Label(master = frame, text = i, font='Calibri 10')
    label_overdue.pack(pady=5) #the padding between each one


#--- Buttons --- 
button1 = tk.Button(
  main_frame,
  background=colour2, #button background
  foreground=colour4, #text colour
  text='In Stock', #what the button says
  command=instock_clicked #what it does when it's clicked
)

button2 = tk.Button(
  main_frame,
  background=colour2,
  foreground=colour4,
  text='On Loan',
  command=onloan_clicked
)

button3 = tk.Button(
  main_frame,
  background=colour2,
  foreground=colour4,
  text='Overdue',
  command=overdue_clicked
)

button4 = tk.Button(
  main_frame,
  background=colour2,
  foreground=colour4,
  text='Exit',
  command=root.destroy #this is what closes the root page / only the main window
)

#pbutton placement, padx is padding on the x axis pady is padding on the y axis
button1.pack(side=tk.LEFT, padx=10, pady=10)
button2.pack(side=tk.LEFT, padx=10, pady=10)
button3.pack(side=tk.LEFT, padx=10, pady=10)
button4.pack(side=tk.BOTTOM, padx=5, pady=5)

#how it starts up the main root page
root.mainloop()










