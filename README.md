# shinyserver

## 1. Version info

R Shiny Server 1.3 (on Ubuntu 14.04)
Shiny server lets you put shiny web applications and interactive documents online.

## 2. Use

### Create a container from this image: 
docker run -d --name shinyserver -p 80:3838 -v /srv/shinyapps/:/srv/shiny-server/ -v /srv/shinylog/:/var/log/ kenvanderheyden/shinyserver

### Start the container: 
docker start shinyserver

### Copy your R shiny app: 
Copy your app folder to the local folder mapped into your container. 
For the example run statement above this would be: /srv/shinyapps/ folder on your local machine. (for linux)

### Use your app: 
Browse to the url http://localhost/YourAppFolderName (for linux). 
Replace "YourAppFolderName" with the actual name of the application folder that contains both server.R and ui.R files at minimum. 
