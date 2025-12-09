## Authorization Test Report

Student: Maxence Gautier-Grall / Ilan Rubaud

In this report, we have listed and described all the things that the following three roles can do on a test website: Guest, Reserver, and Administrator. 


### List of all pages and endpoints :
* http://localhost:8003/
* http://localhost:8003/resources
* http://localhost:8003/reservation
* http://localhost:8003/reservation?id=...
* http://localhost:8003/resources?id=...
* http://localhost:8003/register
* http://localhost:8003/login
* http://localhost:8003/api/reservation
* http://localhost:8003/api/resources            
* http://localhost:8003/api/session              
* http://localhost:8003/api/users
---
## Role (Guest, Reserver, Administrator)
---

### 🧑‍🦲 **Guest**

---

**✅ Can do**

Here are all the actions that Guests can perform:

* “Can view public resource list — `/`”
* “Can access login form — `/login`”
* "Can see reservation but without the name of the person whe reserved"
* "Can access Register form '/register'"
* "Can register if they are over 15 years of age."
* "Can access the '/api/reservation'"
* "Can access the '/api/resources'"
* "Can access the '/api/users'"
* "Can add resources '/resources'"


---

**❌ Cannot do**

Here are all the actions that Guests can not perform:

* “Cannot access to the page '/resources' ”
* “Cannot access to the page '/reservation' ”
* “Cannot see who made the reservations"
* “Cannot access reserver profile page `/profile`”
* "Cannot access the '/api/session'"

---

### 🧑‍💼 **Reserver**

---

**✅ Can do**

Here are all the actions that Reservers can perform:

Example format:

* “Can book a resource — /reservation ”
* "Can login as a reserver -- /login"
* “Can list resources — /resources”
* "Can modify his reservation -- /reservation?id=?"
* "Can modify the reservation of another reserver with the link '/reservation?id=?'"
* "Can access the '/api/reservation'"
* "Can access the '/api/resources'"
* "Can access the '/api/users'"
* "Can access the '/api/session'"
    

---

**❌ Cannot do**

Here are all the actions that Reservers can not perform:

* “Cannot delete other users ”
* “Cannot modify his resources and the other resources”
* “Cannot modify his own information”
* “Cannot escalate privileges via hidden form fields (test with Brup suit)” 

---

### 🧑‍💼🛡️ **Administrator**

---

**✅ Can do**

Here are all the actions that Administrator can perform:

* “Can add a resource — `/admin/resources/new`”
* “Can delete a reservation in '/reservation?id=1'"
* “Can manage a reservation in '/reservation?id=1'"
* “Can view all users”
* "Can manage and modify the ressouces in '/resources?id=1'"
* "Can access the '/api/reservation'"
* "Can access the '/api/resources'"
* "Can access the '/api/users'"
* "Can access the '/api/session'"

---

**❌ Cannot do**

Here are all the actions that Administrator can not perform:

* “Cannot delete resources”
* "Cannot delete reserver"

---
## Zap Finding
---
-> "With Zap, we also found the /static page, the /robots.txt link, and the /sitemap.xml link."
