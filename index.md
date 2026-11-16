<!--
DRAFT for review by Obaida. Written 2026-11-15 from ADR-0014, ADR-0011 and the code of build 1.0.0+1.
NOT legal advice. It must be checked by the pilot customer or a data protection adviser before it
is published (ADR-0014). Fill in every [PLACEHOLDER] first.

What this text covers: exactly what build 1.0.0+1 (closed test) does. The block marked
"NOCH NICHT IN DIESER VERSION" describes planned features; leave it OUT of the published page until
that feature ships, then move it into the main text and update the date.

Form of address: Sie (this is the public page; ADR-0017).
Publish at a public https URL and enter that URL in Play Console (app content, privacy policy).
-->

# Datenschutzerklärung der App „Feldoro"

Stand: [DATUM]

## 1. Wer ist verantwortlich?

Anbieter der App: [Obaida Aljjarrah / Feldoro], [Meissnerstr41], [34134 Kassel], Deutschland
E-Mail: [obaidaxt@gmail.com]

Feldoro ist eine App zur Dokumentation von Arbeiten im Winterdienst. Sie wird von Unternehmen eingesetzt, deren Beschäftigte die App nutzen. Für die Daten, die ein Unternehmen mit der App über seine Beschäftigten erfasst, ist in der Regel dieses Unternehmen verantwortlich. Der Anbieter verarbeitet diese Daten dann in dessen Auftrag. [Von einem Datenschutzberater prüfen lassen: Rollenverteilung und Auftragsverarbeitungsvertrag mit dem Pilotkunden.]

## 2. Was die App erfasst

Die App erfasst nur, wann Sie an einem Objekt einen NFC-Aufkleber scannen. Zwischen den Scans wird nichts erfasst. Es gibt keine Routenaufzeichnung und keine Standortverfolgung. Die Uhrzeit jedes Scans wird gespeichert; daraus ist erkennbar, wann gearbeitet wurde.

Im Einzelnen werden folgende Daten verarbeitet:

**Konto**
- E-Mail-Adresse und Passwort für die Anmeldung. Das Konto legt das Unternehmen an; eine Selbstregistrierung gibt es nicht.
- Ihr Name, Ihre Rolle (Fahrer oder Büro) und die Zugehörigkeit zu Ihrem Unternehmen.

**Erfassungen (Scans)**
- Der Code des gescannten Aufklebers.
- Die Uhrzeit des Scans auf Ihrem Telefon und die Uhrzeit, zu der der Server ihn erhalten hat.
- Wer gescannt hat (Ihr Konto) und für welches Unternehmen.
- Ob das Telefon beim Scan eine Netzverbindung hatte (online, offline oder unbekannt) und wann das geprüft wurde. Dafür fragt die App Android, ob ein Netz aktiv ist, und öffnet eine kurze Testverbindung zum Server der App. Dabei werden keine Inhalte übertragen. Das Ergebnis ist ein Hinweis des Geräts, kein Beweis.
- Das Zuordnen eines Aufklebers zu einem Objekt (Kopplung), wenn Sie das tun.

**Einsatzstart**
- Ob und wann Sie einen Einsatz bestätigt und gestartet haben.

**Auf Ihrem Telefon**
- Noch nicht gesendete Erfassungen werden in einer Datenbank auf dem Telefon gespeichert und später übertragen. Außerdem merkt sich die App, welches Konto angemeldet war, damit eine Erfassung ohne Netz dem richtigen Konto zugeordnet werden kann. Die App legt keine Sicherung in der Cloud an.

**Navigation**
- Die Schaltfläche „Navigation" öffnet Google Maps (eine andere App) mit der Adresse des Objekts. Dabei gilt die Datenschutzerklärung von Google. Die Feldoro-App übermittelt dabei keinen Standort.

**Nicht erfasst in dieser Version:** Standort, Fotos, Kontakte, Mikrofon, Kamera, Werbe-ID. Es gibt keine Werbung, keine Analyse- und keine Absturzberichts-Dienste.

