# CRUD API Basics (HTB & Real-World Understanding)

##  What is an API?

An API (Application Programming Interface) allows applications to communicate with a server or database. Instead of using a website interface, we send direct HTTP requests.

---

##  What is CRUD?

CRUD represents the 4 basic operations for managing data:

| Operation | HTTP Method | Description          |
| --------- | ----------- | -------------------- |
| Create    | POST        | Add new data         |
| Read      | GET         | Retrieve data        |
| Update    | PUT / PATCH | Modify existing data |
| Delete    | DELETE      | Remove data          |

---

##  How APIs interact with databases

APIs act as a middle layer between the user and database.

Example SQL behind the scenes:

* READ → `SELECT * FROM city WHERE name='london';`
* UPDATE → `UPDATE city SET name='flag' WHERE name='london';`
* DELETE → `DELETE FROM city WHERE name='london';`

---

## API URL Structure

Example:

```
/api.php/city/london
```

Breakdown:

* `api.php` → API endpoint
* `city` → database table
* `london` → specific record (row)

---

##  READ (GET request)

### Get one record:

```bash
curl http://SERVER_IP:PORT/api.php/city/london
```

### Get formatted output:

```bash
curl -s http://SERVER_IP:PORT/api.php/city/london | jq
```

### Search partial match:

```bash
curl -s http://SERVER_IP:PORT/api.php/city/le | jq
```

### Get all records:

```bash
curl -s http://SERVER_IP:PORT/api.php/city/ | jq
```

---

##  UPDATE (PUT request)

Used to modify existing data.

```bash
curl -X PUT http://SERVER_IP:PORT/api.php/city/london \
-H "Content-Type: application/json" \
-d '{"city_name":"flag","country_name":"(UK)"}'
```

Meaning:

* Target: `london`
* Update value: `flag`

---

##  DELETE (DELETE request)

Remove a record:

```bash
curl -X DELETE http://SERVER_IP:PORT/api.php/city/london
```

---

##  HTB Exercise Flow

1. List all cities (GET)
2. Pick a city
3. Update it to `"flag"` (PUT)
4. Delete any city (DELETE)
5. Search for `"flag"` (GET)

```bash
curl -s http://SERVER_IP:PORT/api.php/city/flag | jq
```

---

##  Key Takeaways

* APIs expose database operations over HTTP
* CRUD = Create, Read, Update, Delete
* JSON is the data format used to communicate
* URLs often represent database structure
* HTB labs test how well you understand and manipulate APIs

---

##  Real-World Understanding

Modern apps (Facebook, banking, shopping apps) use the same concept:

* Buttons → API calls
* UI actions → HTTP requests
* Database changes → CRUD operations

Learning this is the foundation of:

* Web development
* API security
* Penetration testing
