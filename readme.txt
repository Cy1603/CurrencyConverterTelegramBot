README.txt

Muthu Currency Converter v1.0.0
From Group: CurrentCyAlerterBoT
=======================


What Is This?
-------------
Two main functions

1. Convert currency with SGD base and then a calculator will appear to help user's do 
   simple multiplication with the rates and the amount of money they need to exchange.
2. Compare the rates from yesterday and last week's rate. Giving a percentage change.
   After comparison, the bot will ask the user if they want to be notified of the rates     
   for the same currency in 24 hours.


Features of the bot
-----------------------
1. It has inline keyboards for the all the inputs it asks for (except /start)
   This is to make sure that the user pass the correct input to the bot thus 
   we don't have to validate every single possible input that the user may possibly 
   give. Hence it is less prone to bugs and crashes due to missing input validation.

2. The alert functions automatically gets the currency rate for the users base on the  
   country the user previously selected. This saves the trouble and time for the user to 
   go through the steps again. Although out bot is very user-friendly but this still saves 
   time, and could even save the bot from overloading in a case when too many people are 
   using the bot as it reduces the usage from repeat users.

How To Use The BOT
-----------------------

1. Go to the bot on telegram via this link https://t.me/MuthuCurrencybot

2. Press start to start the bot, and start using the bot by typing or pressing /start

3. Follow the instructions and flow chart from the report to get a bigger picture of the 
   bot



What makes the bot 
--------------------------

1. The bot gets its rate from "fixer.io"

2. "Fixer.io" is a free JSON API(Application Programming interface) for current and 
   historical foreign exchange rates published by the European Central Bank. It updates 
   once daily at 11pm +8GMT. The source code is from 
   https://github.com/hakanensari/fixer-io.

3. Therefore the "requests" library is needed to get data from http://api.fixer.io/. 
   Requests save us the trouble to manually add query strings to URLs, thus we are able to 
   get data from the api more easily. 

4. "Json"(Javascript Object notation) is a lightweight data interchange format. So it
   changes the data format retrieved from fixer.io to a Python object hence enabling us to   
   extract the specific data that we need.

5. The bot also uses "Telepot" which helps build applications for Telegram Bot API. It is 
   essentially a wrapper for us to use the API from telegram. Source code referenced from 
   http://telepot.readthedocs.io/en/latest/

6. The bot requires another library called "schedule" which provides us with the function 
   to schedule the bot to call a function after a set interval, which ultimately allow us 
   to help users remind them of the updated rates.Source code referenced from 
   https://pypi.python.org/pypi/schedule

7."Datetime" module is used to retreive the unix time so that we can make use of the 
   fixer.io's existing function to retreive data from previous days (whichever days we 
   want) rather than retrieving and storing the data in a database everyday manually by  
   ourselves. 

8. The bot is hosted on heroku(https://www.heroku.com/), a cloud server application. Since it 
   is a free and easy to use platform.
9. Lastly, we used the time module so that we can use the function time(). which is much 
   more accurate than the unix equivalent. We used the time function to keep bot awake and 
   reusable. 

