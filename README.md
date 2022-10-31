# cs361-microservice
# Written by Christopher Irwin
This is a microservice that receives the labor and material cost of making a product and the desired retail markup. The microservice then calculates and returns the retail price to the requesting client.

Client Request:
1. The client saves their product information as a JSON formatted string.The variables in PascalCase are customizable by client:

   {"ProductName": [{"materials": {"MaterialName": "MaterialCost", "MaterialName": "MaterialCost"}}, {"labor": {"NumberOfHours": "HourlyRate"}}, {"percent_markup": "MarkupAsFloatOrInteger"}]}
   
2. The client then writes to a text file called "acctnotif.txt". The first line will say "calculate" and the second line will be the JSON formatted string.

3. The client then sleeps for about 0.5 seconds.

   An example call would look like this:  
       
   calculate  
   {"Artisanal Clay Pot": [{"materials": {"Clay": "20", "Paints": "15"}}, {"labor": {"4": "20"}}, {"percent_markup": "50"}]}

Client Retrieval:
1. The client reads from "acctnotif.txt". The first line will be a string representing the retail price as a float.

2. The client formats the string to match the required currency and prints the value for the user of their software.

   An example response would look like this:
   
   172.5

<p>
    <img src="/assets/images/Diagram.jpg" width="1000" height="400" />
</p>
