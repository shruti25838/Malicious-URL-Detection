## Malicious URL Detection System

This project is a complete web-based application for detecting **malicious URLs** using machine learning and real-time feature extraction. It uses a Flask backend, a trained Gradient Boosting model, and a custom-built feature extraction engine that analyzes the structure, behavior, and metadata of URLs.

---

##  How It Works

1. **User inputs a URL** through the web interface.
2. **Features are extracted** from the URL using WHOIS info, domain structure, and content analysis.
3. **Trained model (model.pkl)** classifies the URL as **Safe** or **Malicious**.
4. **Confidence score** is displayed to the user on the frontend.

---

##  Features Extracted (30)

This project extracts a rich set of features, including:

- IP Address in URL
- Length of URL / domain
- Shortened URL detection (bit.ly, tinyurl, etc.)
- `@` symbols and redirect patterns
- HTTPS presence
- WHOIS info like domain age and registration length
- JavaScript-based attacks (popups, status bar spoofing)
- Google Index presence
- Alexa/Rank checks
- DNS and traffic validation
- Suspicious TLDs and IP blocks

> All feature logic is encapsulated in `feature.py`.

---

## Frontend

- **Responsive HTML/CSS**
- URL input field with submit button
- Shows result as:
  -  Safe
  -  Unsafe
- Background styling via `url.jpeg`

---

This project successfully demonstrates how machine learning can be used to detect malicious URLs with high accuracy. Through detailed feature extraction and model comparison, we found that the Gradient Boosting Classifier delivered the best performance with 97.4% accuracy, followed closely by CatBoost and Random Forest.

