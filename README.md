<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Μέρος του κώδικα του ιστότοπου είναι ανοιχτού κώδικα, ευπρόσδεκτο να βοηθήσει στη βελτιστοποίηση της μετάφρασης.

## κωδικός διεπαφής

* [κωδικός διεπαφής](https://github.com/xxai-art/web)
* [Πακέτα γλωσσών για τον ιστότοπο ως σύνολο](https://github.com/xxai-art/web/tree/main/i18n)
* [Πακέτα γλωσσών για ενότητες σύνδεσης](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Ιστοσελίδα Πολυγλωσσική Τεκμηρίωση](https://github.com/xxai-doc)

Η διεπαφής γλώσσα προγραμματισμού είναι [η @w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , η οποία προσθέτει ορισμένες δυνατότητες που βασίζονται στη σύνταξη του coffeescript, βλ [. ./coffee_plus.md](./coffee_plus.md) .

## Διεθνοποίηση ιστοσελίδων και εγγράφων

Βασιστείτε στα ακόλουθα 3 έργα

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Το επίθημα είναι `.mdt` , μπορείτε να χρησιμοποιήσετε τη σύνταξη παρόμοια με το `<+ ./coffee_plus/import.js>` για να αναφερθείτε σε εξωτερικά αρχεία και να δημιουργήσετε σημάδια με το επίθημα `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Η μετάφραση Markdown δεν θα μεταφράζει κώδικες και συνδέσμους και θα αποθηκεύει προσωρινά μεταφρασμένες προτάσεις. Εάν η μετάφραση τροποποιηθεί αλλά το αρχικό κείμενο δεν τροποποιηθεί, η εκ νέου εκτέλεσή της δεν θα αντικαταστήσει την τροποποίηση της μετάφρασης.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Αρχεία γλώσσας για τη μετάφραση ιστότοπων που δημιουργούνται από `yaml` .
