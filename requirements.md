# BhashaSetu AI - Requirements Document

## 1. Project Overview

BhashaSetu AI is a culturally-aware government scheme navigator designed for Indian citizens. The system enables users to describe their real-life situations in natural language or voice and receive personalized recommendations for eligible government schemes. Unlike traditional information portals, BhashaSetu AI translates complex policy language into culturally appropriate, story-based explanations that resonate with users' lived experiences, literacy levels, and local contexts.

## 2. Problem Statement

Millions of Indian citizens remain unaware of government schemes they are eligible for due to:

- Complex bureaucratic and legal language in official documentation
- Lack of awareness about scheme existence and eligibility criteria
- Language barriers beyond simple translation (cultural context matters)
- Difficulty navigating multiple schemes across central and state governments
- Low digital and functional literacy in rural and semi-urban areas
- Disconnect between policy language and citizens' real-world problems

Current solutions provide information access but not understanding access. Citizens need culturally grounded explanations that connect abstract policies to their daily lives.

## 3. Goals and Non-Goals

### Goals

- Enable users to discover relevant government schemes by describing their situation naturally
- Provide culturally appropriate explanations using local metaphors, stories, and context
- Support multiple Indian languages with cultural translation, not just literal translation
- Adapt explanations based on user context (rural/urban, literacy level, region)
- Make scheme information accessible through voice and text interfaces
- Build trust through transparent, explainable AI recommendations

### Non-Goals

- Direct application submission or form filling (out of hackathon scope)
- Real-time integration with government databases for application status
- Payment processing or financial transactions
- Legal advice or guaranteed eligibility determination
- Comprehensive coverage of all schemes (focus on high-impact schemes for MVP)
- Multi-turn conversational dialogue (focus on single query-response for MVP)

## 4. Target Users

### Primary Users

- **Rural citizens** with low digital literacy seeking agricultural, housing, or welfare schemes
- **Urban low-income families** looking for education, health, or employment schemes
- **Women and marginalized communities** often excluded from information access
- **Senior citizens** seeking pension and healthcare benefits

### Secondary Users

- **Community workers and NGO staff** helping citizens access schemes
- **Gram Panchayat officials** providing scheme information to villagers
- **Self-help group members** seeking collective benefits

### User Characteristics

- Age range: 18-70+ years
- Literacy levels: Non-literate to graduate
- Digital literacy: Low to moderate
- Language preference: Hindi, Tamil, Telugu, Bengali, Marathi (prioritize for MVP)
- Device access: Basic smartphones, feature phones (voice), shared devices

## 5. Functional Requirements

### 5.1 User Input and Query Processing

**5.1.1** The system shall accept user queries in natural language text describing their situation, needs, or problems.

**5.1.2** The system shall accept voice input in supported Indian languages and convert it to text for processing.

**5.1.3** The system shall support at least 3 major Indian languages for MVP (Hindi, Tamil, Telugu recommended).

**5.1.4** The system shall extract key information from user queries including: demographic details, location context, problem domain, and implicit needs.

**5.1.5** The system shall handle incomplete or ambiguous queries by making reasonable inferences based on context.

### 5.2 Scheme Matching and Recommendation

**5.2.1** The system shall maintain a curated database of at least 20-30 high-impact central and state government schemes for MVP.

**5.2.2** The system shall match user situations to relevant schemes based on eligibility criteria including age, income, gender, location, occupation, and specific needs.

**5.2.3** The system shall rank matched schemes by relevance to the user's stated situation.

**5.2.4** The system shall return top 3-5 most relevant schemes for any given query.

**5.2.5** The system shall provide confidence scores or indicators for each recommendation.

### 5.3 Cultural Translation and Explanation

**5.3.1** The system shall generate explanations in culturally appropriate language that avoids bureaucratic jargon.

**5.3.2** The system shall adapt explanations based on detected or specified user context (rural/urban, literacy level, region).

**5.3.3** The system shall use local metaphors, analogies, and storytelling techniques relevant to the user's cultural context.

**5.3.4** The system shall explain scheme benefits in terms of real-world outcomes (e.g., "helps you build a pucca house" instead of "provides housing subsidy").

**5.3.5** The system shall present eligibility criteria as simple yes/no questions or relatable scenarios.

**5.3.6** The system shall provide next steps in actionable, sequential language (e.g., "First, go to your nearest Anganwadi center").

### 5.4 Output and Presentation

**5.4.1** The system shall display scheme recommendations with: scheme name in local language, simple explanation, eligibility summary, key benefits, and basic next steps.

**5.4.2** The system shall support text-to-speech output for low-literacy users.

**5.4.3** The system shall provide visual indicators (icons, colors) to enhance comprehension for low-literacy users.

**5.4.4** The system shall allow users to request more detailed information about any recommended scheme.

**5.4.5** The system shall provide scheme information in the same language as the user's query.

### 5.5 Explainability and Transparency

**5.5.1** The system shall explain why each scheme was recommended based on the user's stated situation.

**5.5.2** The system shall clearly indicate when information might be outdated or requires verification.

**5.5.3** The system shall provide sources or references for scheme information (e.g., official government portal links).

**5.5.4** The system shall allow users to provide feedback on recommendation relevance.

## 6. Non-Functional Requirements

### 6.1 Performance

**6.1.1** The system shall return scheme recommendations within 5 seconds for 90% of queries.

