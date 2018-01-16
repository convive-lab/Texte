# Telegram und Signal

Ziel dieses Textes ist es, die Unterschiede zwischen [Telegram](https://telegram.org/) und [Signal](https://signal.org/), insbesondere im Hinblick auf Provatsphäre und Verschlüsselung möglichst leicht verständlich zu erklären.

## Telegram

Bei Telegram werden standardmäßig alle Nachrichten und Dateien auf dem Telegram-Server (ziemlich sicher unverschlüsselt) gespeichert.
Daraus ergeben sich folgende Funktionen, die bei Signal so nicht gehen:

* Nahtlose Synchronisation zwischen beliebig vielen Geräten pro Benutzer*in
* Ein nichts vergessendes gut durchsuchbares Archiv auch auf ganz neu angemeldeten Geräten
* Nachrichten können nach dem Versand am empfangenden Gerät geöscht oder editiert werden
* Medien und Dateien können vom lokalen Gerät gelöscht werden, können aber dann trotzdem noch vom Server abgerufen werden.
* Die Möglichkeit für Geheimdienste zentral mit-zu-lesen.

Zudem hat Telegram schöne Link Previews, einfache Bots, sogenannte "Sticker" und die allseits beliebte gut durchsuchbare GIF-Bibliothek.

Sicherheit gibt es bei Telegram nur durch die "Transportverschlüsselung", also dass der Kommunikationskanal zum Server verschlüsselt ist. Die Nachrichten an sich sind nicht verschlüsselt. (Ein "geheimer Chat" kann geöffnet werden, dann fallen die oben genannten Vorzüge weg. Leider ist aber die Schwäche der Verschlüsselung schon wissenschaftlich belegt worden.)

Telegrams Geschäftsmodell dürften wohl Kundendaten und Payment-Dienstleistungen sein bzw werden. Die Entwicklung wurde vom russischen Mark Zuckerberg, Pavel Durov angestoßen. Nach [eigenen Angaben](https://de.wikipedia.org/wiki/Telegram_Messenger#Geschichte_und_Hintergr%C3%BCnde) sind sie gemeinnützig. 

## Signal

Signal ist ausnahmslos [Ende-zu-Ende Verschlüsselt](https://de.wikipedia.org/wiki/Ende-zu-Ende-Verschl%C3%BCsselung), wobei nicht einzelnen Identitäten sondern einzelnen Geräten vertraut wird (anders als bei zb [PGP](https://de.wikipedia.org/wiki/Pretty_Good_Privacy)). Die Funktionsweise der Verschlüsselung im Detail ist deutlich ausgefeilter als alles was es sonst so gibt, wurde schon mehrfach als State-of-the-Art bezeichnet und spielt alle stückerln die man heute heute erwarten kann. 

Der Server, oder sonst wer, kann somit keine Nachrichten lesen, sondern diese nur zwischenspeichern und zustellen. Dabei muss eine Nachricht für jedes empfangende Gerät extra verschlüsselt werden (u.u mehrere pro user, desktop clients, -> in einer Gruppe ist es technisch nicht eine nachricht sondern sehr viele). Nach der Zustellung existieren diese Nachrichten nur noch auf den jeweiligen Geräten.
Bei Signal ist immer ein Smartphone (Android, iOS) das Haupt-Gerät, über das desktop clients hinzugefügt und entfernt(!) werden können.
Das ist insbesondere bei Medien nachteilig, da diese gerne den lokalen Speicher füllen und dann bei Geräten mit wenig Speicher für Probleme sorgen.
Es liegt also nahe über Signal nur Text zu versenden, und Bilder extern zu verlinken, wenn sie keinen problematischen Inhalt haben.
Wenn dein Speicher voll ist kannst du alte Nachrichten schnell und einfach löschen (Einstellungen->Unterhaltungen und Medieninhalte->Alte Nachrichten löschen). 

Signal hat (noch) keine schönen Link Previews. Ihr müsst also schreiben worum es bei einem Link geht, damit er auch angeklickt wird.

Signal unterstützt verschwindende Nachrichten. Die Nachricht bekommt also ein Ablaufdatum und das empfangende Gerät ist dafür verantwortlich, die Nachricht nach Ablauf des Datums zu löschen. So kann immerhin die menge an belastendem Material minimiert werden, sollte ein Gerät in die falschen Hände fallen.

Der lokale Speicher kann mit einem App-Passwort verschlüsselt werden, was insbesondere auf Geräten mit unverschlüsseltem Speicher, Geräten mit alter Software, aber auch generell (stichwort [Meltdown](https://de.wikipedia.org/wiki/Meltdown_(Sicherheitsl%C3%BCcke))), empfehlenswert ist. 

Signel [sendet deine Kontkte nicht(!)](https://signal.org/blog/private-contact-discovery/) an den zentralen Server.

Signal bzw. Open Whisper Systems, hat ein nachvollziehbares Geschäftsmodell, nämlich den Verkauf und die Anpassung dieses Protokolls, das trotzdem open source ist(!), zb an Facebook (Whatsapp, Messenger), Google (Allo) und Microsoft (Skype). Ob OWS gemeinnützig ist konnte ich jetzt so auf die Schnelle nicht feststellen. In der Vergangenheit haben sie sich jedenfalls [durch Spenden finanziert](https://en.wikipedia.org/wiki/Open_Whisper_Systems#Funding). 


