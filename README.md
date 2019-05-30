# invoice-challenge

I was tasked with creating a simple frontend application which would make an API call to retrieve items and allow a user to select from thos items to create and invoice. I used Bootstrap as well as jQuery/AJAX javascript libraries.

Since this is a frontend application no setup is required and you can simply open index.html with a web browser, I tested in Chrome.

Upon page load an AJAX function is triggered to retrieve the items from the given endpoint and then displayed in a table. These items are clickable which will the populate an "Invoice" table where information is displayed as well as quantity selected. There is a memo field above the table per the requirements as well as a Total which displays the total in dollar amounts for all items added to the invoice.

Upon clicking submit, the invoice items are sent to an AJAX POST request and the invoice is created. Depending on the status of this call the UI will display either success or an error message.

I am storing the returned items in an array to access later when building the AJAX POST and also create a simple cart object to help with keeping track of which items have been selected for the invoice. This is used both to populate the invoice table/keep track of quantity as well as cross-reference the array containing all items from the initial GET request so I can easily access any necessary information (i.e. price, details, id, etc)

There is addmittedly a bit of nasty jQuery magic used to access and update the quantity of items on the invoice table as well as building HTML strings to append to the table in order to populate the invoice.



