# nubibus

@startuml
User  --> Customer
Customer --> Agreement
Customer  --> Document
Customer  --> Communication
Customer  --> Transaction

(User,Customer).. Role

User  --> Account
Account --> Agreement
Account  --> Document
Account  --> Communication
Account  --> Transaction

Customer -> Account


Agreement --> Policy
Policy --> Coverage
Policy --> Party
Policy --> InsurableObject

(Policy,Party) .. PolicyRole

Role .. (User,Account)
@enduml
