Inspiration
Our inspiration came from how we are all relatively new drivers and terrified of busy intersections. Although speed is extremely important to transport from one spot to another, safety should always be highlighted when it comes to the road because car accidents are the number one cause of death in the world.

What it does

When the website is first opened, the user is able to see the map with many markers indicating the fact that a fatal collision happened here. As noted in the top legend, the colours represent the different types of collision frequency. When the user specifies an address for the starting and ending location, our algorithm will detect the safest route in order to avoid all potentially dangerous/busy intersections. However, if the route must pass a dangerous intersection, our algorithm will ultimately return it back.

How we built it

For the backend, we used Javascript functions that took in the latitude and longitude of collisions in order to mark them on the Google Map API. We also had several functions to not only check if the user's path would come across a collision, but also check alternatives in which the user would avoid that intersection.

We were able to find an Excel spreadsheet listing all Toronto's fatal collisions in the past 5 years and copied that into a SQL database. That was then connected to Google SQL to be used as a public host and then using Node.js, data was then taken from it to mark the specified collisions.

For the frontend, we also used a mix of HTML, CSS, Javascript and Node.js to serve the web app to the user. Once the request is made for the specific two locations, Express will read the .JSON file and send information back to other Javascript files in order to display the most optimal and safest path using the Google Map API.

To host the website, a domain registered on Domain.com and launched by creating a simple engine virtual machine on Compute Engine. After creating a Linux machine, a basic Node.js server was set up and the domain was then connected to Google Cloud DNS. After verifying that we did own our domain via DNS record, a bucket containing all the files was stored on Google Cloud and set to be publicly accessible.

Challenges we ran into

We have all never used Javascript and Google Cloud services before, so challenges that kept arising was our unfamiliarity with new functions (Eg. callback). In addition, it was difficult to set up and host Domain.com since we were new to web hosting. Lastly, Google Cloud was challenging since we were mainly using it to combine all aspects of the project together.

Accomplishments that We're proud of

We're very proud of our final product. Although we were very new to Javascript, Google Cloud Services, and APIs, my team is extremely proud of utilizing all resources provided at the hackathon. We searched the web, as well as asked mentors for assistance. It was our determination and great time management that pushed us to ultimately finish the project.

What we learned

We learned about Javascript, Google APIs, and Google Cloud services. We were also introduced to many helpful tutorials (through videos, and online written tutorials). We also learned how to deploy it to a domain in order for worldwide users to access it.

What's next for SafeLane

Currently, our algorithm will return the most optimal path avoiding all dangerous intersections. However, there may be cases where the amount of travel time needed could be tremendously more than the quickest path. We hope to only show paths that have a maximum 20-30% more travel time than the fastest path. The user will be given multiple options for paths they may take. If the user chooses a path with a potentially dangerous intersection, we will issue out a warning stating all areas of danger.

We also believe that SafeLane can definitely be expanded to first all of Ontario, and then eventually on a national/international scale. SafeLane can also be used by government/police departments to observe all common collision areas and investigate how to make the roads safer.
 
