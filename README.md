This project implements a lightweight website health monitoring system using Bash.
It performs periodic HTTP checks using curl, logs status and response time, and automatically archives logs daily to maintain clean log rotation.

```
       Health Monitoring Script

        +------------------+
        |   Start Script   |
        +------------------+
                  |
                  v
     +---------------------------+
     | Define URL & Log Path     |
     +---------------------------+
                  |
                  v
     +---------------------------+
     | Create Log Directory      |
     +---------------------------+
                  |
                  v
     +---------------------------+
     | Send curl HTTP Request    |
     +---------------------------+
                  |
                  v
     +---------------------------+
     | Extract Status & Time     |
     +---------------------------+
                  |
                  v
     +---------------------------+
     | Append Data to Log File   |
     +---------------------------+
                  |
                  v
        +------------------+
        |      End         |
        +------------------+


      Log Archiving Script


        +------------------+
        |  Start Archive   |
        +------------------+
                  |
                  v
     +---------------------------+
     | Get Yesterday's Log File  |
     +---------------------------+
                  |
                  v
     +---------------------------+
     | Check If Log Exists       |
     +---------------------------+
           |               |
          No              Yes
           |               v
           |     +----------------------+
           |     | Already Archived?    |
           |     +----------------------+
           |         |            |
           |        Yes          No
           |         |            v
           |         |   +-------------------+
           |         |   | Compress Log File |
           |         |   +-------------------+
           |         |            |
           |         |            v
           |         |   +-------------------+
           |         |   | Delete Old Log    |
           |         |   +-------------------+
           v         v
     +---------------------------+
     | Log Archive Activity      |
     +---------------------------+
                  |
                  v
        +------------------+
        |       End        |
        +------------------+

```
