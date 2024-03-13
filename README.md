# Language-Docs
- 🇺🇸 [**English**](#english):
  - [Become a translator](#become-a-translator)
  - [File structure](#file-structure)
  - [languages.json file](#languagesjson-file)
  - [Translation and language rules](#translation-and-language-rules)
  - [Text formats](#text-formats)
- 🇩🇪 [**Deutsch (German)**](#deutsch-german):
  - [Werde Übersetzer:in](#werde-Übersetzerin)
  - [Dateistruktur](#dateistruktur)
  - [languages.json-Datei](#languagesjson-datei)
  - [Übersetzungs- und Sprachregeln](#übersetzungs--und-sprachregeln)
  - [Textformate](#textformate)

---
## English
### __Become a translator__
- __Official translator__: To become an official translator, please open a normal support ticket on our [Discord server](https://discord.skydinse.net/)! Please make sure that you meet the following requirements:
    - Interest in languages and Minecraft
    - Pass an aptitude test (general knowledge of Minecraft and Skydinse)
    - Pass a language test (AI is permitted, but must be completely correct in terms of content and language) **OR** provide a language certificate or proof of native speaker status
    - Submit correctly translated texts (task will be set after the application)
- __Unofficial translator__: If you don't want to be an official translator, you can volunteer here on GitHub and create your [own pull requests](#own-pull-requests). Your pull requests will then be checked by an official translator and adopted if they are okay.
##
### __File structure__

- **global**: Global language files are the files for systems that are globally available on the entire Skydinse network and are not limited to a specific game mode, for example. A file path for the global system "chat" would look like this: `/global/chat/lang.json`.
- **groups**: The language files in groups are the exact opposite of their global equivalents. The files of a group are only ever loaded on servers with the corresponding group (a group name can either be the first part of the server name (e.g. "lobby" for "Lobby-1") or a name defined in the server settings (e.g. "citybuild" for CBplot, CBfarm and CBend)). A file path for the "game" system from the Duels group could look like this: `/groups/duels/game/lang.json`. A file path for the system "citybuild" from the group "citybuild" would look like this: `/groups/citybuild/citybuild/lang.json` (in this case the system happens to have the same name as the group).
- Subfolders: Since many systems also have their own subordinate systems, each system can also have any number of subfolders (and subfolders of subfolders, ...). For example, the "lobbygames" system in the lobby (group "lobby") is subordinate to the "lobby" system. A file path would then look like this: `/groups/lobby/lobby/lobbygames/lang.json`.
- __Important__: all names of groups and systems are written __in lower case__!
##
### __languages.json file__

soon!
##
### __Translation and language rules__
- **AI**: AI tools (e.g. ChatGPT) for translating texts are __allowed__, but the responsibility for a correct translation always lies with the person.
- Placeholders**: Placeholders must be specified in the form `[name]`. If there are several values with the same name, these must be distinguished by `.NUMBER` (e.g. `[name.1]`, `[name.2]`, ...). Placeholder names are always in English and must not be translated. The respective placeholders specified by the developer must be adhered to. **Standard placeholders** are:
  - `[player]`: Name of a player
  - `[link]`: Link to a website
  - `[command]`: Command
  - `[message]`: Message
  - Old placeholders are often still in the form "VAR1", "VAR2", ... or "VAL1", "VAL2", ... - These must retain their form so that no problems arise.
- **Special rules for languages**:
  soon!
##
### __Text formats__

- **Hex-Colors**: Hex colors can be specified in two different formats: `#&000000` or `<#000000>`. Examples: `&#abc123`, `<#abc123>,`, `#&face05`, `<#face05>`. IMPORTANT: the color code __must__ always be __6 characters long__ (instead of "000" for black, for example, "000000" would have to be specified for black)!

- **Links**:
 - **automatic formatting**: Links can be made automatically clickable and provided with a tooltip (similar to chat) if they are specified in the format `<@LINK>` (e.g. `<@https://www.skydinse.net/>`).
 - **individual formatting**: Links can be integrated with your own tooltips and text (which can be seen in the chat). The formatting: `<@tip:'TOOLTIP',value:'LINK',text:'TEXT'>`. The value (link) is necessary, tip and text are not (there are default values).
  - Possible examples:
    - `&7You can reach our website at &e<@https://www.skydinse.net/>&7!`
    - `&7You can reach our website at &e<@tip:'&7Click here!',value:'https://www.skydinse.net/'>&7!`
    - `&7You can reach our website <@value:'https://www.skydinse.net/',text:'&ehere'>&7!`
    - `&7You are welcome to visit <@tip:'&7Click here!',value:'https://www.skydinse.net/',text:'&our website'>&7!`

- **Copyable text**: This is text that is copied to the client clipboard when it is clicked in the chat. This can be specified with the format `<$COPY_TEXT>` (a tooltip is generated automatically, the text is the text to be copied). An individual tooltip and/or display text can be used with the format `<$tip:'TOOLTIP',value:'COPY_TEXT',text:'TEXT'>`.

- **SGA and TinyText**: Text with latin characters can also be automatically converted to SGA ([Standard Galactic Alphabet or Enchanting Table Language](https://kryptografie.de/kryptografie/chiffre/standard-galactic-alphabet.htm)) and to [TinyText](https://lingojam.com/TinyTextGenerator).
  - To display __Text in SGA__ the formatting `<?TEXT>` (e.g. `<?Here is text in SGA>`) must be used (the original text is always given as the tooltip, in the Bedrock edition text is not displayed in SGA). 
  - To use __TinyText__, the formatting `<!TEXT>` (e.g. `<?Here is TinyText>`) must be used.

- **Clickable commands**:
  - __Clickable commands (chat-paste)__ are commands (possibly with arguments) which are copied into a player's chat line when clicked. These can be specified with the format `</COMMAND>` (a tooltip is generated automatically, the text is the command). An individual tooltip and/or text can be used with the format `</tip:'TOOLTIP',value:'COMMAND',text:'TEXT'>`.
  - __Clickable commands (auto-run)__ are commands (possibly with arguments) which are executed directly by the client in their transmitted form when clicked. These can be specified with the format `<\COMMAND>` (a tooltip is generated automatically, the text is the command). An individual tooltip and/or text can be used with the format `<\tip:'TOOLTIP',value:'COMMAND',text:'TEXT'>`.

- **Text with tooltip**: This formatting is useful to generally display a tooltip when hovering over text. IMPORTANT: the tooltip is not used within the formatting for links, SGA, commands and copyable text. A tooltip can be used as follows: `<+tip:'TOOLTIP',text:'TEXT'>`

---
## Deutsch (German)
### __Werde Übersetzer:in__
- __Offizielle:r Übersetzer:in__: Um offizielle:r Übersetzer:in zu werden, öffne bitte ein Support-Ticket auf unserem [Discord server](https://discord.skydinse.net/)! Bitte vergewissere dich, dass du folgenden Anforderungen erfüllst:
    - Interesse an Sprachen und an Minecraft
    - Bestehen eines Eignungstests (allgemeines Wissen über Minecraft und Skydinse)
    - Bestehen eines Sprachtests (KI ist erlaubt, muss aber inhaltlich und sprachlich komplett richtig sein) **ODER** Vorlage eines Sprachzeugnisses oder eines Nachweises einer Muttersprachlichkeit
    - Korrekt übersetzte Texte vorlegen (Aufgabe wird nach der Bewerbung gestellt)
- __Inoffizielle:r Übersetzer:in__: Falls du kein:e offizielle:r Übersetzer:in sein möchtest, kannst du dich auf freiwillig hier auf GitHub engagieren und deine [eigenen pull requests](#eigene-pull-requests) erstellen. Deine pull requests werden dann von einem:r offiziellen Übersetzer:in überprüft und übernommen, wenn sie in Ordnung sind.
##
### __Dateistruktur__

- **global**: Globale language-files sind die Dateien für Systeme, welche global auf dem gesamten Skydinse-Netzwerk verfügbar sind und sich nicht beispielsweise auf einen bestimmten Spielmodus beschränken. Ein Dateipfad für das globale System "chat" sieht dann beispielsweise wie folgt aus: `/global/chat/lang.json`.
- **groups**: Die language-files in Gruppen (groups) sind das genaue Gegenteil zu ihren globalen äquivalenten. Die files (Dateien) einer Gruppe werden immer nur auf Servern mit der entsprechenden Gruppe geladen (ein Gruppenname kann hierbei entweder der erste Teil des Servernamens (z.B. "lobby" für "Lobby-1") oder ein in den Servereinstellungen definierter Name (z.B. "citybuild" für CBplot, CBfarm und CBend) sein). Ein Dateipfad für das System "game" aus der Gruppe Duels kann dann beispielsweise so aussehen: `/groups/duels/game/lang.json`. Ein Dateipfad für das System "citybuild" aus der Gruppe "citybuild" würde so aussehen: `/groups/citybuild/citybuild/lang.json` (in diesem Fall trägt das System zufällig den selben Namen wie die Gruppe).
- Unterordner: Da viele Systeme auch über weitere, eigene untergeordnete Systeme verfügen, kann jedes System auch beliebig viele Unterordner (und Unterordner von Unterordnern, ...) haben. Das System "lobbygames" in der Lobby (Gruppe "lobby") ist beispielsweise dem System "lobby" untergeordnet. Ein Dateipfad sähe dann so aus: `/groups/lobby/lobby/lobbygames/lang.json`.
- __Wichtig__: alle Namen von Gruppen und Systemen werden __kleingeschrieben__!
##
### __languages.json-Datei__

bald!
##
### __Übersetzungs- und Sprachregeln__
- **KI**: KI-Tools (z.B. ChatGPT) zum Übersetzen von Texten sind __erlaubt__, die Verantwortung einer korrekten Übersetzung liegt aber dennoch immer bei der Person.
- **Platzhalter**: Platzhalter sind in der Form `[name]` anzugeben. Falls es mehrere Werte mit demselben Namen gibt, sind diese durch `.ZAHL` zu unterscheiden (z.B. `[name.1]`, `[name.2]`, ...). Platzhalter-Namen sind immer Englisch und dürfen nicht übersetzt werden. Es muss sich an die jeweiligen Platzhalter gehalten werden, welche von dem:r Developer:in vorgegeben sind. **Standard-Platzhalter** sind:
  - `[player]`: Name eines:r Spieler:in
  - `[link]`: Link zu einer Webseite
  - `[command]`: Befehl
  - `[message]`: Nachricht
  - Alte Platzhalter sind oft noch in der Form "VAR1", "VAR2", ... oder "VAL1", "VAL2", ... angegeben, diese müssen ihre Form beibehalten, damit keine Probleme entstehen.
- **Besondere Regeln für Sprachen**:
  bald!
##
### __Textformate__

- **Hex-Colors**: Hex-Colors können in zwei verschiedenen Formaten angegeben werden: `#&000000` oder `<#000000>`. Beispiele: `&#abc123`, `<#abc123>,`, `#&face05`, `<#face05>`. WICHTIG: der Colorcode __muss__ immer __6 Zeichen lang__ sein (statt "000" für schwarz müsste dann beispielsweise "000000" für schwarz angegeben werden)!

- **Links**:
  - **automatische Formatierung**: Links können automatisch klickbar gemacht und mit tooltip versorgt werden (ähnlich wie im Chat), wenn diese im Format `<@LINK>` (z.B. `<@https://www.skydinse.net/>`) angegeben werden.
  - **individuelle Formatierung (SOON)**: Links können mit eigenen Tooltips und eigenem Text (der im Chat zu sehen ist) eingebaut werden. Die Formatierung: `<@tip:'TOOLTIP',value:'LINK',text:'TEXT'>`. Der Wert "value" (Link) ist hier notwendig, Tip und Text nicht (es gibt Standardwerte).
  - Mögliche Beispiele:
    - `&7Unsere Webseite kannst du unter &e<@https://www.skydinse.net/> &7erreichen!`
    - `&7Unsere Webseite kannst du unter &e<@tip:'&7Klicke hier!',value:'https://www.skydinse.net/'> &7erreichen!`
    - `&7Unsere Webseite kannst du <@value:'https://www.skydinse.net/',text:'&ehier'> &7erreichen!`
    - `&7Besuche gerne <@tip:'&7Klicke hier!',value:'https://www.skydinse.net/',text:'&eunsere Webseite'>&7!`

- **Kopierbarer Text**: Hierbei handelt es sich um Text, welcher im Chat beim anklicken in die Zwischenablage des Clients kopiert wird. Dieser kann mit dem Format `<$COPY_TEXT>` angegeben werden (ein Tooltip wird automatisch erzeugt, der Text ist der zu kopierende Text). Ein indivitueller Tooltip und/oder Anzeige-Text kann mit dem Format `<$tip:'TOOLTIP',value:'COPY_TEXT',text:'TEXT'>` verwendet werden.

- **SGA und TinyText**: Text mit lateinischen Buchstaben kann auch automatisch ins SGA ([Standard Galactic Alphabet bzw. Enchanting Table Language](https://kryptografie.de/kryptografie/chiffre/standard-galactic-alphabet.htm)) und in [TinyText](https://lingojam.com/TinyTextGenerator) umgewandelt werden.
  - Um __Text im SGA__ anzuzeigen muss die Formatierung `<?TEXT>` (z.B. `<?Hier steht Text im SGA>`) verwendet werden (als Tooltip wird immer der Originaltext angegeben, in der Bedrock-Edition wird Text nicht im SGA wiedergegeben). 
  - Um __TinyText__ zu verwenden, muss die Formatierung `<!TEXT>` (z.B. `<?Hier steht TinyText>`) verwendet werden.

- **Klickbare Commands**:
  - __Klickbare Commands (chat-paste)__ sind Commands (ggf. mit Argumenten), welche beim Anklicken in die Chat-Zeile kopiert werden. Diese können mit dem Format `</COMMAND>` angegeben werden (ein Tooltip wird automatisch erzeugt, der Text ist der Command). Ein indivitueller Tooltip und/oder Text kann mit dem Format `</tip:'TOOLTIP',value:'COMMAND',text:'TEXT'>` verwendet werden.
  - __Klickbare Commands (auto-run)__ sind Commands (ggf. mit Argumenten), welche beim Anklicken direkt in ihrer übermittelten Form vom Client ausgeführt werden. Diese können mit dem Format `<\COMMAND>` angegeben werden (ein Tooltip wird automatisch erzeugt, der Text ist der Command). Ein indivitueller Tooltip und/oder Text kann mit dem Format `<\tip:'TOOLTIP',value:'COMMAND',text:'TEXT'>` verwendet werden.

- **Text mit Tooltip**: Diese Formatierung ist nützlich, um allgemein einen Tooltip beim Hovern über Text anzuzeigen. WICHTIG: der Tooltip wird nicht innerhalb der Formatierungen für Links, SGA, Commands und kopierbaren Text übernommen. Ein Tooltip kann wie folgt verwendet werden: `<+tip:'TOOLTIP',text:'TEXT'>`.