**6.1.2** The system shall support at least 100 concurrent users during hackathon demo.

**6.1.3** Voice input processing shall complete within 3 seconds for 30-second audio clips.

### 6.2 Privacy and Security

**6.2.1** The system shall not store personally identifiable information (PII) beyond the current session.

**6.2.2** The system shall process queries without requiring user registration or authentication for MVP.

**6.2.3** The system shall anonymize any logged data used for system improvement.

**6.2.4** The system shall comply with Indian data protection principles and best practices.

### 6.3 Accessibility

**6.3.1** The system shall be usable on devices with screen sizes from 4 inches to desktop monitors.

**6.3.2** The system shall function on low-bandwidth connections (2G/3G networks).

**6.3.3** The system shall support voice input and output for users with visual impairments or low literacy.

**6.3.4** The system shall use simple, clear visual design with high contrast for readability.

**6.3.5** The system shall minimize data usage to accommodate users with limited data plans.

### 6.4 Usability

**6.4.1** The system shall require no more than 2 interactions to receive scheme recommendations (query input and result viewing).

**6.4.2** The system shall provide clear error messages in the user's language when queries cannot be processed.

**6.4.3** The system shall use culturally familiar UI patterns and iconography.

### 6.5 Accuracy and Reliability

**6.5.1** The system shall achieve at least 70% accuracy in matching relevant schemes to user queries during testing.

**6.5.2** The system shall correctly identify user language with 90% accuracy.

**6.5.3** The system shall provide accurate scheme information verified against official government sources.

### 6.6 Explainability

**6.6.1** The system shall make AI decision-making transparent by showing which aspects of the user's query triggered each recommendation.

**6.6.2** The system shall avoid "black box" recommendations by providing clear reasoning.

**6.6.3** The system shall indicate confidence levels for recommendations.

## 7. Assumptions and Constraints

### Assumptions

- Users have access to smartphones or can access the system through community workers
- Basic internet connectivity is available (2G minimum)
- Users are willing to describe their situation to receive recommendations
- Government scheme information is publicly available and can be curated for the database
- Cultural context patterns can be identified and encoded for major user segments

### Constraints

- **Time constraint**: 24-48 hour hackathon timeline limits scope to MVP features
- **Data constraint**: Limited availability of structured, multilingual government scheme data
- **Resource constraint**: No access to official government APIs or real-time databases
- **Language constraint**: MVP will support 3-5 languages maximum
- **Scheme coverage**: MVP will cover 20-30 high-impact schemes, not comprehensive coverage
- **Testing constraint**: Limited time for user testing with actual target demographic
- **Infrastructure constraint**: Deployment on free or low-cost cloud services

## 8. Success Metrics

### Primary Metrics

- **Recommendation relevance**: 70%+ of test users find at least one recommended scheme relevant to their situation
- **Comprehension**: 80%+ of test users can explain a recommended scheme in their own words after reading the explanation
- **Cultural appropriateness**: 75%+ of test users rate explanations as "easy to understand" and "relatable to my life"
- **Language accuracy**: 90%+ accuracy in language detection and translation quality

### Secondary Metrics

- **Response time**: Average query-to-result time under 5 seconds
- **User satisfaction**: 4+ out of 5 rating on ease of use
- **Coverage**: System successfully handles 80%+ of test queries without errors
- **Accessibility**: System usable by users with varying literacy levels (tested with representative users)

### Hackathon Demo Metrics

- Successful demonstration with 5+ diverse test scenarios
- Positive feedback from judges on cultural translation approach
- System stability during live demo (no crashes or major errors)

## 9. Ethical Considerations

### 9.1 Fairness and Inclusion

- The system must not discriminate based on caste, religion, gender, or socioeconomic status
- Scheme recommendations must be based solely on eligibility criteria, not biased patterns in training data
- The system must serve marginalized communities as effectively as privileged users
- Language and cultural support must not favor urban or educated users

### 9.2 Transparency and Trust

- Users must understand that the system provides information, not guaranteed eligibility
- AI limitations must be clearly communicated (e.g., "This is a recommendation, please verify eligibility")
- Sources of information must be traceable to official government documentation
- The system must not make false promises about scheme benefits or approval likelihood

### 9.3 Privacy and Dignity

- Users must not be required to share sensitive personal information publicly
- The system must respect user dignity by avoiding patronizing or condescending language
- Cultural explanations must be respectful and avoid stereotypes
- User queries and data must be handled with confidentiality

### 9.4 Accuracy and Harm Prevention

- Incorrect recommendations could cause users to waste time and resources
- The system must clearly indicate when information might be outdated
- The system must not provide legal or financial advice beyond scheme information
- Error handling must fail gracefully without misleading users

### 9.5 Digital Divide Considerations

- The system must not assume high digital literacy or expensive devices
- Voice and visual interfaces must accommodate users with disabilities
- The system should work in low-connectivity environments
- Community-based access models should be considered (e.g., through NGO workers)

### 9.6 Cultural Sensitivity

- Cultural translation must be done respectfully, avoiding appropriation or mockery
- Local metaphors and stories must be authentic and validated with community members
- The system must respect regional diversity and avoid homogenizing Indian culture
- Explanations must be empowering, not reinforcing existing power imbalances

---

**Document Version**: 1.0  
**Last Updated**: February 14, 2026  
**Status**: Draft for Hackathon Submission
