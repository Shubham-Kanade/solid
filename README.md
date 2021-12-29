# solid
This program is for taking orders with name of item, quantity, and their price
and then displaying the total price of the order.

The abstract methods are used for authorization and payment processing

I have used different payment methods such as debit, credit and paypal.

There are two types of authorization SMS authorization and to check if you are a robot

authorizer = NotARobot() or </br>
authorizer = SMSAuth()

processor = DebitPaymentProcessor("",authorizer) or </br>
processor = CreditPaymentProcessor("",authorizer) or </br>
processor = PaypalPaymentProcessor("",authorizer)   </br>
the first input is any code (letters & numbers)

authorizer.not_a_robot() or </br>
authorizer.verify_code(1276527)</br>   
First option should be given when authorizer has input as NotARobot() and second for SMSAuth() and Only SMSAuth() requires a code</br>



Single Responsibility:
The Payment and Authorization Classes are kept different from Orders Class.</br>

Open/Closed Principle:
New Payment Methods and Authorization Methods can be added using the Authorizer and PaymentProcessor abstract classes.</br>

Liskov Substitution:
Different payment methods can have different requirements i.e. emails or security code as needed</br>

Interface Segragation Principle:
Different Payment methods can have or not have Authorization as needed.</br>

Dependency Inversion:
Different Payment methods can have different types of Authorization.</br>
