#Telegram und Signal

Ziel dieses Textes ist es, die Unterschiede zwischen Telegram und Signal, insbesondere im Hinblick auf Provatsphäre und Verschlüsselung möglichst leicht verständlich zu erklären.

##Telegram

Bei Telegram werden standardmäßig alle Nachrichten und Dateien auf dem Telegram-Server (ziemlich sicher unverschlüsselt) gespeichert.
Daraus ergeben sich folgende Funktionen, die bei Signal so nicht gehen:

* Nahtlose Synchronisation zwischen beliebig vielen Geräten pro Benutzer*in
* Ein nichts vergessendes gut durchsuchbares Archiv auch auf ganz neu angemeldeten Geräten
* Die Möglichkeit Nachrichten nach Versand am empfangenden Gerät zu löschen oder zu Editieren
* Die Möglichkeit, Medien und Dateien vom lokalen Gerät zu löschen, aber trotzdem noch abrufen zu können.
* Die Möglichkeit für Geheimdienste zentral mit-zu-lesen.

Zudem hat Telegram schöne Link Previews, einfache Bots, sogenannte "sticker" und die allseits beliebte gut durchsuchbare GIF-Bibliothek.

Sicherheit gibt es bei Telegram nur durch die "Transportverschlüsselung", also dass der Kommunikationskanal zum Server verschlüsselt ist. Die Nachrichten an sich sind nicht verschlüsselt. (Ein "geheimer Chat" kann geöffnet werden, dann fallen die oben genannten Vorzüge weg. Leider ist aber die Schwäche der Verschlüsselung schon wissenschaftlich belegt worden.)

Telegrams Geschäftsmodell dürften wohl Kundendaten und Payment-Dienstleistungen sein bzw werden. Die Entwicklung wurde vom russischen Mark Zuckerberg, Pavel Durov angestoßen. Nach eigenen Angaben sind sie gemeinnützig, es ist aber eine normale Personengesellschaft. https://de.wikipedia.org/wiki/Telegram_Messenger#Geschichte_und_Hintergr%C3%BCnde 

##Signal

Signal ist ausnahmslos Ende-zu-Ende Verschlüsselt, wobei nicht einzelnen Identitäten sondern einzelnen Geräten vertraut wird (anders als bei zb PGP). Die Funktionsweise der Verschlüsselung im Detail ist deutlich ausgefeilter als alles was es sonst so gibt, wurde schon mehrfach als State-of-the-Art bezeichnet und spielt alle stückerln die man heute heute erwarten kann. 

Der Server, oder sonst wer, kann somit keine Nachrichten lesen, sondern diese nur zwischenspeichern und zustellen. Dabei muss eine Nachricht für jedes empfangende Gerät extra verschlüsselt werden (u.u mehrere pro user, desktop clients, -> in einer Gruppe ist es technisch nicht eine nachricht sondern sehr viele). Nach der Zustellung existieren diese Nachrichten nur noch auf den jeweiligen Geräten.
Bei Signal ist immer ein Smartphone (Android, iOS) das Haupt-Gerät, über das desktop clients (Chrome App [0]) hinzugefügt und entfernt(!) werden können.
Das ist insbesondere bei Medien nachteilig, da diese gerne den lokalen Speicher füllen und dann bei Geräten mit wenig Speicher für Probleme sorgen.
Insoferne würde ich dafür plädieren über Signal nur Text zu versenden, und Bilder extern zu verlinken, wenn sie keinen problematischen Inhalt haben..

Signal hat (noch) keine schönen link-previews. Ihr müsst also schreiben worum es bei einem Link geht, damit er auch angeclickt wird.

Signal unterstützt verschwindende Nachrichten, wobei diese meiner Einschätzung nach nicht tief in die Verschlüsselung integriert sind (das gibts glaube ich aber nirgends). Die Nachricht bekommt also ein Ablaufdatum und das empfangende Gerät ist dafür verantwortlich, die Nachricht nach Ablauf des Datums zu löschen. So kann immerhin die menge an belastendem Material minimiert werden, sollte ein Gerät in die falschen Hände fallen.

Der lokale Speicher kann mit einem App-Passwort verschlüsselt werden, was insbesondere auf Geräten mit unverschlüsseltem Speicher, Geräten mit alter Software, aber auch generell (stichwort Meltdown), empfehlenswert ist. 

Signal bzw Open Whisper Systems, hat ein nachvollziehbares Geschäftsmodell, nämlich den Verkauf und die Anpassung dieses Protokolls, das trotzdem open source ist(!), zb an Facebook (Whatsapp) und Microsoft (Skype). Ob OWS gemeinnützig ist konnte ich jetzt so auf die Schnelle nicht feststellen. In der Vergangenheit haben sie sich jedenfalls durch Spenden finanziert. https://en.wikipedia.org/wiki/Open_Whisper_Systems#Funding

[0] Warum Chrome? Der hat leider als einziger Browser ein wirklich gutes Sandboxing. Das heißt, dass es kaum möglich ist, auf die Daten einer in Chrome geöffneten Website oder App unberechtigt zuzugreifen. Bei Firefox wird dieser Angriff regelmäßig demonstriert (eine geöffnete Website liest die Daten einer anderen geöffneten Website aus). Ich vermute das hat bei der Entscheidung mitgespielt.
Android und iOS Betreiben auch so ein Sandboxing. Wobei es für die jeweiligen alten Versionen viele Schwachstellen gibt die ausgenützt werden können.


