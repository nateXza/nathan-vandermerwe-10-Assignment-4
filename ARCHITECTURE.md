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
```

## Level 2: Container Diagram
```mermaid
flowchart TD
    A[Farmer] -->|Accesses| B[Web/Mobile UI]
    B -->|API Calls| C[Backend - Python/Django]
    C -->|Processes Images| D[CNN Model - TensorFlow]
    C -->|Stores Data| E[MySQL Database]
    C -->|Sends Alerts| F[Twilio/SMS]
    G[Researchers] -->|Downloads Datasets| E
    H[Agricultural Officer] -->|Validates Results| C
```

## Level 3: Component Diagram 
```mermaid
graph TD
    A[API Gateway] -->|Routes Requests| B[Image Preprocessor]
    A -->|Routes Requests| C[Disease Predictor]
    A -->|Routes Requests| D[Recommendation Engine]
    B -->|Uses| E[OpenCV]
    C -->|Uses| F[TensorFlow/Keras]
    D -->|Fetches Data| G[MySQL Database]
    C -->|Saves Results| G
    D -->|Stores Recommendations| G
```

Explanation :

API Gateway : Routes user requests to the appropriate components.
Image Preprocessor : Uses OpenCV to clean and format uploaded images.
Disease Predictor : Uses TensorFlow/Keras for CNN-based disease classification.
Recommendation Engine : Fetches treatment data from the MySQL Database .
All components interact with the database to store/retrieve results.

## Level 4: Code Diagram
```mermaid
classDiagram
    class ImageHandler {
        +upload_image()
        +preprocess()
    }
    class Predictor {
        +classify_image()
        +generate_report()
    }
    class Database {
        +store_results()
        +fetch_history()
    }
    ImageHandler --> Predictor
    Predictor --> Database
```
Explanation :

ImageHandler : Manages image uploads and preprocessing.
Predictor : Uses the CNN model to classify images and generate reports.
Database : Stores prediction results and user history.
Arrows indicate dependencies (e.g., ImageHandler relies on Predictor).
