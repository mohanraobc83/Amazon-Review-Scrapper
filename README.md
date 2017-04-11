# Amazon-Review-Scrapper
A Python code to extract ratings and reviews from Amazon

This code was developed on Spyder with in Anaconda using Python 3.6.0

The objective is to extract the following details from the Amazon Review web pages for a list of products
   - Review Date
   - URL Page
   - Review Title
   - Author
   - Rating
   - Review Text
   - Information on how many people found the review helpfull

The required input file is the list of URLs for the first review page of all the required products under scope in an excel format
The format of the input file is attached for reference. These URL list needs to prepared before running the code

Issues to lookout for?

The request call to Amazon might fail with various HTTP response code. This program handles the failures with 503 response. If there are other response codes, then the code needs to be modified to handle such errors. Amazon does not like people loading their infrastructure with such data scapping requests and they keep developing firewalls and other protection algorithms to avoid such programs. So, for all practical purposes, this code is expected work well for small number of products. But if the number of products under scope is large (say 100), the code might not work and you might get session timeout errors or 503 errors. This is Amazon asking you to stop loading their infrastructure with such requests.

The possible solution to overcome this hurdle is to have revolving IP setting to run the code (i did not try this, but saw such solutions proposed on the internet) or a better solution is to use Salenium web driver to open the links in web browser and then pars the source HTML page using beautiful soup with in python. This method works because with salenium you are making the call with the browser, which is legit and Amazon will not block the call as you are actually emulating a user accessing the web page using a browser. 

Please mail me at mohanraobc@gmail.com for any questions, conerns, comments or suggestions to improve the code

This code will not work if the HTML design of Amazon pages changes


