#Jayvee N Mapote
#Activity 3
#A11
def ending():
    exit()
def InputNum():
    
    num = [int(input('Enter a Number: ')) for i in range(10)]
    a = sorted(num)                                     
    b = sorted(num, reverse=True)
    c = sum(num)/len(num)
    d = max(num)
    e = min(num)
    print('\nInput Order: %s\nAscending Order: %s\nDescending Order: %s\nAverage: %s\nHighest: %s\nLowest: %s' 
    %(str(num),str(a),str(b),str(c),str(d),str(e)))
    
def Input_order():
    string_input = []
    def ending():
        exit()
    def add_list_string():
        user_string = input("enter your string to append the it in list: ")
        string_input.append(user_string)
        print("\nnow your string is")
        print(string_input)
    def insert_at_position():
        user_index = int(input("enter your location to insert string: "))
        value = input("enter your string: ")
        string_input.insert(user_index-1,value)
        print("now your string is")
        print(string_input)
    def remove_string():
        item = input("which string you want to remove: ")
        string_input.remove(item)
        print("now your string is")
        print(string_input)

    for i in range(5):
        user = input("Please enter 5 string: ")
        
        if len(user) > 1:
            string_input.append(user)
        else:
            print("please enter string with more than one letter")
            ending()
    b = sorted(string_input)                                     
    c = sorted(string_input, reverse = True)
    print('\nInput Order: %s\nAlphabetical order: %s\nReverse order: %s' %(str(string_input),str(b),str(c)))

    while True:
        print(
            "\n\n1. for append string and print\n" +
            "2. for insert at particular position and print\n" +
            "3. for remove string and print\n" +
            "Type [End] to quit\n")

        selection = input("Enter Selection: ")
        
        print()
    #The selection from the program
        {"1":add_list_string,
        "2":insert_at_position,
        "3":remove_string,
        "End":ending
        }[selection]()

while True:
    print(
          "1. Input_Number\n" +
          "2. Input_String\n" +
          "Type [End] to quit\n")
    selection = input("Enter Selection: ")
    
#The selection from the program
    {"1":InputNum,
     "2":Input_order,
     "End":ending
    }[selection]()