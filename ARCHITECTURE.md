C4 Architectural Diagrams 

# C4 Architecture  

## Level 1: Context Diagram  
```mermaid
graph TD
    A[Farmer] -->|Uploads Image| B[CropGuardian]
    B -->|Fetches Data| C[Open-Source Datasets]
    B -->|Stores Results| D[MySQL Database]
    B -->|Sends Alerts| E[Notification Service]
    F[Agricultural Extension Officer] -->|Validates Results| B

![Level 1 Context Diagram](https://i.imgur.com/UBBg39k.png)





Level 2
flowchart TD
    A[Farmer] -->|Accesses| B[Web/Mobile UI]
    B -->|API Calls| C[Backend - Python/Django]
    C -->|Processes Images| D[CNN Model - TensorFlow]
    C -->|Stores Data| E[MySQL Database]
    C -->|Sends Alerts| F[Twilio/SMS]
    G[Researchers] -->|Downloads Datasets| E
    H[Agricultural Officer] -->|Validates Results| C


