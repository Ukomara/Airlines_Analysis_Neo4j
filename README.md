# Airlines_Analysis_Neo4j
This project aims to analyze flight delay data and its impact on passenger demand and airfares. Flight delays not only irritate air passengers but also cause a decrease in efficiency, an increase in capital costs, and additional crew expenses. Therefore, an accurate estimation of flight delay is critical for airlines to increase customer satisfaction and incomes.

### User Group and Use Cases
The primary user group for the "Airline Delays" project is airline companies. The use cases for this project are as follows:

To identify if flight delays occur more frequently on particular days of the week
To determine if some airlines are more likely than others to create delays
To examine if the trip length is a factor that prolongs delays more frequently
To identify routes that experience more delays than others

### Data
The Airlines Delay dataset is used in this project, which is available on Kaggle. The dataset contains the following attributes:
Airline
Flight ID
AirportFrom
AirportTo
DayOfWeek
Length(Duration of the flight)
Delay(yes or no)

### Challenges in data were:
The original dataset had more than 50k records, which made the network complex and challenging to derive insights from.
Loading the data into Neo4j resulted in a hairball network. To simplify the network, a subset of 1000 records was used.
To create a better network, the "From Airport" and "To Airport" attributes were combined to form a route of the flight.
A new attribute "Source-Destination" was created by concatenating "AirportFrom" and "AirportTo" attributes for all records.
Identifying a useful relationship "AIRLINE_TRAVELLING" with meaningful properties led to a simpler network.


In conclusion, the Airlines Analysis Project with Neo4j provides valuable insights into flight delays, which can help airlines improve customer satisfaction and incomes.Future suggestions for this project could include analyzing additional datasets such as weather and traffic data to identify potential factors contributing to flight delays. Additionally, exploring the impact of delays on airline revenue and customer satisfaction could provide further insights for airline companies to improve their services.
