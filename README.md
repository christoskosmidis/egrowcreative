# Egrow - Ιστοσελίδες & eShop Services

Σύγχρονη, minimal ιστοσελίδα για την πώληση υπηρεσιών ιστοσελίδων και eShop με PayPal integration.

## 🚀 Χαρακτηριστικά

- ✨ **Σύγχρονα εφέ**: Gradient blobs, smooth animations, hover effects
- 📱 **Responsive Design**: Λειτουργεί τέλεια σε όλες τις συσκευές
- 💳 **PayPal Integration**: Ενσωματωμένα PayPal buttons για κάθε πακέτο
- 🎨 **Minimal & Clean**: Κατηγορίες υπηρεσιών, πακέτα με τιμές
- ⚡ **Lightweight**: Καμία εξάρτηση, pure HTML/CSS/JavaScript
- 🔍 **SEO Ready**: Σωστή δομή HTML

## 📋 Δομή

```
├── index.html      # Main page
├── styles.css      # Styling με animations
├── script.js       # JavaScript interactivity
├── package.json    # Project metadata
└── README.md       # Αυτό το αρχείο
```

## ⚙️ Ρύθμιση

### 1. Ενημέρωση PayPal Email
Ανοίξτε το `index.html` και αντικαταστήστε τα εξής με το δικό σας PayPal email:

```html
<input type="hidden" name="business" value="YOUR_PAYPAL_EMAIL@example.com">
```

### 2. Ενημέρωση Return URLs
Αντικαταστήστε τα URLs στα PayPal forms:

```html
<input type="hidden" name="return" value="https://yourdomain.com/success">
<input type="hidden" name="cancel_return" value="https://yourdomain.com">
```

### 3. Ενημέρωση Πληροφοριών Επικοινωνίας
Ενημερώστε το email και το τηλέφωνό σας στο τμήμα Contact.

## 🚀 Ανάπτυξη

### Τοπικά
```bash
# Εγκατάσταση http-server (προαιρετικό)
npm install -g http-server

# Εκκίνηση
npx http-server -p 8000 -o
```

Στη συνέχεια, επισκεφτείτε `http://localhost:8000`

### Στο GitHub
```bash
git init
git add .
git commit -m "Initial commit: Egrow website"
git branch -M main
git remote add origin https://github.com/yourusername/egrow-website.git
git push -u origin main
```

### Στο Vercel
1. Πάρτε τον κώδικα από το GitHub
2. Συνδέστε το repo στο [Vercel](https://vercel.com)
3. Vercel θα κάνει auto-deploy σε κάθε push
4. Αποκτήστε δικό σας domain (πχ. egrow.vercel.app → custom domain)

## 🎨 Παραμετροποίηση Χρωμάτων

Στο `styles.css`, βρείτε τις CSS variables:

```css
:root {
    --primary-color: #0066ff;        /* Μπλε */
    --secondary-color: #00d4ff;      /* Κυανό */
    --accent: #ff006e;               /* Ροζ */
    --dark-bg: #0a0e27;              /* Σκοτεινό background */
}
```

## 📦 Πακέτα

- **Starter (€299)**: Ιστοσελίδα 5 σελίδων
- **Professional (€799)**: 10 σελίδες + eShop 20 προϊόντα (Δημοφιλές)
- **Enterprise (€1999)**: Unlimited σελίδες + πλήρες eShop

## 🔧 PayPal IPN (Ανταρκτική)

Για automated emails/notifications μετά την πληρωμή:
1. Πάρτε IPN URL από το Vercel
2. Ενημερώστε το PayPal account settings → IPN

## 📞 Support

- Email: info@egrow.gr
- Phone: +30 210 123 4567

---

**Δημιουργήθηκε με ❤️ για την Egrow**
