# Bank-Account-
class BankAccount: #Creating a clas
    def __init__(self, holder_name, account_number, balance=0): #construction 
        self.holder_name = holder_name #assigning
        self.account_number = account_number  # assigning
        self.balance = balance
    
    def withdraw(self, amount): # create a function of amount to store balance
        if amount > self.balance:
            print("Insufficient balance")
        else:
            self.balance -= amount
            print(f"Withdrawn: ${amount}")
    
    def deposit(self, amount):
        self.balance += amount
        print(f"Deposited: ${amount}")
    
    def get_balance(self):
        print(f"Account Balance: ${self.balance}")
      
account = BankAccount("John Smith", "123456789", 1000.00)
account.get_balance() # Account Balance: $1000.0
account.deposit(500.00) # Deposited: $500.0
account.get_balance() # Account Balance: $1500.0
account.withdraw(200.00) # Withdrawn: $200.0
account.get_balance() # Account Balance: $1300.0
account.withdraw(1500.00) # Insufficient balance
account.get_balance() # Account Balance: $1300.0
