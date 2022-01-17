# HANA-AI-API_BASE
UPS CC_ACCESS
{
    "password": "Abcd123!",
    "schema": "",
    "tags": [
        "hana"
    ],
    "user": "ACCESS_GRANTOR"
}


API_DDL/API_DML
create role API_SCHEMA_ACCESS;
grant  SELECT, UPDATE, INSERT, DELETE, EXECUTE, SELECT METADATA ON SCHEMA AI_API TO API_SCHEMA_ACCESS with grant option;
grant  SELECT, UPDATE, INSERT, DELETE, EXECUTE, SELECT METADATA ON SCHEMA <...guid...> TO API_SCHEMA_ACCESS with grant option;

DBADMIN
grant API_SCHEMA_ACCESS to ACCESS_GRANTOR with admin option;
