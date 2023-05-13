# Group Name
# //////////////////////////////////////////////////////
# ////////////    Coding Comrades  /////////////////////  
# //////////////////////////////////////////////////////
# Group Leader
# ----------->>>>>>>>>>>>>>>>>>>>>>>>>>>>>-------------- 
# ----------->>>>>>  Aiman Shabbir  <<<<<<--------------
# -----------<<<<<<<<<<<<<<<<<<<<<<<<<<<<<--------------
# Group Members 
# ------------>>>>>  ALishba Shaukat <<<< --------------
# ------------>>>>>  Mehvish Shareef <<<< --------------
# ------------>>>>>  Shaista Parveen <<<< --------------
# ------------>>>>>     Laiba Noor   <<<< --------------
# Project Title
# """"""""""""""""""""""""""""""""""""""""""""""""""""""
# """""""""""""""  Triathlon PK  """""""""""""""""""""""
# """"""""""""""""""""""""""""""""""""""""""""""""""""""
# Date of Creation 
# ******************************************************
# ***************   01-May-2023  ***********************
# ******************************************************
# Language 
# \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
# \\\\\\\\\\\\\\      Python     \\\\\\\\\\\\\\\\\\\\\\\
# \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
i=1
while i==1:
    print("                       ************************************************************")
    print("                       ************************************************************")
    print("                       ** >>>>>>>>       Welcome To Triathlon PK        <<<<<<<< **")
    print("                       ************************************************************")
    print("                       ************************************************************")
    print("                       **|| Option 1 About Triathlon                           ||**")
    print("                       **|| Option 2 to Register Student Athletes              ||**")
    print("                       **|| Option 3 to See Trainers Profiles                  ||**")
    print("                       **|| Option 4 to Read Athlete's record                  ||**")
    print("                       **|| Option 5 to See Events of Triathlon                ||**")
    print("                       **|| Option 6 to See Results of Competitions            ||**")
    print("                       **|| Option 7 to For Training of Athletes               ||**")
    print("                       **|| Option 8 to For Feedback                           ||**")
    print("                       **|| Option 9 to Read Reviews                           ||**")
    print("                       **|| Only Admin Enter PIN code to Remove File           ||**")
    print("                       **|| Option 10 to End or Quit                           ||**")
    print("                       ************************************************************")
    print("                       ************************************************************")
    operation = int(input("Choose Your Option:  "))
# Choose operation 1 containing Triathlon class to give information & Contact Details about Triathlon Pk.
    if operation == 1:
        class Triathlon: #class 
            print("\n>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>")
            print(">>>>>>>>>>>>>>>>>>>>>>>>>>>>>   About Us   <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<")
            print("<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<\n")
            def __init__(self, name, distance, location, participants, contact): #constructor & Attributes
                self.name = name
                self.distance = distance
                self.location = location
                self.participants = participants
                self.contact = contact
            def get_details(self): #Method
                return f"* Name of Triathlon: {self.name}.\n* Distance of Triathlon PK: {self.distance} distance from Multan Airport.\n* Location of Triathlon Pk: Triathlon PK is held in {self.location}.\n* Total Athletes Enrolled in Triathlon Pk: It has {self.participants} participants.\n* Contatc Number: {self.contact}.\n"
        triathlon1 = Triathlon("Traithlon Pk", "Short", "Multan Kantt", 1000, "+923027431995") #Object
        print(triathlon1.get_details())   #Calling Method
