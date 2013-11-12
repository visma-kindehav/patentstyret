**********************************************
******************    README    **************
**********************************************

=====================
=== Mappestruktur ===
=====================

./android			Android spesifik kode
./iphone			iOS spesifik kode
./wp8				Windows Phone 8 spesifik kode
./www				All html for PhoneGap 

./www/css			Inneholder all styling til applkasjonen
./www/img			Bilder brukt i applikasjonen
./www/lib			Biblioteker benyttet i applikasjonen
						* Analytics biblioteket er endret for å støtte PhoneGap (Fjernet protokoll sjekk)
./www/localization	Inneholder språkfiler for oversettelser
./www/res			PhoneGap spesifikk mappe (resources)
./www/spec			PhoneGap spesifikke biblioteker
./www/Visma			JavaScript kode for prosjektet

./www/Visma/Core			Kjernefunksjonalitet for applikasjonen
./www/Visma/Integration		Inneholder funksjonalitet for integrering av eksterne systemer
./www/Visma/Lookup			Søkefunksjonalitet og støtteklasser for disse
./www/Visma/Screens			Skjermbildene i applikasjonen
./www/Visma/Tabs			Kode for håndtering av tabs


=======================
=== Ripple Emulator ===
=======================

Plugin til Chrome hvor man kan kjøre PhoneGap i browser

*	Lag en ny snarvei til Chrome
*	Høyreklikk -> Properties
* 	Legg til " --allow-file-access-from-files --disable-web-security" etter program path i target felter.
*	Eks: "C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" --allow-file-access-from-files --disable-web-security
*	Skriv inn chrome://extensions
*	Under Ripple extension, huk av for "Allow Acces to File URLs"


============================
=== Installasjon Android ===
============================

*	Importer prosjektet i IntelliJ
*	Legg til symlinks fra PROJECT_HOME/android/assets/www og PROJECT_HOME/ios/www til PROJECT_HOME/www.
*		Du må ikke ha opprettet www mappen tidligere.

**		(Android) 	mklink /D PROJECT_HOME\www PROJECT_HOME\android\assets\www\
**		(iOs) 		ls -s PROJECT_HOME/ios/www PROJECT_HOME/www


=====================================
== Konfigurasjon av applikasjonen ===
=====================================

*	Endre API endpoints
		Konfigurasjon av globale variabler ligger i ./www/Visma/Core/Globals.js
		Her kan adresse av Patentstyrets- og eksterne APIer endres.
