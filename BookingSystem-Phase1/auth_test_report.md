## Authorization Test Report

Student: Maxence Gautier-Grall / Ilan Rubaud

In this report, we have listed and described all the things that the following three roles can do on a test website: Guest, Reserver, and Administrator.


---

### 🧑‍🦲 **Guest**

---

**✅ Can do**

List every action a *Guest* can perform, with the page or endpoint.
Example format:

* “Can view public resource list — `/`”
* “Can access login form — `/login`”
* “Can view registered reservations without identity — `/` (spec 8)”

---

**❌ Cannot do**

List every action that a *Guest* is blocked from doing.
Example format:

* “Cannot access `/reservation` (redirect to login)”
* “Cannot POST `/api/reservations`”
* “Cannot access any `/admin/*` pages”
* “Cannot access reserver profile page `/profile`”

---

### 🧑‍💼 **Reserver**

---

**✅ Can do**

List actions a *Reserver* can do according to specs + actual test results.
Include visible pages **and** API endpoints.

Example format:

* “Can book a resource — `/reservation` + `/api/reservations`”
* “Can view own profile page — `/profile`”
* “Can list resources — `/resources`”

---

**❌ Cannot do**

List actions a *Reserver* is correctly blocked from.

Example format:

* “Cannot access admin user list — `/admin/users`”
* “Cannot delete other users — `/api/admin/users/:id`”
* “Cannot modify resources (spec says admin only)”
* “Cannot escalate privileges via hidden form fields”

---

### 🧑‍💼🛡️ **Administrator**

---

**✅ Can do**

List actions an *Administrator* can perform.

Example format:

* “Can add a resource — `/admin/resources/new`”
* “Can delete a reserver — `/admin/users/delete/:id`”
* “Can manage all reservations — `/admin/reservations`”
* “Can view all users (spec 4)”

---

**❌ Cannot do**

List prohibited behaviors, if any, or incorrect implementation issues.

Example format:

* “Cannot book a resource if the system incorrectly blocks admins (bug?)”
* “Cannot perform an action because the UI has no link (but API allows?) — flag as ⚠️”

---