## 3. Wofür die Daten verwendet werden

- Anmeldung und Bereitstellung der App.
- Dokumentation, wann welches Objekt bearbeitet wurde, für den Nachweis gegenüber dem Kunden, zum Beispiel bei Reklamationen.
- Anzeige des Tagesstands für das Büro.

[Rechtsgrundlagen von einem Datenschutzberater festlegen lassen. Bei Beschäftigten kommen insbesondere Art. 6 Abs. 1 lit. b und f DSGVO sowie § 26 BDSG in Betracht. Bei Unternehmen mit Betriebsrat ist voraussichtlich eine Vereinbarung nötig (ADR-0014).]

## 4. Wer die Daten erhält

- Das Unternehmen, bei dem Sie beschäftigt sind (Fahrer und Büro dieses Unternehmens, nicht andere Unternehmen).
- Technischer Dienstleister: Supabase (Datenbank und Anmeldung). Die Daten liegen in einem Rechenzentrum in Frankfurt am Main. [Anbieter und Vertragsgrundlage prüfen: Auftragsverarbeitungsvertrag, Standardvertragsklauseln, Sitz des Anbieters in den USA.]
- Eine Weitergabe zu Werbezwecken oder der Verkauf von Daten findet nicht statt.

Beim Betrieb der Server können technische Verbindungsdaten wie IP-Adressen kurzzeitig in Protokollen des Hosting-Anbieters anfallen.

## 5. Wie lange die Daten gespeichert werden

[SPEICHERDAUER FESTLEGEN, zum Beispiel: Erfassungen so lange, wie das Unternehmen sie für Nachweise benötigt, höchstens [N] Jahre; Konto bis zum Ende der Nutzung durch das Unternehmen.] Erfassungen werden nicht nachträglich verändert.

## 6. Ihre Rechte

Sie haben das Recht auf Auskunft, Berichtigung, Löschung, Einschränkung der Verarbeitung, Datenübertragbarkeit und Widerspruch (Art. 15 bis 21 DSGVO). Wenden Sie sich dafür an [obaidaxt@gmail.com] oder an Ihr Unternehmen. Eine Löschung kann durch gesetzliche Aufbewahrungspflichten oder Nachweisinteressen begrenzt sein.

Sie können sich bei einer Datenschutz-Aufsichtsbehörde beschweren, zum Beispiel beim Hessischen Beauftragten für Datenschutz und Informationsfreiheit. [Zuständige Behörde prüfen.]

## 7. Änderungen

Wenn sich die App ändert, zum Beispiel durch neue Funktionen, wird diese Erklärung vorher angepasst. Der Stand steht oben.

---

<!--
NOCH NICHT IN DIESER VERSION. Do not publish until the feature is built (ADR-0011, ADR-0014).
Then move each paragraph into section 2 and update the date.

Standortprüfung (ADR-0011, ADR-0014 driver text, formal here):
"Bei jedem Scan oder jeder Erfassung per „Erledigt" wird einmal der Standort geprüft, nur solange die App geöffnet ist.
Gespeichert wird nur das Ergebnis: der Abstand zum Objekt, die Genauigkeit, die GPS-Uhrzeit und ob ein Hinweis auf einen
simulierten Standort vorlag. Koordinaten werden nicht gespeichert. Zwischen den Objekten wird nichts erfasst, und Ihre
Route wird nicht aufgezeichnet."

Fotos: "Sie können einer Erfassung ein Foto hinzufügen. Das Foto wird auf dem Server des Unternehmens gespeichert."

Benachrichtigungen: "Für „Einsatz starten" und Zusatzaufträge nutzt die App Push-Benachrichtigungen. Dafür wird ein
Dienst von Google (Firebase Cloud Messaging) genutzt und eine Geräte-Kennung übertragen." (Check: this adds a third
party and a device ID; Data Safety changes too.)
-->
