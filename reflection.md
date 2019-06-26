# Reflection

## Web App From Scratch

Web app from scratch was all about creating structures, fetching and gathering data en sorting and filtering the data. My take on this during the 'Meesterproef' was to create a solid foundation with Typescript and write mostly class based components. This way I always know what outcome would be expected and write classes gives a great structure to the server.

The class based components were not really that difficult to implement as I had experience with it, but the value it gives is very nice. For me, it gives a foundation for an expandable application.

Typescript on the other hand was somewhat more difficult to implement, declaring types and interfaces in general was not the hardest part, but due to (still after many times rewriting the data modal) I had to change my data structure often. This means that there would be many declarations changing often. This wouldn't be a main problem as it is the way Typescript works and it will benefit you in the end. But I struggled with the fact that MongoDB and Graphql have many functions that they provide and I can't type beforehand.

Afterall in the lastweek I found out that there were types for graphql and mongoose which should fix these, so it can be fixed but my lack of knowledge gave me a hard time.

## CSS To The Rescue

For CSS to the Rescue we used coding structures like BEM and SCSS. I didn't work that much on the front-end but we vouched for these standards by the three of us. These structures gave us coding and naming standards which resulted in fast debugging and developing throuhgout the project.

We all worked with BEM and SCSS before, but not really in team composition. So this was a great test of how useful it can be. And it turned out to be very useful, since we have a standard coding style throughout the whole application. Overall I'm happy with how it turned out.

## Browser Technologies

For Browser Tech it was a goal of mine to have offline support for when people would drive through a tunnel or would be in areas with no internet connection. It was meant as a nice to have at start, but at the end of the project we did have time to implement a Progressive Web Application with offline support. This meant that the user could load any page that he visited before and got a nice message when he reached a phase or page that required internet connection.

For me this is quite important as it provides users with meaningful feedback and doesn't leave the user guessing when the internet connections dissappears.

The implementation of this went quite smooth, we added zero-states for data depending components to provide information when the page is offline and the other pages that have been visited will be served from the cache.

We wanted to implement caching for the post requests to graphql but this would require BrowserSync, unfortunately this was not possible but would have been a very great asset. As our app would be completely usable offline.

## Web design

For webdesign I ran usability test over the application and it turned out that there was a small lack of semantics. The tabindex didn't gave much feedback and click events would sometimes be put on divs. To fix this I changed every item that could be clicked to buttons and created a outline based on our themecolors when you use the tab now.

I also tested on color blindness and contrast ratio's. The color blindness was no problem for our application, but the contrast ratio was .5 off, so I changed this and it did meet de double A standards now.

We have a large target audience, so it is important to atleast have the basic conventions right and that the application can be accessed by people with bad eyesight or any other restrictions.

## Performance Matters

For performance matters I used GraphQL which is known for being a better perfomer that REST API does. However REST calls are more reliable, based on performance GraphQL wins.

The reason I chose for GraphQL is that you can find deepnested items and return only the necessary items. Comparing this to REST, you would return a complete endpoint or an id with all of its data. This would mean longer calls and more unused data that moves around the server.

I would have liked to implement more server optimalisations, but as this was already quite fast I focussed more on the client side at the end of the project and fixed some low hanging fruit that improved the overall performance. As the client is being rendered server side, the performance already was great but based on Lighthouse I fixed some small points that were giving errors.

## Real-Time Web

In the application I provided a real time connection between the server and the client. Our app was pretty straight forward and lacked some flair, so with the implementation of sockets on the client and server, we could send events around and take actions based on the events.

I found it very nice to work with, also the implementation went quite smooth which is 50% of the developer experience. It was nice to see that we could now emit events when you update a status or create an issue in the app. Stakeholders in the dashboard would be notified when a new issue appeared and when the issue status changed, the user would be notified.

This kind of interaction really gives a lot more meaning to your application and I am very happy that we could implement it inside our app.
