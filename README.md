# Convert Trello JSON to Jira JSON

This tool is intended to help a 1-time migration of the Trello-exported JSON into a Jira-import supported format. 

- Trello format: https://help.trello.com/article/924-making-sense-of-trellos-json-export
- Jira format: https://confluence.atlassian.com/adminjiracloud/importing-data-from-json-776636779.html

The first version of this tool is intended for Jira Cloud importing. All contributions to expand this convertion tool are welcome.

## How to Use it

    # Convert the file trello.json into jira.json
    ttj to-jira trello.json jira.json
    # or
    ttj j trello.json jira.json

## Supported Features

- Trello Members into Jira Users


## Known Bugs and Limitations

