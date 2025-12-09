## Authorization Test Report

Student: Maxence Gautier-Grall / Ilan Rubaud

In this report, we have listed and described all the things that the following three roles can do on a test website: Guest, Reserver, and Administrator.


---

### 🧑‍🦲 **Guest**

---

**✅ Can do**

Here are all the actions that Guests can perform:

* “Can view public resource list — `/`”
* “Can access login form — `/login`”
* "Can see reservation but without the name of the person whe reserved"
* "Can access Register form '/register'"

---

**❌ Cannot do**

Here are all the actions that Guests can not perform:

* “Cannot access to the page '/resources' ”
* “Cannot access to the page '/reservation' ”
* “Cannot see who made the reservations"
* “Cannot access any `/admin/*` pages”
* “Cannot access reserver profile page `/profile`”

---

### 🧑‍💼 **Reserver**

---

**✅ Can do**

Here are all the actions that Reservers can perform:

Example format:

* “Can book a resource — `/reservation` + `/api/reservations`”
* “Can view own profile page — `/profile`”
* “Can list resources — `/resources`”

---

**❌ Cannot do**

Here are all the actions that Reservers can not perform:

* “Cannot access admin user list — `/admin/users`”
* “Cannot delete other users — `/api/admin/users/:id`”
* “Cannot modify resources (spec says admin only)”
* “Cannot escalate privileges via hidden form fields”

---

### 🧑‍💼🛡️ **Administrator**

---

**✅ Can do**

Here are all the actions that Administrator can perform:

* “Can add a resource — `/admin/resources/new`”
* “Can delete a reservation in '/reservation?id=1'"
* “Can manage a reservation in '/reservation?id=1'"
* “Can view all users (spec 4)”
* "Can manage and modify the ressouces in '/resources?id=1'"

---

**❌ Cannot do**

Here are all the actions that Administrator can not perform:

/////* “Cannot book a resource if the system incorrectly blocks admins (bug?)”
/////* “Cannot perform an action because the UI has no link (but API allows?) — flag as ⚠️”

---
