# solid
This program is for taking orders with name of item, quantity, and their price
and then displaying the total price of the order.

The abstract methods are used for authorization and payment processing

I have used different payment methods such as debit, credit and paypal.

There are two types of authorization SMS authorization and to check if you are a robot

authorizer = NotARobot() or SMSAuth()

processor = DebitPaymentProcessor("",authorizer) or CreditPaymentProcessor("",authorizer) or PaypalPaymentProcessor("",authorizer)   the first input is any code (letters & numbers)

authorizer.not_a_robot() or authorizer.verify_code(1276527)</br>   
First option should be given when authorizer has input as NotARobot() and second for SMSAuth() and Only SMSAuth() requires a code</br>
