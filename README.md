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

### Οδηγίες Αυτοματισμού Μετάφρασης Εγγράφων

Δείτε το αποθετήριο [xxai-art/doc](https://github.com/xxai-art/doc)

Συνιστάται να εγκαταστήσετε πρώτα τα nodej, [direnv](https://direnv.net) και [bun](https://github.com/oven-sh/bun) και μετά να εκτελέσετε `direnv allow` αφού μπείτε στον κατάλογο.

Για να αποφύγω τις υπερβολικά μεγάλες αποθήκες μεταφρασμένες σε εκατοντάδες γλώσσες, δημιούργησα μια ξεχωριστή αποθήκη κωδικών για κάθε γλώσσα και δημιούργησα έναν οργανισμό για την αποθήκευση αυτής της αποθήκης

Η ρύθμιση της μεταβλητής περιβάλλοντος `GITHUB_ACCESS_TOKEN` και μετά την εκτέλεση [του create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) θα δημιουργήσει αυτόματα την αποθήκη.

Φυσικά, μπορείτε να το βάλετε και σε αποθήκη.

Αναφορά σεναρίου μετάφρασης [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Ο κώδικας σεναρίου ερμηνεύεται ως εξής:

[Το bux](https://bun.sh/docs/cli/bunx) είναι μια αντικατάσταση του npx, το οποίο είναι πιο γρήγορο. Φυσικά, αν δεν έχετε εγκατεστημένο το bun, μπορείτε να χρησιμοποιήσετε `npx` .

`bunx mdt zh` αποδίδει `.mdt` στον κατάλογο zh ως `.md` , δείτε τα 2 συνδεδεμένα αρχεία παρακάτω

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` είναι ο βασικός κώδικας για τη μετάφραση (εάν έχετε εγκαταστήσει μόνο `nodejs` , αλλά δεν είναι εγκατεστημένα `bun` και `direnv` , μπορείτε επίσης να εκτελέσετε `npx i18n` για μετάφραση).

Θα αναλύσει [το i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , η διαμόρφωση του `i18n.yml` σε αυτό το έγγραφο είναι η εξής:

```
en:
zh: ja ko en
```

Το νόημα είναι: Κινέζικη μετάφραση στα Ιαπωνικά, Κορεάτικα, Αγγλικά, Αγγλική μετάφραση σε όλες τις άλλες γλώσσες. Εάν θέλετε να υποστηρίζετε μόνο κινέζικα και αγγλικά, μπορείτε απλώς να γράψετε `zh: en` .

Το τελευταίο είναι [το gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , το οποίο εξάγει το περιεχόμενο μεταξύ του κύριου τίτλου και του πρώτου υπότιτλου του `README.md` κάθε γλώσσας για να δημιουργήσει μια καταχώρηση `README.md` . Ο κώδικας είναι πολύ απλός, μπορείτε να τον δείτε μόνοι σας.

Το Google API χρησιμοποιείται για δωρεάν μετάφραση. Εάν δεν μπορείτε να αποκτήσετε πρόσβαση στο Google, διαμορφώστε και ορίστε έναν διακομιστή μεσολάβησης, όπως:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Το σενάριο μετάφρασης θα δημιουργήσει μια προσωρινή μνήμη μετάφρασης στον κατάλογο `.i18n` , ελέγξτε το με `git status` και προσθέστε το στο αποθετήριο κώδικα για να αποφύγετε επαναλαμβανόμενες μεταφράσεις.
