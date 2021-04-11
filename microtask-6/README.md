## Microtask-6

Using the SortingHat GraphQL Console, create a query that fetches the data (identities, enrollments) of an individual profile.

### Query

    {
      individuals(pageSize:1) {
          entities {
            profile {
              id
              name
              email
              gender
              individual {
                identities {
                  uuid
                  name
                  email
                  username
                  source
                }
                enrollments {
                  organization {
                    name
                  }
                  start
                  end
                }
              }
            }
          }
        }
      }

### GIF of Executing Query to fetch individual data

![GraphQL_query.gif](https://github.com/SourabhSaraswat-191939/GSoC-chaoss-microtasks/blob/main/microtask-6/GraphQL_query.gif)
