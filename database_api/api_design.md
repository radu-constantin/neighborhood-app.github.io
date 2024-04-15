---
title: API Design
layout: default
parent: Database and API
---

RE-WRITE!

In developing the API for <span style="color:#FF0054">Neighbourhood</span>  we wanted to ensure that we adhere to REST[^1] principles.

Leveraging these principles, we designed an API that implemented a logical structure. Through standardized endpoints we achieved a consistent and intuitive experience for users across different devices and platforms.

Our API facilitated <span style="color:#FF0054">neighbourhood</span>  creation, membership management, and interaction, following RESTful conventions for resource manipulation. By defining clear and predictable endpoints for neighbourhood CRUD operations, users can seamlessly create, join, or leave neighborhoods, while neighbourhood admins can approve membership requests and update their neighbourhoods' information with ease.

Our users also have the ability to create and respond to their neighbours' requests. Both entities (<span style="color:#FF0054">requests</span> and <span style="color:#FF0054">responses</span>) were given their own routers with a multitude of available endpoints for streamlined interaction and collaboration.

By following the established patterns for resource management, interaction, and manipulation, we ensured a seamless and intuitive user experience.

![API Map](../assets/images/api_map.png)

---

[^1]: https://restfulapi.net
