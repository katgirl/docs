# Simple Tokens

Simple Tokens ist womöglich eines der meistunterschätzten Features innerhalb von Contao und wird im Kern von Contao leider auch nur für das Newsletter-Modul verwendet.

Simple Tokens werden deshalb [in der offiziellen Dokumentation][1] auch nur kurz angerissen.

In Isotope eCommerce werden die Tokens oft verwendet, weil sie dir viel Flexibilität geben.
Sie werden unter anderem hier verwendet:

* Im gesamten <docrobot_route name="notifications">Benachrichtigungszentrum</docrobot_route>
* Für die Darstellung der Adressen der verschiedenen Länder (bspw. PLZ vor oder nach Ort etc.)
* In den <docrobot_route name="documents">Dokumenten</docrobot_route>, um den Dokumententitel sowie den Dokumenten-Dateinamen zu individualisieren

Simple Tokens unterstützen im Gegensatz zu Inserttags auch einfache If-Else-Abfragen wodurch z.B. in Bestellbestätigungs-E-Mails auch sowas möglich wäre:

<pre>
{if billing_gender=="male"}
Sehr geehrter Herr ##billing_lastname##,
{elseif billing_gender=="female"}
Sehr geehrte Frau ##billing_lastname##,
{else}
Sehr geehrte Damen und Herren,
{endif}
</pre>

Es gibt zwei Arten von Simple Tokens in Isotope eCommerce:
* PLAIN-Text Tokens
* HTML-Text Tokens

## HTML-Text Tokens
Diese sind die Standard-Tokens die verwendet werden. Die jeweis möglichen Token erhält man als Auswahl, wenn man ## eingibt
[image:simple_tokens_select.png]


## PLAIN-Text Tokens
Diese sollten verwendet werden z.B. wenn man PLAIN-E-Mails versenden möchte, da hier die Zeilumbrüche <br> durch \n ersetzt sind und sonstige HTML-Zeichen entfernt.
Diese Tokens kann man wie die HTML-Text Token aus dem Auswahlmenü wählen, man erkennt sie an _text am Ende.

[1]: https://contao.org/de/manual/3.2/managing-content.html#newsletter-personalisieren
