# VaaniSetu AI – Requirements Document

## 1. Project Overview

VaaniSetu AI is a multilingual, voice-first AI assistant designed to improve access to government schemes, healthcare programs, agricultural support, and skill development initiatives for citizens across India.

The system bridges the information gap by enabling users to interact in their native language and receive personalized, document-backed responses.

---

## 2. Problem Statement

Many citizens in India face challenges in accessing public welfare schemes due to:

- Language barriers
- Complex government portals
- Low digital literacy
- Poor internet connectivity
- Lack of awareness about eligibility

Although information exists, accessibility remains limited.

---

## 3. Objectives

- Enable voice and text interaction
- Support multiple Indian languages (Tamil, Hindi, English initially)
- Provide eligibility-based personalized recommendations
- Work in low-bandwidth environments
- Use only publicly available or synthetic data

---

## 4. Target Users

- Rural citizens
- Farmers
- Students seeking scholarships
- Low-income families
- Small business owners
- Individuals seeking skill development programs

---

## 5. Functional Requirements

1. User can input queries via voice or text.
2. System detects and processes multiple languages.
3. System retrieves relevant scheme information using RAG.
4. System filters schemes based on eligibility inputs.
5. System provides required documents and application links.
6. Text-to-speech response generation.
7. Display source document references.

---

## 6. Non-Functional Requirements

- Response time under 3 seconds
- Scalable architecture
- Low bandwidth compatibility
- No storage of personal sensitive data
- Secure HTTPS communication
- Modular and extensible design

---

## 7. Data Requirements

- Public government scheme PDFs
- Public open datasets
- Synthetic user profiles for testing
- Structured JSON dataset for schemes

---

## 8. Assumptions

- Users provide accurate eligibility information.
- Public scheme data is available and up to date.
- Internet access is available for API calls (minimal bandwidth mode supported).

---

## 9. Limitations

- Not an official government platform.
- Informational support only.
- No legal or medical advice.
- Uses synthetic/public datasets only.

---

## 10. Success Metrics

- Query response accuracy
- Language recognition accuracy
- User interaction completion rate
- Reduction in search time for schemes
