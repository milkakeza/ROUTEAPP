1.Project Preview
ROUTEAPP is designed to help users get directions from their current location to a specified destination without manually entering their starting point. It is particularly useful for tourists and locals unfamiliar with specific routes. In Rwanda, many bike riders may not know how to use Google Maps, leading to potential issues when guiding them. Additionally, if passengers are unaware of the route, bike riders may double the cost of transport. By using ROUTEAPP, users can guide bike riders or share the route with a contact who can help negotiate a fair price, ensuring an efficient and cost-effective journey.

2.Key Features
.Automatic Geolocation: Determines the user’s current location automatically.
.Destination Routing: Provides step-by-step directions from the user’s location to their destination.
.Error Handling: Alerts users if the entered destination cannot be found.
.Route Sharing: Users can share routes with emergency contacts for guidance or fare negotiation through a private link.

3.APIs used
.Geolocation API: Detects the user’s current location automatically. (https://developers.google.com/maps/documentation/geolocation/overview)
.Geocoding API: Converts addresses into geographic coordinates. (https://developers.google.com/maps/documentation/geocoding/overview)
.Google Maps API: Displays the map and routes visually. (https://developers.google.com/maps/documentation)

4.How to run the app locally:
.Clone the repository: 
->git clone <repository-url>
->cd ROUTEAPP
.Open index.html in your browser or use a live server:
->n VS Code, install the Live Server extension and right click "open with Live" in the index.html file.

5.Deployment process:
.Uploading files to webservers:
->scp index.html styles.css script.js ubuntu@web-01-ip-address:/var/www/html/
->scp index.html styles.css script.js ubuntu@web-02-ip-address:/var/www/html/
.Configure Ngnix load balancer:
->sudo nano /etc/nginx/sites-available/default
.Restarting Nginx:
->sudo systemctl restart nginx
.Access the ROUTEAPP via the load balancer_ip_address.

6.Challenges and Solutions:
.Movable Route Limitation: Making the route draggable was hindered by API costs. I adapted by focusing on accurate static routing.
.File Permissions During Deployment: Adjusted file permissions to prevent deployment errors, excluding the .git directory from uploads.

7.Credits:
.Google Maps Platform: For their powerful suite of APIs enabling seamless routing and geolocation.
.Visual Studio Code: For its convenient development environment and live server feature.