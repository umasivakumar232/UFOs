# UFO Sightings 

![180103-ufo-illustration-mn-1015](https://user-images.githubusercontent.com/85518330/146302833-775b6cab-17ff-46af-a7c5-3eb022069566.jpg)

## Project Overview

In this module we learn to use JavaScript to build a dynamic web page. A dynamic web page accepts user inputs to adjust what is displayed on the screen. Here we used UFO sighting data as an example and built a table to neatly display all the sighting data, we created filters that let our users refine their search. We used HTML to display our web page and used CSS and Bootstrap elements to help style our page 

## Results 

The steps  we followed to build this webpage are as under 

We download the  Data.js which contains the UFO sighting data as an array. We notice that in a JavaScript array, it's not a single item but a recording of an  entire event: date, location, type, and even comments are saved inside a single array
     
<img width="402" alt="Array" src="https://user-images.githubusercontent.com/85518330/131188675-3e56ec72-d273-4baf-8e19-8b898388c521.png">

### Create a Table

We convert the array into a table  - we declare a variable called tableData, we reference the tbody HTML tag using D3. _D3 is a JavaScript library that produces sophisticated and highly dynamic graphics in an HTML webpage_. We create a function **buildTable** and pass in **data** as the argument. We apply a **forEach** function that loops through our data array, and then adds rows of data to the table. We also add an argument **dataRow** that will represent each row of the data as we iterate through the array. We create a variable that will append a row to the table body. we'll add code to loop through each field in the dataRow argument. These fields will become table data and will be wrapped in <td> tags when they're appended to the HTML table

<img width="460" alt="Table code" src="https://user-images.githubusercontent.com/85518330/131189578-3d0f3a5d-5e5d-4606-92b8-6989c2202339.png">
   
<img width="510" alt="Table" src="https://user-images.githubusercontent.com/85518330/131189788-a2897083-bf18-4909-91c8-952ee4dd7a5e.png">
 
### Create Filters to Search Table   
   
First we need to add the search parameters to our **index.html** page. The search parameters are organized as list elements. each list has a **label** and an **input element**, each input element has an **id** and **placeholder**. The id is the property of each element in the dataset 

 <img width="456" alt="Filter_search" src="https://user-images.githubusercontent.com/85518330/131189525-87e84e80-68a1-4ba4-85a4-2fe38181ed18.png">

Next we write code to store all the ids and values that have changed. We create a variable that selects all elements with have changed. This will initialize an array that stores value and id. Next we create a variable that holds the value of the property that has changed

<img width="439" alt="updateFilters" src="https://user-images.githubusercontent.com/85518330/131190127-429c5e4b-2b00-4a44-85f4-699615616160.png">

We use an *if* , *else* statement to check if a value was entered in the filters, if yes, we store the filter element and id of that filter object, if not we clear that filter from our filter object

<img width="478" alt="if_elseif" src="https://user-images.githubusercontent.com/85518330/131190188-ebd1323e-5da8-41a4-ab52-f4f798f219ec.png">

We call on the updateTable function which loops through the filters object and for each key and value that is stored and will filter the table based on the search parameters.

<img width="479" alt="Key_value" src="https://user-images.githubusercontent.com/85518330/131192407-0c06998e-5a9f-4320-aa3f-8d99a9a00b68.png">

We create an *Event listener* as shown below that detects what inputs have changed on HTML page and when changed they call on the updateTable funtion to reflect those changes in the table

<img width="406" alt="eventListerner" src="https://user-images.githubusercontent.com/85518330/131192548-ef29bb4c-2aa0-4d14-9901-8484b335c20e.png">

We finally use CSS, Bootstrap and Jumbotron elements to beautify our webpage by adding the relevant fonts, background colours, images etc. 

The end result of our efforts is a web page that responds nicely to filter the table as per user request

### Unfiltered Table   

<img width="953" alt="Unfiltered table" src="https://user-images.githubusercontent.com/85518330/131190863-e714d249-5290-4dd2-bed3-bc2281526404.png">
   
### Filtered on Date and Shape

<img width="956" alt="Date   shape" src="https://user-images.githubusercontent.com/85518330/131190994-a4a81e4a-744c-40e1-84d7-4e569d51b745.png">

### Filtered on State
   
<img width="926" alt="state" src="https://user-images.githubusercontent.com/85518330/131191052-0fcee473-28d4-48a2-978b-0fd153ee477d.png">


## Summary
 
Our finished UFO webpage looks nice and polished, the filters also work as intended and filter the table to display results, however a second look at the page and we feel that one drawback of the current page is that it doesnt automatically reset the page when one search is completed. We need to manually reload the webpage for the table to reset. In the 2nd phase of development of this page we should look at the below additional functionality 

* A reset button - At the end of the filters to clear all filters and reset the table 

* Dropdowns - It will help users if they can have dropdowns to select the cities, states , countries or shapes. This will help users use the correct spellings and limit the search to what is available in the given table. 

