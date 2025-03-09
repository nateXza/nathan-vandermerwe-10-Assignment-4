# System Specification  

## Introduction  
**Project Title**: CropGuardian: AI-Powered Crop Disease Detection  
**Domain**: Precision Agriculture  
**Problem Statement**:  
Traditional crop disease detection in South Africa is slow, error-prone, and inaccessible to small-scale farmers. CropGuardian addresses this by providing an AI tool for rapid, accurate disease identification.  

**Individual Scope**:  
- Focus on 5 diseases: Maize Streak Virus, Citrus Black Spot, Fusarium Wilt, Late Blight, Downy Mildew.  
- Use open-source datasets (e.g., Kaggle) and frameworks (TensorFlow, Angular).  
- Deployable on cloud platforms (AWS/Azure).  

---

## Functional Requirements  
1. **Image Upload**: Users can upload crop images via drag-and-drop.  
   - *Acceptance Criteria*: Images process in <2 seconds.  
2. **Disease Prediction**: CNN model classifies images into 5 disease categories.  
   - *Acceptance Criteria*: ≥95% accuracy on validation data.  
3. **Recommendations**: Provides treatment steps and Wikipedia links.  
4. **Multi-Language Support**: Interface available in English, isiZulu, Afrikaans.  
5. **Data Export**: Generate PDF reports of predictions.  

---

## Non-Functional Requirements  
- **Performance**: <1s latency for predictions.  
- **Security**: AES-256 encryption for user data.  
- **Scalability**: Support 10k concurrent users.  
- **Usability**: WCAG 2.1 compliance.  
