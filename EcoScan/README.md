


# **EcoScan: Clothing Carbon Footprint Scanner**

## **1. Overview**

EcoScan is a web application that empowers users to assess the environmental impact of their clothing choices. By analyzing images of clothing items, the app calculates their carbon footprint, assigns eco reward points based on eco savings, and provides a catalog of redeemable offers.  The solution is designed as a full stack application, with a React based front end and a Python-based backend using Flask/FastAPI.


## **2. Goals and Features**

### **Goals**

1.  Provide users with a transparent understanding of their clothing's carbon footprint.
2.  Incentivize sustainable clothing choices through an eco reward points system.
3.  Offer an engaging user experience with an intuitive interface.

### **Key Features**

-   Upload or capture clothing images.
-   Real time recognition of clothing items and calculation of their carbon footprint.
-   Display total carbon score and eco reward points.
-   Showcase redeemable offers based on user points.


## **3. Functional Requirements**

### **Frontend Requirements**

1.  **User Interface**:
    
    -   Upload or capture images via camera.
    -   Display list of recognized clothing items.
    -   Show carbon scores, eco reward points, and redeemable offers.
2.  **Interactivity**:
    
    -   Dynamic display of eco-scores upon item recognition.
    -   Responsive design to ensure usability across devices.


### **Backend Requirements**

1.  **API Endpoints**:
    
    -   **Image Analysis**: Accepts an image file and returns recognized items with their      	estimated carbon scores.
    -   **Eco-Score Calculation**: Calculates the carbon footprint and eco reward points based on recognized items.
    -   **Offers Retrieval**: Returns redeemable offers based on user points.
2.  **Data**:
    
    -   In memory store to manage predefined carbon footprint values for clothing items.
    -   Sample list of redeemable offers based on eco-reward points.
3.  **Assumptions**:
    
    -   Carbon footprints of clothing items are predefined (e.g., T-shirt: 5 kg CO₂, 
         Jeans: 10 kg CO₂).
    -   Reward Points = (Base Carbon Score - Item Carbon Score) × Multiplier.


## **4. Technical Requirements**

### **Frontend**

-   **Framework**: React (preferred).
-   **Dependencies**:
    -   React Camera API for photo capture.
    -   Axios or Fetch API for backend communication.
    -   Styling with CSS.

### **Backend**

-   **Framework**: Python-based (FastAPI/ Flask).
-   **Dependencies**:
    -   Pillow or OpenCV for basic image preprocessing.
    -   Pre-trained model (mocked or external API) for clothing recognition.
    -   In-memory data structures (e.g., Python dictionaries) for carbon scores.

## **5. System Architecture**

### **Diagram**

`[Frontend: React] <----HTTP----> [Backend: FastAPI]
      ⬑                                        ⬎
   [Camera / Upload]                [Image Recognition & Carbon Scores]` 

### **Components**

1.  **Frontend**:
    
    -   **FileUploader Component**: Handles image upload and camera integration.
    -   **EcoScore Display**: Displays items, scores, and points.
    -   **Offers Display**: Renders redeemable offers.
2.  **Backend**:
    
    -   **ImageRecognition API**: Simulates item recognition.
    -   **EcoScoreCalculator**: Computes carbon scores and points.
    -   **Offers API**: Fetches offers based on user points.

## **6. Implementation Steps**

### **Step 1**: Setup Frontend

-   Initialize a React project using create react app.
-   Develop UI components:
    -   **UploadButton**: Integrates file input and camera API.
    -   **EcoScoreCard**: Displays identified items, scores, and points.
    -   **OffersList**: Lists redeemable offers dynamically.

### **Step 2**: Setup Backend

-   Initialize a Python project with the chosen framework.
-   Create the following API routes:
    -   upload: Handles image upload and returns recognized items.
    -   calculate: Accepts item list and returns carbon scores and eco-reward points.
    -   offers: Returns redeemable offers based on points.

### **Step 3**: Integrate Frontend and Backend

-   Use Axios for HTTP requests from React to the backend.
-   Implement error handling for API calls.

## **7. Deployment Plan**

### **Frontend Deployment**

-   Host on GitHub Pages.

### **Backend Deployment**

-   Use Microsoft Azure.
-   Expose backend endpoints securely with HTTPS.

## **8. Enhancements Proposal**

### **Improved Carbon Scoring**

-   Integrate external APIs for more accurate carbon scores.

### **Enhanced User Insights**

-   Provide sustainability comparisons (e.g., this item saves X% compared to average).
-   Track user’s historical eco-reward points and carbon footprint.

### **Real-Time Data Integration**

-   Partner with retailers for real-time sustainability scores.
-   Offer live updates on eco-friendly discounts and offers.

----------