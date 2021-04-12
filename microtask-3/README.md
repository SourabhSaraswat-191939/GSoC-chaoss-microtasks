## Microtask-2

Based on the elasticsearch documents produced by micro-mordred and source code of chaoss/grimoirelab-elk, try to answer the following questions:

### 1. What is the meaning of the JSON attribute author_id?
`author_id` is an id provided by Sortinghat, it is to identify each different identity of SortingHat.

### 2. What is the meaning of the JSON attribute author_org_name?
Name of Organization to which autor is affiliated . One author can affiliated to different organization for different time-periods.

### 3. What is the meaning of the JSON attribute author_uuid?
`author_uuid` is an unique identifier for user profile. One author_uuid can consist of 1 or more author_id. By this we can identify the actual number of users.

### 4. What is the meaning of the JSON attribute author_domain?
`author_domain` is the Domain associated with the profile of an author in Sortinghat.

### 5. What is the meaning of the JSON attribute uuid?
`uuid` is an attribute in fetched Raw data which uniquely identify each item .

### 6. What is the meaning of the JSON attribute utc_commit?
`utc_commit` is the commit data in UTC.

### 7. What is the meaning of the JSON attribute origin?
`origin` is reference URL to the refository from where data to be fetched.
