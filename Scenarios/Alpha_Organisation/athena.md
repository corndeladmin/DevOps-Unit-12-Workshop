# Athena: Knowledge Collection

![Athena Architecture](./diagrams/Athena.png)

Used by **Contributors** to provide information to Alpha.

Key activities it supports:

- Hosts the forms contributors use to update Alpha on their health and well-being. These can be accessed from both the web and Alpha's mobile app.
- Synchronises smart device data with third party APIs.
- Every six hours Athena sends all newly collected data to Apollo by compressing all its data and uploading it to Apollo's FTP site. Athena then wipes its own database.
