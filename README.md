# Data-Types-
int_or_str_values = {}
list_values = {}
dict_values = {}
input_ = [] 

# In this class you can print values
class console:
    def log(*args): # In this function I used the javascript log function that prints values in python
        if args in dict_: # check if args in dict_
            char = dict_[args] # if in the dictionary it gets value and prints it
            if char != None:
                print(str(char))
        else:
            print(args)
        
    
    def read_input(value):
        if value in dict_:
            char = dict_[value]
            if char != None:
                print(char)
        else:
            print("[ ]")
    

def input_(*args): # in this function you can prompt 
    for char in args:
        all_char = char
    
    input_value = input(all_char)
    return input_value

class Int_Str: # In this function you can make str and int vars
    def make(int_str_name,*args):# to make vars of str and int
        if int_str_name in int_or_str_dict:
            int_or_str_dict[int_str_name] = args
        else:
            int_str = int_or_str_dict[int_str_name] = args
            return int_str

    def log(*args): # to print vars
        new_list = [*args[:len(args) + 1]]
        element = " ".join(new_list)
        try:
            print(int_or_str_dict[element])
        except:
            print("You cause an error in Int_Str.log")
    


class List: # In this class you can make your own list
    def make(name,*args) -> list: # to make list
        if the name in list_values: #check if the list name is declared 
            print(f"The {name} is created")
        else: # If not it creates a new once
            new_list = args 
            list_values[name] = new_list
            list(new_list)
            return new_list,list_values
    
    def append(list_name,*args): # to append values to list
        if list_name in list_values:
            if len(args) > 1:
                arg = [* args [:len(args) + 1]]

                element = " ".join(arg)
    
                list_value = list(list_values[list_name])

                new_list = list(list_values[list_name])

                new_list.append(element)
                list_values[list_name] = new_list
                new_list = [* args [:len(args) + 1]]
                add_two_list = list_value + new_list
                list_values[list_name] = add_two_list
                return add_two_list

            else:
                new_list = [*args[:len(args) + 1]]
                element = " ".join(new_list)
                list_ = list(list_values[list_name])
                list(list_)
                list_.append(element)
                list_values[list_name] = list_
                return list_
        else:
            print("Please make a variable to append values")

    def clear(list_name): # to clear list
        try :
            if list_name in list_values:
                list_value = list(list_values[list_name])
                clear_list = list.clear(list_value)
                clear_list = [ ]
                list_values[list_name] = clear_list
                return clear_list
            else:
                print("This list name does not exist")
        except:
            print("You have mistakes in List.clear")

        
    def index(name,index : int) -> int : # to do indexing
        if name in list_values:
            value = list_values[name]
            print(value[number])
        else:
            print("This list does not exist")
    
    def log(name):  # Added `self` parameter for class method
        if name in list_values:  # Accessing the class attribute
            value = list_values[name]
            print(value)  # Print the list directly
        else:
            print("[ ]")  # Handle case where list doesn't exist
        
    
    def delete(list_name,index = None) -> int:
        value = list(list_values[list_name])
        if index == None:
            index = len(value) - 1
            value.pop(index)
            list_values[list_name] = value
        else:
            value.pop(index)
            list_values[list_name] = value

class Dict: # Dict class like List
    def make(dict_name,key,value): # to make dict
        if dict_name in dict_values:
            print(" * ")
        else:
            inner_dict = {key:value}
            dict_values[dict_name] = inner_dict
            return inner_dict
    
    def log(dict_name,*key): # to print dictionary values
        if bool(key):
            arg = [*key[:len(key) + 1]]
            new_arg = " ".join(arg)
            str(new_arg)
            if dict_values[dict_name][new_arg] != None:
                print(dict_values[dict_name][new_arg])
            else:
                print(f"This name {name} dictionary does not exist")
        else:
            if dict_values[dict_name] != None:
                print(dict_values[dict_name])
            else:
                print(f"This name {name} dictionary does not exist")
    
    def clear(dict_name): # to clear dict
        try: 
            if dict_name in dict_values:
                clear_dict = dictionary(dict_values[dict_name])
                clear_dict.clear()
                dict_values[dict_name] = clear_dict
                print(clear_dict)
            else:
                print("This list name does not exist")
        except:
            print("You have mistakes in Dict.clear")
