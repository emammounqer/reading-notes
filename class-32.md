# Class 32 - Permissions & Postgresql

## What are the key components and purpose of Django Rest Framework (DRF) permissions, and how do they help in securing an API?

Together with authentication and throttling, permissions determine whether a request should be granted or denied access.

Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.

Permissions are used to grant or deny access for different classes of users to different parts of the API.

## In SQL, what is the purpose of the SELECT statement, and how would you use it to retrieve all columns from a table called ‘employees’?

The SELECT statement is used to select data from a database. The data returned is stored in a result table, called the result-set.

```sql
SELECT * FROM employees;
```

## Can you explain the role of DRF Generic Views and provide examples of their usage in building a RESTful API?

DRF Generic Views are a set of already implemented views that can be used to perform common tasks. They are used to simplify the creation of RESTful APIs.

```python
from rest_framework.permissions import IsAuthenticated
from rest_framework.response import Response
from rest_framework.views import APIView

class ExampleView(APIView):
    permission_classes = [IsAuthenticated]

    def get(self, request, format=None):
        content = {
            'status': 'request was permitted'
        }
        return Response(content)
```
