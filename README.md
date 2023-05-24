# midterm-project---ecosnap-api-barbar0619
midterm-project---ecosnap-api-barbar0619 created by GitHub Classroom

![hacettepe](https://user-images.githubusercontent.com/38729621/228668415-9e9732b7-9678-4d20-a616-cd8bc0ffbd60.jpeg)

# **GMT352 Geographic Information Systems**

---

# EcoSnap

Ecosnap is a mobile application developed by Associate Professor Berk Anbaroğlu and İlyas Çokan. The application can be downloaded from the google play store via an android phone.

EcoSnap aims to collect real-time citizen participation in the determination of environmental and health problems during the creation of urban planning.

Enables to report an array of incidents including, but not limited to:

- Weak Eduroam
- Environmental Pollution
- Bad Sidewalk
- Electrical Problem
- Wrong Parking
- Waste
- Other Problems

---

# Individual Project


First I downloaded the Ecosanp application to my android mobile phone. I contribute 5 posts to the apllication. Here are my post images:

# Post from Armada
![Armada](https://user-images.githubusercontent.com/38729621/236045046-e7c3140d-cada-4230-af77-ed1e5e281da5.jpg)

# Post from Gata
![gata](https://user-images.githubusercontent.com/38729621/236045054-2a1a5d0f-ad3e-4339-aa4e-67a559dd92df.jpg)

# Post from a road of Mamak
![Mamak Yol](https://user-images.githubusercontent.com/38729621/236045069-2571c870-a4b2-4644-be34-b3c425d0dd04.jpg)

# Post from sidewalk of Mamak
![Mamak kaldırım](https://user-images.githubusercontent.com/38729621/236045077-b75364ce-271f-4eed-855d-f46979bb354e.jpg)

# Post from Beytepe
![Beytepe](https://user-images.githubusercontent.com/38729621/236045090-54ba9ce2-bf75-4758-9f9c-fdcfaf777f47.jpg)

Then I Sign up to Postman and get my user Id. With my user Id, I obtained my posts in Ecosnap. Here are a screenshot from postman:

![results_postman](https://user-images.githubusercontent.com/38729621/236043427-4c428eb0-449d-4c84-b9a0-506bd88c0a7c.png)

Then For interactive map production, I decided to use folium using a python script in Google Colab. Here is python code:

```
#import necessary libraries
import requests
import folium
from folium.plugins import MarkerCluster

#Define coordinates of where we want to center our map
ecosnap_center = [39.930000, 32.890000]

#Create the map
my_map = folium.Map(location = ecosnap_center, zoom_start = 13)
hatch_has_fallen = [39.8687748,32.8088858 ]
unprotected_fence_off= [39.9674087,32.8465763 ]
Bad_sidewalk = [39.939664,32.8904371]
Sidewalk= [39.9394249,32.8904301]
Damaged_road=[39.8662157,32.7332884]

#Add markers to the map
folium.Marker(hatch_has_fallen, popup = 'hatch_has_fallen').add_to(my_map)
folium.Marker(unprotected_fence_off, popup = 'unprotected_fence_off').add_to(my_map)
folium.Marker(Bad_sidewalk, popup = 'Bad_sidewalk').add_to(my_map)
folium.Marker(Sidewalk, popup = 'Sidewalk').add_to(my_map)
folium.Marker(Damaged_road, popup = 'Beytepe').add_to(my_map)

#Display the map
my_map

```

Here is my map:

![Tüm harita](https://user-images.githubusercontent.com/38729621/236044180-5569506c-2fc9-4a0b-99d7-179789840c81.png)

Unfortunately, two of my post was very close to each other so They can not be seen seperately from a distance. I zoomed and take a screenshot to visulize them:

![Mamak event](https://user-images.githubusercontent.com/38729621/236044479-5aef177f-7e2e-481a-b7a0-0f0cc8e340ce.png)

