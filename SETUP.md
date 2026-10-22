# 🚀 Οδηγίες Εγκατάστασης - Egrow Website

## Βήμα 1: Ρύθμιση PayPal

### Α) Βρείτε το PayPal Email σας

1. Πάρτε στη σελίδα [PayPal.com](https://paypal.com)
2. Συνδεθείτε στο Seller account σας
3. Πάρτε το **Business Email** (κάτω απ' το κονσόλα)

### Β) Ενημερώστε το index.html

Ανοίξτε το `index.html` και αναζητήστε τρεις φορές:
```html
<input type="hidden" name="business" value="YOUR_PAYPAL_EMAIL@example.com">
```

Αντικαταστήστε `YOUR_PAYPAL_EMAIL@example.com` με το δικό σας (πχ `seller@example.com`)

---

## Βήμα 2: Ενημέρωση URLs

Βρείτε και αντικαταστήστε στα PayPal forms:

```html
<input type="hidden" name="return" value="https://yourdomain.com/success">
<input type="hidden" name="cancel_return" value="https://yourdomain.com">
```

Με τα δικά σας URLs:
- `https://yourdomain.com` → το Vercel domain σας
- Παράδειγμα: `https://egrow.vercel.app`

---

## Βήμα 3: GitHub Setup

```bash
# 1. Δημιουργήστε νέο repo στο GitHub (egrow-website)
# 2. Clone το locally ή push τα αρχεία

git init
git add .
git commit -m "Initial commit: Egrow website with PayPal integration"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/egrow-website.git
git push -u origin main
```

---

## Βήμα 4: Vercel Deployment

### Α) Δημιουργήστε Vercel account
1. Πάρτε στη σελίδα [Vercel.com](https://vercel.com)
2. Συνδεθείτε με GitHub

### Β) Deploy το project
1. Κάντε κλικ "Add New..." → "Project"
2. Επιλέξτε το repo `egrow-website`
3. Αφήστε τις default settings
4. Κάντε κλικ "Deploy"

### Γ) Μετά το deployment
- Θα σας δώσει ένα URL όπως `https://egrow.vercel.app`
- Ενημερώστε το `return` URL στο index.html με αυτό

---

## Βήμα 5: Παραμετροποίηση Πακέτων

Ανοίξτε το `index.html` και αναζητήστε τις τιμές:

```html
<input type="hidden" name="amount" value="299">  <!-- Starter -->
<input type="hidden" name="amount" value="799">  <!-- Professional -->
<input type="hidden" name="amount" value="1999"> <!-- Enterprise -->
```

Αλλάξτε τις τιμές και τα ονόματα πακέτων όπως θέλετε.

---

## Βήμα 6: Προσθήκη περισσοτέρων Υπηρεσιών (Προαιρετικό)

Στο `index.html`, κάτω απ' τα services, προσθέστε:

```html
<div class="service-card">
    <div class="service-icon">🎯</div>
    <h3>Νέα Υπηρεσία</h3>
    <p>Περιγραφή της νέας υπηρεσίας σας...</p>
</div>
```

---

## Βήμα 7: Ενημέρωση Πληροφοριών Επικοινωνίας

Αναζητήστε στο `index.html`:

```html
<p><a href="mailto:info@egrow.gr">info@egrow.gr</a></p>
<p><a href="tel:+302101234567">+30 210 123 4567</a></p>
<p>Αθήνα, Ελλάδα</p>
```

Αντικαταστήστε με τα δικά σας στοιχεία.

---

## ✅ Δοκιμή Τοπικά

```bash
npx http-server -p 8000 -o
```

Στη συνέχεια, επισκεφτείτε `http://localhost:8000`

---

## 💳 PayPal Buttons - Πώς δουλεύουν

Κάθε πακέτο έχει ένα form με:
- **cmd**: `_xclick` (αγορά μίας φοράς)
- **business**: Το PayPal email σας
- **item_name**: Όνομα του πακέτου
- **amount**: Τιμή
- **currency_code**: EUR (Ευρώ)
- **return**: URL μετά την επιτυχή πληρωμή

Όταν κάνει κλικ το πελάτη, πηγαίνει στο PayPal, πληρώνει, και γυρίζει πίσω.

---

## 🎨 Προσαρμογή Στυλ

Στο `styles.css`, αλλάξτε τα χρώματα:

```css
:root {
    --primary-color: #0066ff;        /* Μπλε */
    --secondary-color: #00d4ff;      /* Κυανό */
    --accent: #ff006e;               /* Ροζ */
    --dark-bg: #0a0e27;              /* Σκοτεινό background */
}
```

---

## 🔐 Ασφάλεια

- Το PayPal email είναι **δημόσιο** (δεν μπορεί να κραχτεί)
- Κανένα **API key** που χρειάζεται
- Το hosting είναι δωρεάν στο Vercel

---

## 📞 Troubleshooting

### Τα PayPal buttons δεν δουλεύουν
- ✅ Ελέγξτε ότι το PayPal email είναι σωστό
- ✅ Ελέγξτε ότι το Seller account είναι ενεργό

### Δεν δουλεύει η smooth navigation
- ✅ Ανοίξτε τη console (F12) και δείτε το error
- ✅ Βεβαιωθείτε ότι το script.js φορτώνεται

### Vercel δεν διαθέτει το domain μου
- ✅ Πάρτε στα Vercel settings
- ✅ Προσθέστε custom domain

---

## 🎉 Έγινε!

Η ιστοσελίδα σας είναι έτοιμη! 🚀

**Επόμενα βήματα:**
- [ ] Ενημέρωση PayPal email
- [ ] Push στο GitHub
- [ ] Deploy στο Vercel
- [ ] Δοκιμή PayPal buttons
- [ ] Share το link! 

---

Έχετε απορίες; Τσεκάρετε το README.md για περισσότερες λεπτομέρειες.
