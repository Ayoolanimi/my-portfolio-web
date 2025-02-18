---
title: Bank System Simulation
slug: bank-simulation-simulation
date: '2024-01-05'
excerpt: ''
featuredImage:
  url: /images/Screenshot 2025-02-05 202125.png
  altText: Case study 1
  styles:
    self:
      borderRadius: large
  type: ImageBlock
bottomSections:
  - title: Divider
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-7
          - pl-7
          - pb-7
          - pr-7
    type: DividerSection
  - items:
      - title: Created by Olalekan Oseni
        tagline: ''
        subtitle: >-
          A dynamic junior data scientist and analyst with over 3 years of
          experience working with tools such as Python, SQL, MS Excel, Power BI,
          and Tableau, along with libraries like Pandas, NumPy, Scikit-Learn,
          Matplotlib, and Seaborn. This blog provides an overview of a project I
          worked on, including the code and key details.
        image:
          url: /images/Screenshot 2025-02-05 193005-Photoroom.png
          altText: Company logo
          styles:
            self:
              margin:
                - ml-3
          type: ImageBlock
        colors: bg-light-fg-dark
        styles:
          self:
            padding:
              - pt-6
              - pl-6
              - pb-6
              - pr-6
            textAlign: left
            borderColor: border-neutralAlt
            borderStyle: none
            borderWidth: 0
            borderRadius: none
            flexDirection: row
        type: FeaturedItem
    variant: small-list
    colors: bg-light-fg-dark
    styles:
      self:
        margin:
          - mb-20
        padding:
          - pt-0
          - pl-0
          - pb-0
          - pr-0
        justifyContent: center
      subtitle:
        textAlign: center
    type: FeaturedItemsSection
isFeatured: true
colors: bg-light-fg-dark
styles:
  self:
    padding:
      - pt-5
      - pl-5
      - pb-5
      - pr-5
    textAlign: center
    borderColor: border-light
    borderStyle: none
    borderWidth: 0
    borderRadius: none
    flexDirection: col
type: PostLayout
author: content/data/gbp-vs-usd-ml-project.json
---
**SUMMARY**

The Bank System class simulates basic banking functions, including deposit, withdrawal, and balance inquiry. It initializes with a default balance of $10,000 and prompts the user to select an action. Deposits update the balance, while withdrawals check if sufficient funds are available, offering an overdraft option if needed. The program runs by creating an instance of Bank System and calling the greetings method, providing a simple console-based banking interface with input validation.

**LINES OF CODE**

```
# creating a class for the BankSystem functions
class BankSystem():
    def __init__(self):
        self.balance = 10000    # initializing the default balance belonging to the user

    def greetings(self):    #  initiate the greetings' function interface to determine the action user would like to perform
        self.welcome = input("Welcome, what action would you like to perform? Deposit, Withdrawal, Check Balance: ").lower()
        if self.welcome == "deposit":
            self.user_deps = int(input("Enter the amount you would like to deposit: "))                    self.deposit()
        elif self.welcome == "withdrawal":
            self.user_with = int(input("Enter the amount you would like to withdraw: "))                  self.withdraw()
        elif self.welcome == "check balance":
            print("Your account balance is", self.balance)
        else:
            print("Invalid input. Please try again.")

    def deposit(self):  # initiate the deposit function to comprehend the user's deposit actions
        self.balance += self.user_deps
        new_bal = ('Deposit Successful!! Your account balance is now ${}'.format(self.balance))
        print(new_bal)

    def withdraw(self): # initiate the withdrawal function to comprehend the user's deposit actions
        if self.user_with > self.balance:
            self.user_over = input('You do not have sufficient balance \nWould you like to request an overdraft? yes/no \n').lower()
            if self.user_over == 'yes':
                print('Your request is being reviewed. You will be contacted via email')
            else:
                print('Please try again later')
        else:
            self.balance -= self.user_with
            new_bal2 = ('Withdrawal Successful!! Your account balance is now ${}'.format(self.balance))
            print(new_bal2)

bank = BankSystem()
bank.greetings()
```



**MEDIA**

****![](/images/Screenshot%202025-02-05%20202125.png)
