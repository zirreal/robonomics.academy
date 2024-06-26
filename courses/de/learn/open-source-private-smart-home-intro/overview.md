---
title: "Einführung in Open-Source-Lösungen für private Smart Homes"
lastUpdate: Tue May 09 2023 13:56:49 GMT+0400 (Samara Standard Time)
description: Sie werden lernen, wie Sie Open-Source-Lösungen mit preiswerten Smart-Geräten integrieren können, um Ihr Smart Home privat auszurichten und nicht von Clouds abhängig zu machen.
metaOptions: [Lernen]
defaultName: Introduction to open source solution for private smart homes
---

<LessonImages src="smart-home-intro/open-source-private-smart-home-intro.png" imageClasses="mb full" />

<RoboAcademyText>
  Hallo zusammen! Heute möchte ich mit Ihnen über ein Smart Home sprechen, wann es benötigt wird, woraus es besteht und was es bieten kann.
</RoboAcademyText>

## Smart Homes: Probleme mit Heizung und Warmwasser lösen

Im Jahr 2022 zog ich nach Zypern und musste mich schnell an die Lebensbedingungen an einem neuen Ort gewöhnen. Nach Russland fällt der Unterschied in der Einstellung zur Nutzung von Energieressourcen besonders stark auf. Zum Beispiel gibt es in Zypern keine Zentralheizung. Und bis Dezember konnte man nicht daran denken. Und dann stellte sich heraus, dass die Temperatur in meinem Schlafzimmer die gleiche ist wie draußen am Fenster. Um ehrlich zu sein, ist es unangenehm, bei +10 °C zu schlafen ... brrr!

## Sparen Sie Energiekosten mit Smart Home-Überwachung

Außerdem gibt es auch keine zentrale Warmwasserversorgung. Es gibt Boiler, die auf dem Dach installiert sind und von der Sonne erwärmt werden. Aber im Winter reicht die Sonne nicht aus, um den Wassertank zu erwärmen. Die Wohnung verfügt ber einen Schalter, der das Heizelement im Tank einschaltet. Das Erste, was unpraktisch ist, ist, dass man es im Voraus einschalten muss. Eine halbe Stunde bis eine Stunde vor dem Duschen. Abends ist dieses Szenario noch akzeptabel, aber morgens wird man nie warmes Wasser haben. Zweitens kann man leicht vergessen, es auszuschalten. Das Ergebnis: ein durchgebranntes Heizelement und eine Stromrechnung.

Übrigens ist Strom hier sehr teuer, und man muss alle 2 Monate dafür bezahlen. Es ist im Moment unmöglich, den Hauptverbraucher zu bestimmen. Es wäre schön, Statistiken über die Hauptstromverbraucher wie Klimaanlage, Fußbodenheizung, Beleuchtung usw. zu haben. Mit Echtzeitdaten zum Stromverbrauch zur Hand können Sie zumindest damit beginnen zu analysieren, wofür er ausgegeben wird.

## Wesentliche Komponenten eines Smart Homes: Schalter, Sensoren und Smart Meter

Es stellt sich heraus, dass die ersten Kandidaten für Smart-Geräte verschiedene Schalter und Stromverbrauchsüberwachung sind. Als nächstes werden Sie wahrscheinlich darüber nachdenken, die Klimaanlage und die Fußbodenheizung nach einem Zeitplan oder nach Temperaturmessungen zu steuern. Das bedeutet, dass wir Temperatur- und Feuchtigkeitssensoren, Relais zur Steuerung der Fußbodenheizung und IR-Fernbedienungen für Klimaanlagen benötigen. Jedes Haus hat auch Fenster, und die Fenster haben normalerweise Vorhänge - es wäre cool, wenn die Vorhänge beim Zubettgehen automatisch fallen würden. So bilden Schalter, Sensoren und Smart Meter die Grundlage eines Smart Homes. Und dann können Sie basierend auf spezifischen Bedürfnissen träumen.

## Die richtige Smart Home-Lösung wählen: KNX vs. Sonoff vs. Xiaomi

Welche Smart Home- und Automatisierungslösungen gibt es auf dem Markt? Wir können an KNX denken, das heute eine der häufigsten Lösungen für den Einsatz in mittleren und großen Automatisierungssystemen für Wohnungen, Büros und Gewerbeimmobilien ist. Es ist seit über zwanzig Jahren auf dem Markt und wird jetzt von vielen großen Herstellern von elektrischen Geräten unterstützt. Um jedoch eine KNX-Lösung zusammenzustellen, muss viel Ingenieurarbeit geleistet werden. Die Hauptlogik wird in der Regel in einem separaten Schaltschrank zusammengebaut. Wenn dies nicht von Anfang an vorgesehen war, kann die Installation in einer bestehenden Wohnung schwierig oder überhaupt nicht möglich sein, ohne entsprechende Änderungen am Layout vorzunehmen. Darüber hinaus sind KNX-basierte Lösungen ziemlich teuer.

Ein anderer Ansatz könnte sein, Geräte von chinesischen Herstellern wie Sonoff oder Xiaomi zu kaufen. Ihr Hauptvorteil ist der Preis, die einfache Installation und Konfiguration. Jeder wird die meisten Sensoren und Geräte in seinen eigenen vier Wänden installieren können. An einigen Stellen benötigen Sie möglicherweise einen Elektriker, um beispielsweise intelligente Schalter zu installieren, aber sie werden die alten ersetzen und Sie müssen keine Änderungen am Layout der Wohnung vornehmen. Der Hersteller bietet eine einzige Anwendung zur Verwaltung der Geräte an. Sie müssen jedoch immer daran denken, dass Ihre Daten irgendwo an den Server gesendet werden und jegliche Kommunikation mit den Geräten ohne Internetverbindung unmöglich ist.


## DIY Smart Home: Aufbau eines Heimservers für volle Kontrolle

Ein weiterer Ansatz zum Aufbau eines Smart Homes basiert auf dem zweiten, d.h. auf der Verwendung verfügbarer Geräte von denselben chinesischen Herstellern, aber zusätzlich die Installation eines Heimservers in Ihrer Wohnung / Ihrem Haus, um die Clouds loszuwerden. Dies ist der Weg, den wir in unserer Smart-Home-Lösung eingeschlagen haben. In den folgenden Teilen werde ich ausführlich über den Aufbau unseres Demostands und seine Möglichkeiten sprechen.

<RoboAcademyText fWeight="500">
  Das war's fürs Erste! Im nächsten Lektion werden wir tiefer in die praktische Seite des Aufbaus eines Smart Homes eintauchen und Ihnen zeigen, wie Sie ein Smart Home Board zusammenbauen können. Bleiben Sie dran und machen Sie sich bereit, Ihren ersten Schritt in Richtung eines voll funktionsfähigen und automatisierten Zuhauses zu machen.
</RoboAcademyText>