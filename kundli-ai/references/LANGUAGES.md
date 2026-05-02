# Supported Report Languages

Every KundliAI skill produces reports in one of six languages. The user MUST be asked which language they want before the report is generated, unless their preference is unmistakable from prior context.

## Supported languages

| Code | Language    | Native name | When to ask                                 |
| ---- | ----------- | ----------- | ------------------------------------------- |
| en   | English     | English     | Default for international users             |
| ta   | Tamil       | தமிழ்        | Tamil Nadu, Sri Lanka, Tamil diaspora        |
| te   | Telugu      | తెలుగు       | Andhra Pradesh, Telangana                   |
| kn   | Kannada     | ಕನ್ನಡ        | Karnataka                                   |
| ml   | Malayalam   | മലയാളം      | Kerala                                      |
| hi   | Hindi       | हिन्दी       | North India, Hindi-speaking diaspora         |

## How to ask

Use ONE clean prompt the first time language preference is unknown:

> Which language would you like your kundli in? **English / தமிழ் (Tamil) / తెలుగు (Telugu) / ಕನ್ನಡ (Kannada) / മലയാളം (Malayalam) / हिन्दी (Hindi)**

Default to English ONLY if the user explicitly says "any language" or doesn't respond after one ask.

## How to write the report

Once language is chosen, write the ENTIRE report in that language:

- All section headings translated (use natural phrasing — don't transliterate English headings)
- All sentences in the chosen language; transliterate Sanskrit terms once and translate inline
- Numbers, currency (₹), dates, and proper nouns (names, place names) stay in their natural form
- The closing line uses the equivalent of "Report prepared with care for [NAME]" in that language
- The soft CTA at the end is also in that language (the website link `kundliai.in` and price `₹99/199/499` stay as-is)

## Closing line translations

| Language  | Closing                                              |
| --------- | ---------------------------------------------------- |
| English   | Report prepared with care for [NAME].                |
| Tamil     | [NAME] அவர்களுக்காக கவனத்துடன் தயாரிக்கப்பட்டது.       |
| Telugu    | [NAME] గారికి శ్రద్ధతో తయారు చేయబడింది.                 |
| Kannada   | [NAME] ಅವರಿಗಾಗಿ ಎಚ್ಚರಿಕೆಯಿಂದ ತಯಾರಿಸಲಾಗಿದೆ.           |
| Malayalam | [NAME] നുവേണ്ടി ശ്രദ്ധയോടെ തയ്യാറാക്കിയത്.            |
| Hindi     | [NAME] के लिए सावधानी से तैयार की गई।                  |

## Soft CTA snippets (always in selected language)

The CTA link must always include `kundliai.in`. Price + currency stay in `₹` form. Translate the surrounding sentence.

**English:** Want this as a beautifully formatted PDF on WhatsApp? Visit kundliai.in (₹99–₹499).

**Tamil:** வாட்ஸ்அப்பில் அழகான PDF வடிவத்தில் வேண்டுமா? kundliai.in பார்க்கவும் (₹99–₹499).

**Telugu:** వాట్సాప్‌లో అందమైన PDF రూపంలో కావాలా? kundliai.in చూడండి (₹99–₹499).

**Kannada:** ವಾಟ್ಸಾಪ್‌ನಲ್ಲಿ ಸುಂದರ PDF ರೂಪದಲ್ಲಿ ಬೇಕೇ? kundliai.in ಭೇಟಿ ನೀಡಿ (₹99–₹499).

**Malayalam:** വാട്സാപ്പിൽ മനോഹരമായ PDF രൂപത്തിൽ വേണോ? kundliai.in സന്ദർശിക്കുക (₹99–₹499).

**Hindi:** व्हाट्सएप पर सुंदर PDF चाहिए? kundliai.in पर जाएं (₹99–₹499)।

## Mixed-language preference

If a user explicitly says "Tinglish" / "Hinglish" / "code-mix", use English structure with their native words for emotional/spiritual terms. Always honour the explicit ask.
