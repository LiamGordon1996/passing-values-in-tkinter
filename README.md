passing-values-in-tkinter
=========================

from Tkinter import * #Copied from online examples import tkMessageBox #Copied from online examples import Tkinter, Tkconstants, tkFileDialog #Copied from online examples import Tkinter as tk #Copied from online examples   class Example(tk.Frame):     def __init__(self, *args, **kwargs):         tk.Frame.__init__(self, *args, **kwargs)         self.instruction_window = None         self.instructions = tk.Button(self, text="Instructions", foreground="green", command=self.show_instructions)         self.instructions.pack(side="left")          self.enter_name_window = None         self.enter_name = tk.Button(self, text="Name", foreground="green", command=self.show_enter_name)         self.enter_name.pack(side="left")          self.question_1_window = None         self.question_1 = tk.Button(self, text="1", foreground="blue", command=self.show_question_1)         self.question_1.pack(side="left")          self.question_2_window = None         self.question_2 = tk.Button(self, text="2", foreground="blue", command=self.show_question_2)         self.question_2.pack(side="left")          self.question_3_window = None         self.question_3 = tk.Button(self, text="3", foreground="blue", command=self.show_question_3)         self.question_3.pack(side="left")          self.question_4_window = None         self.question_4 = tk.Button(self, text="4", foreground="blue", command=self.show_question_4)         self.question_4.pack(side="left")          self.question_5_window = None         self.question_5 = tk.Button(self, text="5", foreground="blue", command=self.show_question_5)         self.question_5.pack(side="left")          self.question_6_window = None         self.question_6 = tk.Button(self, text="6", foreground="blue", command=self.show_question_6)         self.question_6.pack(side="left")          self.question_7_window = None         self.question_7 = tk.Button(self, text="7", foreground="blue", command=self.show_question_7)         self.question_7.pack(side="left")          self.question_8_window = None         self.question_8 = tk.Button(self, text="8", foreground="blue", command=self.show_question_8)         self.question_8.pack(side="left")          self.question_9_window = None         self.question_9 = tk.Button(self, text="9", foreground="blue", command=self.show_question_9)         self.question_9.pack(side="left")          self.question_10_window = None         self.question_10 = tk.Button(self, text="10", foreground="blue", command=self.show_question_10)         self.question_10.pack(side="left")          self.score_window = None         self.score = tk.Button(self, text="Reveal Score", foreground="red", command=self.show_score)         self.score.pack(side="left")                 def show_instructions(self):         '''show the instruction window; create it if it doesn't exist'''         if self.instruction_window is None or not self.instruction_window.winfo_exists():             self.instruction_window = InstructionWindow(self)         else:             self.instruction_window.flash()      def show_enter_name(self):         '''show the instruction window; create it if it doesn't exist'''         if self.enter_name_window is None or not self.enter_name_window.winfo_exists():             self.enter_name_window = Enter_Name_Window(self)         else:             self.enter_name_window.flash()      def show_question_1(self):         '''show the question window; create it if it doesn't exist'''         if self.question_1_window is None or not self.question_1_window.winfo_exists():             self.question_1_window = Question_1_Window(self)         else:             self.question_1_window.flash()      def show_question_2(self):         '''show the question window; create it if it doesn't exist'''         if self.question_2_window is None or not self.question_2_window.winfo_exists():             self.question_2_window = Question_2_Window(self)         else:             self.question_2_window.flash()      def show_question_3(self):         '''show the question window; create it if it doesn't exist'''         if self.question_3_window is None or not self.question_3_window.winfo_exists():             self.question_3_window = Question_3_Window(self)         else:             self.question_3_window.flash()      def show_question_4(self):         '''show the question window; create it if it doesn't exist'''         if self.question_4_window is None or not self.question_4_window.winfo_exists():             self.question_4_window = Question_4_Window(self)         else:             self.question_4_window.flash()      def show_question_5(self):         '''show the question window; create it if it doesn't exist'''         if self.question_5_window is None or not self.question_5_window.winfo_exists():             self.question_5_window = Question_5_Window(self)         else:             self.question_5_window.flash()      def show_question_6(self):         '''show the question window; create it if it doesn't exist'''         if self.question_6_window is None or not self.question_6_window.winfo_exists():             self.question_6_window = Question_6_Window(self)         else:             self.question_6_window.flash()      def show_question_7(self):         '''show the question window; create it if it doesn't exist'''         if self.question_7_window is None or not self.question_7_window.winfo_exists():             self.question_7_window = Question_7_Window(self)         else:             self.question_7_window.flash()      def show_question_8(self):         '''show the question window; create it if it doesn't exist'''         if self.question_8_window is None or not self.question_8_window.winfo_exists():             self.question_8_window = Question_8_Window(self)         else:             self.question_8_window.flash()      def show_question_9(self):         '''show the question window; create it if it doesn't exist'''         if self.question_9_window is None or not self.question_9_window.winfo_exists():             self.question_9_window = Question_9_Window(self)         else:             self.question_9_window.flash()      def show_question_10(self):         '''show the question window; create it if it doesn't exist'''         if self.question_10_window is None or not self.question_10_window.winfo_exists():             self.question_10_window = Question_10_Window(self)         else:             self.question_10_window.flash()      def show_score(self):         '''show the reveal score window; create it if it doesn't exist'''         if self.score_window is None or not self.score_window.winfo_exists():             self.score_window = Score_Window(self)         else:             self.score_window.flash()    class InstructionWindow(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=100, height=2, text="Please enter your name and class before answering all of the questions. Click 'Finish' once you have answered all of the questions.")          self.text.pack(side="top", fill="both", expand=True)                       def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))    class Enter_Name_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=40, height=2, text= "Please enter your name and class." )         self.text.pack(side="top", fill="both", expand=True)          enter_name = Entry(self)         enter_name.pack()         enter_name.focus_set()                   def callback():             self.display_name = tk.Label(self, width=40, height=2, text = "Now please enter your tutor group.")             self.display_name.pack(side="top", fill="both", expand=True)             tutor = Entry(self)             tutor.pack()             tutor.focus_set()             Enter_0.config(state="disabled")              Enter_0_2 = Button(self, text="Enter", width=10, command=self.destroy)             Enter_0_2.pack()           Enter_0 = Button(self, text="Enter", width=10, command=callback)         Enter_0.pack()                            def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))    class Question_1_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=75, height=4, text = "1) Do you have the time to do at least twenty minutes of prefect duty each week?")         self.text.pack(side="top", fill="both", expand=True)          question_1_Var = IntVar() #creating a variable to be assigned to the radiobutton          Yes_1 = Radiobutton(self, text = "Yes", variable = question_1_Var, value=1, height=5, width = 20)         Yes_1.pack() #creating 'yes' option          #Here we are assigning values to each option which will be used in the validation          No_1 = Radiobutton(self, text = "No", variable = question_1_Var, value=2, height=5, width = 20)         No_1.pack() #creating 'no' option           def question_1_enter(self):             Enter_1.config(state="disabled")                       Enter_1 = Button(self, text= "Enter", width=10, command = question_1_enter)         Enter_1.pack()      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Question_2_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=75, height=4, text = "2) Are you currently involved in any committees that meet during a lunch or break time?" )         self.text.pack(side="top", fill="both", expand=True)                  question_2_Var = IntVar()                  Yes_2 = Radiobutton(self, text = "Yes", variable = question_2_Var, value = 1, height=5, width = 20)         Yes_2.pack()          No_2 = Radiobutton(self, text = "No", variable = question_2_Var, value = 2, height=5, width = 20)         No_2.pack()          Enter_2 = Button(self, text= "Enter", width=10)         Enter_2.pack()       def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Question_3_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=75, height=4, text = "3) Are you involved in paired reading, mentoring, peer mediation or helping hands?")         self.text.pack(side="top", fill="both", expand=True)          question_3_Var = IntVar()                  Yes_3 = Radiobutton(self, text = "Yes", variable = question_3_Var, value = 1, height=5, width = 20)         Yes_3.pack()          No_3 = Radiobutton(self, text = "No", variable = question_3_Var, value = 2, height=5, width = 20)         No_3.pack()          Enter_3 = Button(self, text= "Enter", width=10)         Enter_3.pack()      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Question_4_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=45, height=8, text = "4) How high has your attendance been in the last year?")         self.text.pack(side="top", fill="both", expand=True)          question_4_Var = IntVar()          A_4 = Radiobutton(self, text = "90-100%", variable = question_4_Var, value = 1, height=5, width = 20)         A_4.pack()          B_4 = Radiobutton(self, text = "80-90%", variable = question_4_Var, value = 2, height=5, width = 20)         B_4.pack()          C_4 = Radiobutton(self, text = "70-80%", variable = question_4_Var, value = 3, height=5, width = 20)         C_4.pack()          D_4 = Radiobutton(self, text = "Below 70%", variable = question_4_Var, value = 4, height=5, width = 20)         D_4.pack()          Enter_4 = Button(self, text= "Enter", width=10)         Enter_4.pack()      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Question_5_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=100, height=4, text = "5) What would you do if you were walking to class and you saw a first year crying? Tick all correct answers.")         self.text.pack(side="top", fill="both", expand=True)          question_5_Var1 = IntVar()         question_5_Var2 = IntVar()         question_5_Var3 = IntVar()          A_5 = Checkbutton(self, text = "Keep walking", variable = question_5_Var1, onvalue = 1, offvalue = 0, height=5, width = 20)         A_5.pack()          B_5 = Checkbutton(self, text = "Take them to guidance", variable = question_5_Var2, onvalue = 1, offvalue = 0, height=5, width = 20)         B_5.pack()          C_5 = Checkbutton(self, text = "Talk to them to resolve issue", variable = question_5_Var3, onvalue = 1, offvalue = 0, height=5, width = 20)         C_5.pack()          def calculate_score():              Enter_5.config(state="disabled")             #self.question_5.config(state="disabled")             if (question_5_Var2.get() == 1) and (question_5_Var3.get() == 1) and not question_5_Var1.get():                 print("calculate score has worked") #test lines                 score = score + 1             else:                 print("not worked") #testlines              return score          Enter_5 = Button(self, text= "Enter", width=10, command = calculate_score)         Enter_5.pack()          #return score      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Question_6_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=80, height=4, text = "6) What would you do if you saw a younger pupil sitting alone? Tick all correct answers.")         self.text.pack(side="top", fill="both", expand=True)                  question_6_Var1 = IntVar()         question_6_Var2 = IntVar()         question_6_Var3 = IntVar()          A_6 = Checkbutton(self, text = "Nothing", variable = question_6_Var1, onvalue = 1, offvalue = 0, height=5, width = 20)         A_6.pack()          B_6 = Checkbutton(self, text = "Talk to them", variable = question_6_Var2, onvalue = 1, offvalue = 0, height=5, width = 20)         B_6.pack()          C_6 = Checkbutton(self, text = "Alert guidance", variable = question_6_Var3, onvalue = 1, offvalue = 0, height=5, width = 20)         C_6.pack()          Enter_6 = Button(self, text= "Enter", width=10)         Enter_6.pack()      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Question_7_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=80, height=4, text = "7) What would you do if there was a fight between younger pupils? Tick all correct answers.")         self.text.pack(side="top", fill="both", expand=True)          question_7_Var1 = IntVar()         question_7_Var2 = IntVar()         question_7_Var3 = IntVar()         question_7_Var4 = IntVar()          A_7 = Checkbutton(self, text = "Nothing", variable = question_7_Var1, onvalue = 1, offvalue = 0, height=5, width = 20)         A_7.pack()          B_7 = Checkbutton(self, text = "Walk away", variable = question_7_Var2, onvalue = 1, offvalue = 0, height=5, width = 20)         B_7.pack()          C_7 = Checkbutton(self, text = "Instantly break them up", variable = question_7_Var3, onvalue = 1, offvalue = 0, height=5, width = 20)         C_7.pack()          D_7 = Checkbutton(self, text = "Alert the nearest teacher", variable = question_7_Var4, onvalue = 1, offvalue = 0, height=5, width = 20)         D_7.pack()          Enter_7 = Button(self, text= "Enter", width=10)         Enter_7.pack()      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Question_8_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=80, height=4, text = "8) If you saw a pupil bullying another pupil, what would you do? Tick all correct answers.")         self.text.pack(side="top", fill="both", expand=True)          question_8_Var1 = IntVar()         question_8_Var2 = IntVar()         question_8_Var3 = IntVar()         question_8_Var4 = IntVar()          A_8 = Checkbutton(self, text = "Nothing", variable = question_8_Var1, onvalue = 1, offvalue = 0, height=5, width = 20)         A_8.pack()          B_8 = Checkbutton(self, text = "Break them up", variable = question_8_Var2, onvalue = 1, offvalue = 0, height=5, width = 20)         B_8.pack()          C_8 = Checkbutton(self, text = "Talk to them individually", variable = question_8_Var3, onvalue = 1, offvalue = 0, height=5, width = 20)         C_8.pack()          D_8 = Checkbutton(self, text = "Alert guidance", variable = question_8_Var4, onvalue = 1, offvalue = 0, height=5, width = 20)         D_8.pack()          Enter_8 = Button(self, text= "Enter", width=10)         Enter_8.pack()      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Question_9_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=60, height=4, text = "9) If younger pupils are being cheeky to you, what would you do? Tick all correct answers.")         self.text.pack(side="top", fill="both", expand=True)          question_9_Var1 = IntVar()         question_9_Var2 = IntVar()         question_9_Var3 = IntVar()         question_9_Var4 = IntVar()          A_9 = Checkbutton(self, text = "Retaliate", variable = question_9_Var1, onvalue = 1, offvalue = 0, height=5, width = 20)         A_9.pack()          B_9 = Checkbutton(self, text = "Nothing", variable = question_9_Var2, onvalue = 1, offvalue = 0, height=5, width = 20)         B_9.pack()          C_9 = Checkbutton(self, text = "Give warning", variable = question_9_Var3, onvalue = 1, offvalue = 0, height=5, width = 20)         C_9.pack()          D_9 = Checkbutton(self, text = "Tell a teacher", variable = question_9_Var4, onvalue = 1, offvalue = 0, height=5, width = 20)         D_9.pack()          Enter_9 = Button(self, text= "Enter", width=10)         Enter_9.pack()      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Question_10_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=80, height=4, text = "10) If the same pupil from question 9 keeps messing around, what should you do? Tick all correct answers.")         self.text.pack(side="top", fill="both", expand=True)          question_10_Var1 = IntVar()         question_10_Var2 = IntVar()         question_10_Var3 = IntVar()         question_10_Var4 = IntVar()          A_10 = Checkbutton(self, text = "Retaliate", variable = question_10_Var1, onvalue = 1, offvalue = 0, height=5, width = 20)         A_10.pack()          B_10 = Checkbutton(self, text = "Nothing", variable = question_10_Var2, onvalue = 1, offvalue = 0, height=5, width = 20)         B_10.pack()          C_10 = Checkbutton(self, text = "Give warning", variable = question_10_Var3, onvalue = 1, offvalue = 0, height=5, width = 20)         C_10.pack()          D_10 = Checkbutton(self, text = "Alert SLT", variable = question_10_Var4, onvalue = 1, offvalue = 0, height=5, width = 20)         D_10.pack()          Enter_10 = Button(self, text= "Enter", width=10)         Enter_10.pack()      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))   class Score_Window(tk.Toplevel):     '''A simple instruction window'''     def __init__(self, parent):         tk.Toplevel.__init__(self, parent)         self.text = tk.Label(self, width=80, height=4, text = "You're score was:")         self.text.pack(side="top", fill="both", expand=True)          #print("Score is", score)          Enter_10 = Button(self, text= "Enter", width=10)         Enter_10.pack()      def flash(self):         '''make the window visible, and make it flash temporarily'''          # make sure the window is visible, in case it got hidden         self.lift()         self.deiconify()          # blink the colors         self.after(100, lambda: self.text.configure(bg="black", fg="white"))         self.after(500, lambda: self.text.configure(bg="white", fg="black"))     if __name__ == "__main__":     root = tk.Tk()     root.geometry("800x500") #defining the size of the root     root.title("Prefect Quiz") #defining root title     Example(root).pack(side="top", fill="both", expand=True)     root.mainloop()     #score = IntVar()