# Choose operation 2 containing Student class to Register Athletes for Training.
    elif operation == 2: 
            class student: #class
                print("\n<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<")
                print("<<<<  Enter the Following Data for Registeration  >>>>>")
                print(">>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>\n")
                def __init__(self, name, fname, number, cnic, age, gender, amount, disability): #Constructor & Attributes
                    self.name = name
                    self.fname = fname
                    self.number = number
                    self.cnic = cnic 
                    self.age = age
                    self.gender = gender
                    self.amount = amount
                    self.disability = disability
                def display_record(self): # Method of class 
                    print("                                                     ")
                    print("_______________________________________________")
                    print("|        Student Saved Record                ")
                    print("|Name of student = "+self.name)
                    print("|Father Name of student = "+self.fname)
                    print("|Phone Number of student = "+self.number)
                    print("|CNIC of student = "+self.cnic)
                    print("|Age of student = "+self.age)
                    print("|Gender of student = "+self.gender)
                    print("|Amount deposited by Student = "+self.amount) 
                    print("|Do you have any Disability? = "+self.disability) 
                    print("________________________________________________") 
            # Taking Input Data to Enroll Students in Triathlon PK.
            name = input("Enter Your Name: ")
            fname = input("Enter Your Father Name: ")
            number = input("Enter Your Phone Number: ")
            cnic = input("Enter Your CNIC: ")
            age = input("Age of Student: ")
            gender = input("Gender of Student: ")
            amount = input("Amount deposited by Student: ")
            disability = input("Do you have any Disability?: ")
            # File Handling for creating, opening and closing file.
            f=open(name,"w")
            f.write(" Name of customer:  " + name + ".\n")
            f.write(" Father name of customer:  " + fname + ".\n")           
            f.write(" Number: " + number + ".\n")
            f.write(" CNIC NO# " + cnic + ".\n")
            f.write(" Age of student: " + age + ".\n")
            f.write(" Gneder of Student: " + gender + ".\n" )
            f.write(" Amount deposited by Student: " + amount + ".\n" )
            f.write(" Disability of Student:  " + disability + ".\n")
            f.close()
            # Objects of Student class
            std1 = student(name, fname, number, cnic, age, gender, amount, disability)
            std1.display_record() # Calling a method
    # Choosing Operation 3 to see Trainers Profile instructing in Traithlon
    elif operation == 3:        
        class trainers: #class
            print("|    Triathlon PK Trainer Profile                 ")
            def __init__(self, name, dob, status, experience): #Constructor & Attributes
                self.name=name
                self.dob=dob
                self.status=status
                self.experience=experience
            def trainers_record(self): # Method of class
                print("_______________________________________________")
                print("|Name of Trainer = "+self.name)
                print("|Date of Birth of Trainer = "+self.dob)
                print("|Status of Trainer = "+self.status)
                print("|Experience of Trainer = "+self.experience) 
                print("________________________________________________") 
        # Objects of class
        trainer1 = trainers("Jane Robinson", "30-11-1993", "Cycling Trainer", "10 years")
        trainer2 = trainers("Brett Whitinui", "02-10-1995", "Running Trainer", "09 years")
        trainer3 = trainers("Wendy Jones", "08-06-1988", "Running Trainer", "13 years")
        # Calling methods
        trainer1.trainers_record()
        trainer2.trainers_record()
        trainer3.trainers_record()
    # Choosing Operation 4 to read records of Athletes Enrolled in Traithlon
    elif operation==4:
        class read: #class
            try:
                a=input("Enter Athlete File Name to Read: ")
                f=open(a,"r")
                print(f.read())  #Showing File
            except:
                print("File is not available") #Incase file is not available
            else:
                f.close()
                print("Thanks you")
    # Choosing Operation 5 to see Major Events of Triathlon.            
    elif operation == 5:        
        class Event: #class
            print("\n<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<")
            print("<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<            Major Events of Traithlon PK          >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>")
            print(">>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>\n")
            def __init__(self, name, location, date, participatiton): #constructors & attributes
                self.name = name
                self.location = location
                self.date = date
                self.participation = participatiton
            def event_details(self): # Method of class
                return f"* {self.name} is an event held in {self.location} on {self.date}. Athlete named {self.participation} participates in this Event."
        # Creating objects of class
        event1 = Event("Running Competition", "New York", "2023-11-05", "Aiman Shabbir")
        event2 = Event("Cycling Competition", "Los Angeles", "2023-07-15", "Alishba Shaukat")
        event3 = Event("Racing Competition", "America", "2020-12-06", "Mehvish Shareef")
        event4 = Event("Cycling Competition", "Dubai", "2019-07-11", "Shaista Parveen")
        event5 = Event("Running Competition", "Australia", "2017-08-03", "Laiba Noor")
        # Calling method of class
        print(event1.event_details())
        print(event2.event_details())
        print(event3.event_details())
        print(event4.event_details())
        print(event5.event_details())
        print("\n") #For line break
    #Choosing Operation 6 to see Results of Competitions 
    elif operation == 6:        
        class Results: #Class
            print("\n<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<")
            print("<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<              Results of Competitions               >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>")
            print(">>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>\n")
            def __init__(self, position, event, location, date): #Constructors & Attributes
                self.position = position
                self.event = event
                self.location = location
                self.date = date
            def result_details(self): # Declearing a Method of class
                return f"* Got {self.position} Position in {self.event} event held in {self.location} on {self.date}."
        # Creating Objects of Class
        result1 = Results("First (1st)", "Running Competition", "New York", "2023-11-05")
        result2 = Results("Second (2nd)", "Cycling Competition", "Los Angeles", "2023-07-15")
        result3 = Results("Third (3rd)", "Racing Competition", "America", "2020-12-06")
        result4 = Results("First (1st)", "Cycling Competition", "Dubai", "2019-07-11")
        result5 = Results("Second (2nd)", "Running Competition", "Australia", "2017-08-03")
        #Calling Method
        print(result1.result_details())
        print(result2.result_details())
        print(result3.result_details())
        print(result4.result_details())
        print(result5.result_details())
        print("\n") #For Line Break
    # Choosing Option 07 to see Training Programs, their charges and duration
    # This class is containing concept of inheritance (Parent-Child)
    # Training Program is Parent class 
    # Running Program & Cycling Program are child classes of Parent class (Training Program)
    elif operation == 7:        
        class TrainingProgram: # Parent class
            print("\n<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<")
            print("<<<<<<<<<<<<<<<<<<<<<<<<<<<         Sports Training Programs in Triathlon           >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>")
            print(">>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>\n")
            def __init__(self, program_name, program_duration): #Constructor & Attributes
                self.program_name = program_name
                self.program_duration = program_duration
            def display_program(self): # Declaring a Method
                print(f"Program name: {self.program_name}")
                print(f"Program duration: {self.program_duration} weeks")

        class RunningProgram(TrainingProgram):  # Child Class of Training Program
            def __init__(self, program_name,program_duration, program_charges, distance_perday):
                super().__init__(program_name, program_duration)
                self.program_charges = program_charges
                self.distance = distance_perday

            def display_program(self): # Declaring a Method
                super().display_program()
                print(f"Program Package: {self.program_charges} rs")
                print(f"Running distance: {self.distance} km")

        class CyclingProgram(TrainingProgram):   #Child Class of Training Program
            def __init__(self, program_name,program_duration, program_charges, duration_per_day):
                super().__init__(program_name, program_duration)
                self.program_charges = program_charges
                self.duration_per_day = duration_per_day

            def display_program(self): # Declaring a Method
                super().display_program()
                print(f"Program Package: {self.program_charges} rs")
                print(f"Cycling duration per day: {self.duration_per_day} hours")

        # create objects for running and cycling programs
        running_program = RunningProgram("Super Running Program", 10, 30000, 20)
        cycling_program = CyclingProgram("Super Cycling Program", 12, 40000, 5)

        # display program information
        running_program.display_program()
        cycling_program.display_program()

        print("\n")

    # Choosing operation 08 to give Feedback about Triathlon PK Services.
    elif operation == 8:
        class Reviews: #Class containing constructors & Attributes
            def __init__(self,name, location, environment, security, facilities, cleanliness, management, behaviour):
                self.name=name
                self.location = location
                self.environment = environment
                self.security = security
                self.facilities = facilities
                self.cleanliness = cleanliness
                self.management = management
                self.behaviour = behaviour
            # Declaring Method of Class
            def display_data(self):
                print("\n")
                print("Name of customer:",self.name)
                print("Location: ", self.location)
                print("Environment: ", self.environment)
                print("Security: ", self.security)
                print("Facilities: ", self.facilities)
                print("Cleanliness: ", self.cleanliness)
                print("Management: ", self.management)
                print("Behaviour: ", self.behaviour)
        # Taking Input from User to Record Feedback
        name=input("Enter Your Name: \n")
        location = input("Is location of Triathlon PK good or not? ")
        environment = input("How do you feel about the environment of Triathlon Pk? ")
        security = input("Is Security of Triathlon is good or not? ")
        facilities = input("Does Triathlon provides all types of facilities or not? ")
        cleanliness = input("Triathlon was clean OR not.? ")
        management= input("Is management good or not? ")
        behaviour = input("Do you like the behaviour of Triathlon faculty(Trainers & Athletes) or not? ")
        # File Handling to save feedback
        f=open("Reviwes1.txt","a")
        f.write("Name of client: \n"+ name +".\n")
        f.write("location:\n "+ location + " .\n")
        f.write("Environment:\n " + environment + " .\n")
        f.write("security:\n " + security + " .\n")
        f.write("facilities:\n " + facilities + " .\n")
        f.write("cleanliness: \n" + cleanliness + " .\n")
        f.write("management:\n " + management + " .\n")
        f.write("behaviour:\n " + behaviour + " .\n")
        f.close()
        # Creating object of class
        view = Reviews(name,location, environment, security, facilities, cleanliness, management, behaviour)
        view.display_data() # Calling a method or function
        print("\n")
     # Choosing operation 09 to see reviews of Triathlon   
    elif operation == 9:
        f=open("Reviwes1.txt","r")
        print(f.read())
    # Only Admin know this key to remove some specific records
    elif operation ==2345:
            import os
            b=input("File name: ")
            if os.path.exists(b):
                os.remove(b)
            else:
                print("This file is already removed")
    #Choosing Operaton 10 to close the Program
    elif operation ==10:
        print("Thanks for vist our site")
        break

    else:
        print("Invalid input. Please choose other option") 
      
    c=input("Press 0 to go to Main Menu:  \n")
    if c==1:
        break
    else:
        continue  
