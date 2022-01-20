# Python Live Project
## Introduction
During my first live project in my boot camp, I created an interactive website using the Django framework. The topic I chose was "New York City Restaurants", as I live in Brooklyn and wanted to be able to put my passion for the incredible food scene to use in creating this site. To give the students a chance to understand how a real-world environment would feel like, we utilized Agile/Scrum Methodology. We had a sprint planning meeting, daily stand-ups, and code retrospectives at the end of each week. We were assigned stories  based on what task needed to be accomplished and learned how to succesfully merge into the master through Git. Throughout the project, I utilized my knowledge of Python, HTML, CSS, Javascript, and SQL. 

## CRUD Functionality
* **Create:** For my website, I created a model that contained information about New York City restaurants, including the name, borough, neighborhood, price range, and address. 

* **Read:** On my website, I wanted users to be able to see all the restaurants I had added to the database and then be able to click into them to view details. Below, you can see how that operates. [Click here to see the code.](#read) 

* **Update and Delete:** Users could also go into the details of the restaurant and update or delete the entry in the database. [You can see the code snippet here.](#update-and-delete)


### Read

Code below was put in views.py. The first function displays all the restaurants. The second function displays all the information on the restaurant on a separate page in a table.

      def all_rest(request):
  
        every_rest= Restaurants.Restaurants.all()

        context= {'every_rest': every_rest}

        return render(request, 'NYC_Guide/all_rest.html', context)
      
      

      def details(request, restaurants_id):
  
        rest_request= get_object_or_404(Restaurants, pk=restaurants_id)

        context= {'rest_request': rest_request}

        return render(request, 'NYC_Guide/details.html', context)
      

### Update and Delete
