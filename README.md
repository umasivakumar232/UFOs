# UFO Sightings 

## Project Overview

In this module we have learnt to use JavaScript to build a dynamic web page. A dynamic web page accepts user inputs to adjust what is displayed on the screen. Here we have used UFO sighting data as an example and built a table to neatly display all the sighting data we want to work with and then created filters that let our users refine their search based on their requirements. We used HTML to display our web page and used CSS and Bootstrap elements to help style our page 

## Results 

The steps followed by us to build this webpage are as under 

    * In step 1 we download the  Data.js which contains the UFO sighting data as an array. We notice that in a JavaScript array, it's not a single item but a recording of an entire event: date, location, type, and even comments are saved inside a single array
     
    * Next we convert the array into a table  - we declare a variable called tableData, We want the data to be  displayed in a table, so we reference the tbody HTML tag using D3. *D3 is a JavaScript library that produces sophisticated and highly dynamic graphics in an HTML webpage*. We create a function "buildTable" and pass in "data" as the argument. We apply a **forEach** function that loops through our data array, and then adds rows of data to the table. We also add an argument (dataRow) that will represent each row of the data as we iterate through the array. We create a variable that will append a row to the table body. we'll add code to loop through each field in the dataRow argument. These fields will become table data and will be wrapped in <td> tags when they're appended to the HTML table


    * In the next step we  add **filters search** to the table so that we can search the data using different fields (date, city, state, country and shape). When user enters search criteria the java script code stores the value in the text box and the id's associated with the text box in a java script object.    

     * Create a variable to keep track of the all the filters 
         
         *var filters ={};

    * Create a function to update the filters      

         * function updateFilters() {

    * Before the code to capture the values and id's , we need to add the search parameters to our *index.html* page. The search parameters are organized as list elements. each list has a *label* and an *input element*, each input element has a *id* and *placeholder*. The id is the property of each element in the dataset 

    * Next we write code to store all the ids and values that have changed. We create a variable that selects all elements with have changed. This will initialize an array that stores value and id. Next we create a variable that holds the value of the property that has changed

    * We use an *if* , *else* statement to check if a value was entered in the filters, if yes, we store the filter element and id of that filter object, if not we clear that filter from our filter object

    * Finally we call on the updateTable function which loops through the filters object and for each key and value that is stored and will filter the table based on the search parameters.

    * We create an *Event listener* as shown below that detects what inputs have changed on HTML page and when changed they call on the updateTable funtion to reflect those changes in the table

    * We finally use CSS, Bootstrap and Jumbotron elements to beautify our webpage by adding the relevant fonts, background colours, images etc. 


## Summary
 
    * Our finished UFO webpage looks nice and polished, the filters also work as intended and filter the table to display results, however a second look at the page and we feel that in the 2nd phase of development of this page we should look at the below functionality a little more 

    * A reset button - In the current page once we finish our search the whole webpage needs to be reset for the entire table to appear again. A rest button or a clear filters button may be helpful 

    * Dropdowns - It will help users if they can have dropdowns to select the cities, states , countries or shapes. This will help users use the correct spellings and limit the search to what is available in the given table. 

