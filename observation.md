# 1. AI Model Used

Model 1: GPT-6.1 Sol

Model 2: Gemini 3.8 Flash

# 2. Prompt Used

Create a responsive landing page for an FDE (Forward Deployed Engineer) service using HTML and CSS. Include a header, hero section with dual CTAs, features grid, how-it-works workflow, social proof section, and a footer. Ensure clean structure, modern styling, and mobile responsiveness.

# 3. Code Quality Observation

| Area             | Model 1                                                 | Model 2                                                                                             |
| :--------------- | :------------------------------------------------------ | :-------------------------------------------------------------------------------------------------- |
| Code structure   | Semantic HTML with centralized CSS and no JavaScript    | centralized CSS and no JavaScript. Semantic HTML with CSS, inline styles and JavaScript in one file |
| Readability      | Concise, consistently formatted and easy to follow      | Well-formatted, but verbose inline styles add clutter                                               |
| Component design | Reusable classes for buttons, cards and layout sections | Reusable button, panel and grid classes, but repeated inline styling limits reuse                   |
| Documentation    | Descriptive class names, but few explanatory comments   | but few explanatory comments. Helpful comments explain sections, styles and JavaScript behavior     |
| Error handling   | No custom error handling. Interactions use native HTML. | Uses native form validation, but submissions only simulate success and provide no failure handling  |

# 4. AI Hallucination Observation

**Observation 1 — False form submission confirmation (Gemini):**  
The page claims an engineer has received the user’s briefing, but the JavaScript only displays a success message. No data is sent to a server.

**Observation 2 — False newsletter subscription confirmation (Gemini):**  
The page displays “Subscribed to Production Dispatch,” but the code only shows a message and resets the form. No subscription is created.

**Observation 3 — Unsupported performance claims (Gemini):**  
The AI generated metrics such as “99.995% Uptime” and “14,200 tok/sec (+310%)” without supporting data. These claims require human verification.

**Observation 4 — Placeholder contact information (ChatGPT):**  
The AI used `hello@example.com` as the contact address. It is explicitly labeled as a demo address and must be replaced before launch.

# 5. Final Decision

ChatGPT produced better results because its code has a cleaner structure, reusable CSS classes, good accessibility implementation, and fewer inline styles. It also labels sample content clearly. On the other hand, Gemini included unrealistic performance claims and simulated form success messages. Both covered the requested sections, but ChatGPT followed the requirements closely with HTML and CSS implementation while Gemini added JS features that made the thing more complex.
