# Convert Trello JSON to JIRA JSON

This tool is intended to help a 1-time migration of the Trello-exported JSON into a JIRA-import supported format. 

- Trello format: https://help.trello.com/article/924-making-sense-of-trellos-json-export
- JIRA format: https://confluence.atlassian.com/adminjiracloud/importing-data-from-json-776636779.html

The first version of this tool is intended for JIRA Cloud importing. All contributions to expand this convertion tool are welcome.

## How to Use it

    # Convert the file trello.json into jira.json
    ttj to-jira trello.json jira.json
    # or
    ttj j trello.json jira.json
    
If you need to map specific users and/or project, you can specify `mapping.json` like that:
    
    ttj -m mapping.json to-jira trello.json jira.json
    
and `mapping.json` should contain something like that:

```json
{
    "projects": {
        "Trello Board Name": {
            "name": "JIRA Project Name",
            "key": "JIRA"
        }
    },
    "users": {
        "username": {
            "name": "name",
            "fullName": "fullName", 
            "email": "email@example.org" 
        } 
    },
    "status": {
        "ideas": {"status": "Open", "resolution": null},
        "ready": {"status": "Done", "resolution": "Resolved"}
    }  
}
```  

## Supported Features

- Trello Members into JIRA Users
- Trello Cards to JIRA Issues (with comments)


## Known Bugs and Limitations
