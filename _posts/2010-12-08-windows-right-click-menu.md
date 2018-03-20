---
layout: post
title:  "Dodavanje aplikacija u Windows Desktop Right-Click Menu"
date:   2010-12-08 15:53:34 +0200
categories: arhiva
author: Edin Cenanovic
---
Ako želite brz pristup aplikacijama koje često koristite a da iste nisu u obliku ikona na Desktopu, možete aplikacije dodadi meniju koji aktivirate desnim klikom miša s jednostavnim 'registry hackom'. Evo kako ćete to učiniti.

<img src="/assets/windows_right_click_1.jpg" width="600" />

Ja ću kao primjer uzeti notepad, a Vi naravno možete uzeti bilo koju aplikaciju. Također možete dodati koliko hoćete aplikacija. Prvo što trebate uraditi je ulazak u Registry Editor. To možete učiniti pristiskom na tipku Windows+R i ona upišete **regedit**, ili upisivanjem regedit u Search. U Registry Editor-u se pozicijonirajte u sljedeći direktorij:

    HKEY_CLASSES_ROOTDirectoryBackgroundshell

<img src="/assets/windows_right_click_2.jpg" width="600" />

Sada trebate kreirati novi key. Da bi kreirali novi key kliknite desnim klikom na shell direktorij, zatim izaberite **NewKey**.

<img src="/assets/windows_right_click_3.jpg" width="600" />

Novom keyu dadnite ime koje želite da se pojavi u Context Meniju. Ja ću staviti Notepad.

<img src="/assets/windows_right_click_4.jpg" width="600" />

Sad treba da kreirate 'komandni key' koji će ustvari sadržavati komandu za pokretanje željene aplikacije. Desni klik na novi Notepad key, pa izaberite **NewKey** s menija. Ovom keyu dajte ime 'command'.

<img src="/assets/windows_right_click_5.jpg" width="600" />

Da bi finalizirali dodavnje aplikacije u Context Menu, treba da nađete i kopirate punu putanju aplikacije koju želite da bude u Context Meniju. Najbrži način da to uradite jeste da nađete aplikaciju, **držite tipku Shift i kliknete desnim klikom**. Ovim ćete u meniju dobiti **Copy as path** opciju.

<img src="/assets/windows_right_click_6.jpg" width="600" />

Nakon što ste kopirali punu putanju, poziocionirajte se u predhodno kreirani 'command' direktorij i kliknite dvaput na (Default) key, gdje ćete ubaciti string putanje u Value Data.

<img src="/assets/windows_right_click_7.jpg" width="600" />

Ako ste sve predhodne korake uspješno odradili trebao bi vam se pritiskom desnog klika na Desktopu u Context Meniju pojaviti Notepad.

Napomena: Ovako možete dodati bilo koju aplikaciju u vaš Context Meni.
