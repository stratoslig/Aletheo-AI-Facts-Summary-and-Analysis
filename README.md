# Aletheo: Σύνοψη & Ανάλυση Γεγονότων με AI

![Version](https://img.shields.io/badge/version-1.2.2-blue.svg)
![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![UI Framework](https://img.shields.io/badge/UI-CustomTkinter-blueviolet.svg)

*[🇬🇧 Read this in English](#aletheo-facts-summary-and-analysis-ai)*

Μια ισχυρή Desktop εφαρμογή (χτισμένη με Python & CustomTkinter) που αυτοματοποιεί την αναζήτηση, το φιλτράρισμα και την ανάλυση ειδήσεων. Λειτουργεί ως ένας προηγμένος ελεγκτής γεγονότων και συλλέκτης ειδήσεων με την ισχύ της Τεχνητής Νοημοσύνης.

Το Aletheo συλλέγει δεδομένα από πολλαπλές πηγές (RSS Feeds, URLs, GNews, Mediastack, NewsData.io), επιτρέπει στον χρήστη να επιμεληθεί τα πιο σχετικά άρθρα, και αξιοποιεί την Τεχνητή Νοημοσύνη (μοντέλα Cloud ή Τοπικά) για να εξάγει γεγονότα, να τα επικυρώνει και να παρέχει στοχευμένη ανάλυση.

## 🆕 Τι νέο υπάρχει στην έκδοση 1.2.2
- **Κριτήριο Αληθοφάνειας:** Η Εκτίμηση Εγκυρότητας και η Εκτίμηση Ιστοσελίδας αξιολογούν πλέον την αληθοφάνεια των ισχυρισμών, μειώνοντας δραστικά τη βαθμολογία σε θεωρίες συνωμοσίας και παράλογα άρθρα.
- **Απομόνωση Fake News:** Ειδήσεις με εγκυρότητα κάτω του 40% απομονώνονται ως ανεξάρτητα γεγονότα και αγνοούνται εντελώς από το AI κατά την παραγωγή της τελικής Σύνοψης.
- **Οπτική Επισήμανση:** Ειδήσεις με βαθμολογία κάτω του 30% χρωματίζονται πλέον αυτόματα κόκκινες στην εφαρμογή αλλά και στις τελικές εξαγωγές Word/PDF!
- **Βελτιώσεις:** Η προεπιλεγμένη αξιοπιστία νέων πηγών ορίστηκε στο 10 (μέγιστο) και αφαιρέθηκε η επιλογή της αυτόματης διασταύρωσης για ένα πιο καθαρό UI.

## � Κύρια Χαρακτηριστικά

- **Συλλογή από Πολλαπλές Πηγές**: Αντλήστε ειδήσεις από απλά URLs (μέσω Web Scraping), RSS feeds, και 3 διαφορετικά News APIs (GNews, Mediastack, NewsData.io).
- **Προηγμένο Φιλτράρισμα**: Φιλτράρετε άρθρα τοπικά ανά Κατηγορία, Γλώσσα (με ευρετική ανίχνευση κειμένου), Χώρα, Ημερομηνία, και Λέξεις-κλειδιά (χρησιμοποιώντας `+` για ΥΠΟΧΡΕΩΤΙΚΑ, `-` για ΟΧΙ, και `,` για Ή).
- **Διπλή Υποστήριξη AI**: Χρησιμοποιήστε το Gemini API της Google (Cloud) για κορυφαία αποτελέσματα, ή το Ollama για τοπική εκτέλεση με έμφαση στην ιδιωτικότητα και offline λειτουργία.
- **Μηχανισμός Fact-Checking**: Το AI ομαδοποιεί τις ειδήσεις, αφαιρεί την προκατάληψη, και παράγει μια **σταθμισμένη Εκτίμηση Εγκυρότητας (1-100%)** βασισμένη σε 6 κριτήρια: Διασταύρωση, Τεκμηρίωση, Ουδετερότητα, Λογική Συνοχή, Αυθεντία Πηγής και Αληθοφάνεια. Περιλαμβάνει μηχανισμό «Βέτο» για προστασία από clickbaits.
- **Εκτίμηση Ιστοσελίδας**: Αξιολογήστε τη συνολική αξιοπιστία μίας πηγής ελέγχοντας πολλαπλά άρθρα της για Τεκμηρίωση, Ουδετερότητα, Λογική Συνοχή και Αληθοφάνεια, παράγοντας μια τελική ποσοστιαία βαθμολογία (1-100%).
- **Απομόνωση Fake News**: Τα γεγονότα με Εκτίμηση Εγκυρότητας κάτω του 40% απομονώνονται, ενώ κάτω του 30% επισημαίνονται με κόκκινο χρώμα (και στις εξαγωγές). Η Σύνοψη τα αγνοεί αυτόματα.
- **Βαθμολόγηση Αξιοπιστίας**: Αναθέστε τη δική σας "Βαθμολογία Αξιοπιστίας" σε κάθε RSS feed που προσθέτετε, την οποία το AI λαμβάνει αυτόματα υπόψη στην τελική του Εκτίμηση Εγκυρότητας.
- **Εισαγωγή & Εξαγωγή OPML**: Εισάγετε και εξάγετε εύκολα τις πηγές σας από/προς άλλους RSS readers (π.χ. Feedly) με το πάτημα ενός κουμπιού.
- **Ιστορικό (History)**: Αυτόματη τοπική αποθήκευση των 5 τελευταίων αναλύσεων με δυνατότητα ανάκτησης (φόρτωσης) και διαγραφής.
- **Δυναμικό UI**: Ένα μοντέρνο, καθαρό και πλήρως αποκριτικό περιβάλλον χρήστη με CustomTkinter που διαθέτει:
  - Light/Dark mode support.
  - Collapsible panels for a tidy workspace.
  - **Drag-and-Drop** υποστήριξη για την ταξινόμηση της λίστας πηγών.
  - **Σελιδοποίηση (Pagination)**: Προβολή 20 άρθρων ανά σελίδα για ταχύτατη πλοήγηση χωρίς καθυστερήσεις.
  - **List & Card Views** for news results, including image thumbnails.
  - Ελαφριές 3D σκιές (Drop shadows) στις κάρτες.
  - Διαδραστικά textboxes με **Clickable Links**, παραπομπές και υποστήριξη Bold κειμένου.
- **Τοπική Προβολή (Reader Mode)**: Διαβάστε το πλήρες κείμενο οποιουδήποτε άρθρου κατευθείαν μέσα από την εφαρμογή, χωρίς να ανοίγετε τον browser.
- **Ακυρώσιμες Εργασίες AI**: Ένα ειδικό κουμπί "Ακύρωση" για να σταματάτε τις χρονοβόρες διαδικασίες του AI.
- **Παραμετροποιήσιμη Έξοδος**: Ορίστε τα δικά σας όρια χαρακτήρων για τα Γεγονότα, την Ανάλυση, τη Σύνοψη και το Web Scraping ανά άρθρο. 
- **Ανατροφοδότηση σε Πραγματικό Χρόνο**: Ένας ζωντανός μετρητής δείχνει πόσα άρθρα έχουν επιλεγεί και το συνολικό πλήθος λέξεων που αποστέλλονται στο AI.
- **Πλούσιες Επιλογές Εξαγωγής**: Εξάγετε άμεσα τα επιμελημένα γεγονότα, την ανάλυση ή τις συνόψεις σας σε **Word (.docx)**, **PDF (.pdf)**, ή απευθείας στον εκτυπωτή σας. Οι εξαγωγές διατηρούν τα Clickable links και τις παραπομπές.

## 🛠️ Απαιτήσεις Εγκατάστασης

1. **Python 3.8+**
2. Κλωνοποιήστε το αποθετήριο:
   ```bash
   git clone https://github.com/stratoslig/Aletheo-Facts-Summary-and-Analysis-AI.git
   cd Aletheo-Facts-Summary-and-Analysis-AI
   ```
3. Εγκαταστήστε τις απαιτούμενες εξαρτήσεις:
   ```bash
   pip install -r requirements.txt
   ```
   *(Βεβαιωθείτε ότι έχετε εγκαταστήσει βιβλιοθήκες όπως `customtkinter`, `google-genai`, `ollama`, `feedparser`, `cloudscraper`, `beautifulsoup4`, `python-docx`, `reportlab`, `pillow`).*

## 🚀 Γρήγορη Εκκίνηση

1. Τρέξτε την εφαρμογή:
   ```bash
   python appFSA.py
   ```
2. **Ρυθμίστε τα API Keys σας**: Ανοίξτε την αριστερή πλαϊνή μπάρα και εισάγετε το Gemini API key σας (ή αλλάξτε σε Ollama αν το έχετε εγκαταστήσει τοπικά). Μπορείτε επίσης να προσθέσετε δωρεάν API keys για τα GNews, Mediastack, και NewsData.io. Κάντε κλικ στο **Αποθήκευση Κλειδιών**.
3. **Προσθέστε Πηγές**: Προσθέστε μερικά RSS feeds ή απλά URLs ειδήσεων στην πλαϊνή μπάρα. Αναθέστε τους μια κατηγορία και μια Βαθμολογία Αξιοπιστίας.
4. **Αναζήτηση**: Χρησιμοποιήστε το πάνελ "Επιλογή Πηγών" (πάνω αριστερά) για να φιλτράρετε με βάση το επιθυμητό θέμα και κάντε κλικ στο "Αναζήτηση".
5. **Επιλογή**: Τσεκάρετε τα κουτάκια δίπλα στα άρθρα που σας ενδιαφέρουν στο δεξί πάνελ.
6. **Ανάλυση**: Στο κάτω πάνελ, επιλέξτε σε πόσα θέματα θέλετε να ομαδοποιηθούν, επιλέξτε την εργασία (π.χ., Γεγονότα και Ανάλυση), και πατήστε **Έναρξη**.
7. **Ιστορικό & Εξαγωγή**: Χρησιμοποιήστε το κουμπί του Ιστορικού (κάτω δεξιά) για να ανακαλέσετε παλαιότερες αναλύσεις ή τα κουμπιά εξαγωγής για να αποθηκεύσετε το αποτέλεσμα του AI σε PDF/Word!

## 🌍 Υποστηριζόμενες Γλώσσες
Το περιβάλλον χρήστη και η μηχανή δημιουργίας Prompts υποστηρίζουν πλήρως **Αγγλικά** και **Ελληνικά**. Η λογική μετάφρασης μπορεί εύκολα να επεκταθεί στο `translations.py`.

## 📸 Στιγμιότυπα Οθόνης

*Κύριο παράθυρο εφαρμογής σε Dark Mode, που δείχνει την προβολή καρτών για τα αποτελέσματα των ειδήσεων.*
![Main Window](assets/s01.png)
![Window](assets/s02.png)
![RSS Feeds](assets/s03.png)
*Το πάνελ αποτελεσμάτων με τα παραγόμενα γεγονότα και την ανάλυση.*
![Results Panel](assets/s04.png)

## 📝 Βιβλιοθήκες που Χρησιμοποιήθηκαν
- **CustomTkinter**: Μοντέρνο GUI.
- **Trafilatura & BeautifulSoup**: Ισχυρό Web Scraping.
- **Python-docx & ReportLab**: Δημιουργία εγγράφων.
- **Feedparser**: Ανάλυση RSS.
- **Google-GenAI & Ollama**: Επεξεργασία AI.

## 📜 Άδεια Χρήσης
Αυτό το έργο αδειοδοτείται υπό την Άδεια MIT - δείτε το αρχείο LICENSE για λεπτομέρειες.

## ⚖️ Νομική Σημείωση & Αποποίηση Ευθύνης

Η εφαρμογή Aletheo χρησιμοποιεί τεχνικές web scraping για την άντληση περιεχομένου από ιστοσελίδες. Ο χρήστης φέρει την αποκλειστική ευθύνη να βεβαιώνεται ότι οι ιστοσελίδες που προσθέτει στη Watchlist επιτρέπουν την εξαγωγή και επεξεργασία των πληροφοριών τους. Συνιστάται ο έλεγχος του αρχείου robots.txt και των Όρων Χρήσης (Terms of Service) κάθε πηγής πριν από τη χρήση. Ο δημιουργός της εφαρμογής δεν φέρει καμία ευθύνη για τυχόν ακατάλληλη ή μη εξουσιοδοτημένη χρήση του περιεχομένου τρίτων.

---

# Aletheo: Facts Summary and Analysis AI

*[🇬🇷 Διαβάστε το στα Ελληνικά](#aletheo-σύνοψη--ανάλυση-γεγονότων-με-ai)*

A powerful Desktop application (built with Python & CustomTkinter) that automates the search, filtering, and analysis of news. It acts as an advanced AI-powered fact-checker and aggregator.

Aletheo gathers data from multiple sources (RSS Feeds, URLs, GNews, Mediastack, NewsData.io), allows the user to curate the most relevant articles, and leverages Artificial Intelligence (Cloud or Local models) to extract facts, validate them, and provide targeted analysis.

## 🆕 What's new in version 1.2.2
- **Plausibility Criterion:** The Validity Estimate and Website Evaluation now assess the plausibility of claims, drastically reducing scores for conspiracy theories and absurd articles.
- **Fake News Isolation:** News with validity below 40% are isolated as independent facts and completely ignored by the AI during the final Summary generation.
- **Visual Highlighting:** News with a score below 30% are automatically colored red in the app as well as in the final Word/PDF exports!
- **Tweaks:** Default trust score for new sources is set to 10 (maximum), and the redundant automated cross-check feature was removed for a cleaner UI.

## 🌟 Key Features

- **Multi-Source Aggregation**: Fetch news from raw URLs (via Web Scraping), RSS feeds, and 3 distinct News APIs (GNews, Mediastack, NewsData.io).
- **Advanced Filtering**: Filter articles locally by Category, Language (with heuristic text detection), Country, Date, and Keywords (using `+` for MUST, `-` for NOT, and `,` for OR).
- **Dual AI Support**: Use Google's Gemini API (Cloud) for top-tier results, or Ollama for local, privacy-first, offline execution.
- **Fact-Checking Engine**: The AI groups the news, strips out bias, and generates a **weighted Validity Estimate (1-100%)** based on 6 criteria: Cross-referencing, Documentation, Neutrality, Logical Consistency, Source Authority, and Plausibility. Includes a 'Veto' mechanism against clickbaits.
- **Website Evaluation**: Assess the overall reliability of a specific source by analyzing multiple articles from it for Documentation, Neutrality, Logical Coherence, and Plausibility, generating a final percentage score (1-100%).
- **Fake News Isolation**: Facts with a Validity Estimate below 40% are isolated, and below 30% are highlighted in red (including exports). The Summary automatically ignores them.
- **Trust Scoring**: Assign your own custom "Trust Score" to each RSS feed you add, which the AI automatically factors into its final Validity Estimate.
- **OPML Import & Export**: Easily import and export your source feeds from/to other RSS readers (e.g., Feedly) with a single click.
- **History System**: Automatic local storage of the last 5 analyses with retrieval and deletion capabilities.
- **Dynamic UI**: A modern, clean, and fully responsive User Interface using CustomTkinter with:
  - Light/Dark mode support.
  - Collapsible panels for a tidy workspace.
  - **Drag-and-Drop** support for sorting your RSS sources list.
  - **Pagination System**: Fast navigation with 20 articles per page for zero lag.
  - **List & Card Views** for news results, including image thumbnails.
  - Flat drop shadows on news cards for better aesthetics.
  - Interactive textboxes with **Clickable Links**, citations, and true Bold text rendering.
- **Local Article View (Reader Mode)**: Read the full text of any article directly within the application, without opening a web browser.
- **Cancellable AI Tasks**: A dedicated "Cancel" button to stop long-running AI processes.
- **Configurable Output**: Set your own character limits for Facts, Analysis, Summary, and Web Scraping per article.
- **Real-time Feedback**: A live counter shows how many articles are selected and the total word count being sent to the AI.
- **Rich Export Options**: Instantly export your curated facts, analysis, or summaries to **Word (.docx)**, **PDF (.pdf)**, or directly to your printer. Exports retain Clickable hyperlinks and citations.

## 🛠️ Installation Requirements

1. **Python 3.8+**
2. Clone the repository:
   ```bash
   git clone https://github.com/stratoslig/Aletheo-Facts-Summary-and-Analysis-AI.git
   cd Aletheo-Facts-Summary-and-Analysis-AI
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   *(Ensure you have libraries like `customtkinter`, `google-genai`, `ollama`, `feedparser`, `cloudscraper`, `beautifulsoup4`, `python-docx`, `reportlab`, `pillow` installed).*

## 🚀 Quick Start

1. Run the application:
   ```bash
   python appFSA.py
   ```
2. **Setup your API Keys**: Open the left sidebar and enter your Gemini API key (or switch to Ollama if installed locally). You can also add free API keys for GNews, Mediastack, and NewsData.io. Click **Save Keys**.
3. **Add Sources**: Add some RSS feeds or regular News URLs in the sidebar. Assign them a category and a Trust Score.
4. **Search**: Use the "Source Selection" panel (top-left) to filter by your desired topic and click "Search".
5. **Select**: Check the boxes next to the articles you find interesting in the right panel.
6. **Analyze**: In the bottom panel, choose how many topics you want to group them into, select the task (e.g., Facts and Analysis), and hit **Start**.
7. **History & Export**: Use the History button (bottom right) to recall older analyses or the export buttons to save the AI's output to PDF/Word!

## 🌍 Languages Supported
The User Interface and AI Prompting Engine fully support **English** and **Greek** out of the box. The translation logic can be easily extended in `translations.py`.

## 📸 Screenshots

*Main application window in Dark Mode, showing the card view for news results.*
![Main Window](assets/se01.png)
![Window](assets/se02.png)

*The results panel with generated facts and analysis.*
![Results Panel](assets/se03.png)

## 📝 Libraries Used
- **CustomTkinter**: Modern GUI.
- **Trafilatura & BeautifulSoup**: Robust Web Scraping.
- **Python-docx & ReportLab**: Document generation.
- **Feedparser**: RSS Parsing.
- **Google-GenAI & Ollama**: AI Processing.

## 📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

## ⚖️ Legal Disclaimer

Aletheo utilizes web scraping techniques to fetch content from websites. It is the user's sole responsibility to ensure that the websites added to the Watchlist allow data extraction and processing. We recommend checking the robots.txt file and the Terms of Service of each source before use. The developer of this application bears no responsibility for any improper or unauthorized use of third-party content.
