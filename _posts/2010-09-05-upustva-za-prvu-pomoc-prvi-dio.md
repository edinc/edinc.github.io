---
layout: post
title:  "Mala upustva za prvu pomoć (prvi dio)"
date:   2010-09-05 15:53:34 +0200
categories: arhiva
author: Edin Cenanovic
---
Vaš računar je možda dizajniran da učini vaš život lakšim, ali često ti isti računari imaju dosta problema. Danas ću pisati o najčešćim problemima, i kako da ih se rješite :)

<img src="/assets/upustva_pic1.jpg" width="600" />

Ova lista problema svakako nije kompletna, i uvijek bi trebali imati instaliran neki antivirusni software i firewall, i svakako redovno raditi backup svojih podataka. A ako trenutno imate problem pogledajte listu koja slijedi:

## Računar neće da starta Windows

<img src="/assets/upustva_pic2.jpg" width="600" />

**Prvo pokušajte sa Safe Mode-om**

Prilikom paljenja mašine pritisnite tipku F8 kako bi ušli u Safe Mode. Ako uspijete ući u Windows u Safe Mode-u, problem je vjerovatno u driverima za grafičku karticu, ili imate neke spyware programe na vašem računaru.

**Safe Mode ne pomaže**

Ako ne možete pristupiti Windowsu ni iz Safe Mode-a, onda iskoristite Startup Repair alate, kojima možete pristupiti iz Safe Mode menija. Ili možete jednostavno ubaciti Vaš instalacioni Windows CD/DVD-a, gdje ćete izabrati Repair opciju. Ako Vam prilikom paljenja na ekranu stoji poruka 'bootmgr is missing', popravićete to komandom bootrec /fixboot. Koju upisujete u Command Promt, koji ste pozvali pomoću instalacionog Windows CD/DVD-a.

<img src="/assets/upustva_pic3.jpg" width="600" />

**Blue Screen Of Death (BSOD)**

Ako vam se sistem ruši s vremena na vrijeme, pri čemu se      pojavljuje BSOD, prvo što morate da uradite jeste isključite  automatsko restartovanje računara nakon BSOD-a. Sljedeće što  trebate raditi jeste zapisati error poruku BSOD-a i zatim je  upisati u Google, i tražiti rješenje :) I to je zaista najbolja solucija, jer ima dosta različitih BSOD errora.

<img src="/assets/upustva_pic4.jpg" width="600" />

Kod Windows 7 skoro pa uvijek BSOD prouzrokuju problemi sa driverima i hardware-om. Kada saznate koji driver pravi probleme, jednostavno uđite u Safe Mode i izbrišite ili uprgade-ate isti.

**Ništa nije pomoglo?**

Ako Vam ovo ništa nije pomoglo, i nemate backup podataka. Ubacite neku live linux distribuciju, spasite podatke i reinstališite sistem.

## Računar je usporio

<img src="/assets/upustva_pic5.jpg" width="600" />

**Provjerite Task Manager**

Prva stvar koju će uraditi svaki 'geek'  kad mu uspori računar, jeste ulazak u Task Manager, da bi vidio koje aplikacije i koji procesi uzimaju najviše CPU-a ili memorije. Kada nađete aplikacije koje Vam 'gutaju memoriju' najbolje bi bilo da ih odma 'ubijete'.

**Deinstalirajte sporni software**

Kada ste ubili aplikacije i procese koji vam gutaju CPU i memoriju, vrijeme je i da ih reinstalirate. Najbolje bi bilo da to odradite pomoću nekog software-a predviđenog za to. Kao npr. [Revo Uninstaller] ili [PC Decrapifier], koji će uredno obrisati aplikacije bez ostavljanja bilo kakvih tragova.

**Očistite računar**

Očistiti računar je zaista lako. Taj posao možete odraditi prilično dobrim alatom, zvanim [CCleaner]. Čak ga možete podesiti da sam vrši 'cleaning' jednom sedmično.

**Provjerite ima li virusa ili spyware-a**

Obavezno treba skenirati računar nakon što Vam isti uspori. Preporučujem besplatni Microsoft Security Essentials.

**Koristite Advanced Tools u Windows 7**

Windows 7 ima jako dobar skupa alata za 'rad s problemima'. Oni se nalaze u Control Panelu. Do njih ćete doći ulazkom u Control Panel, pa zatim na Performance Information And Tool -> Advanced Tools. Ovdje se nalazi mnogo solucija u rješavanju određenih problema.

**Ugasite nepotrebne startup aplikacije**

O ovome sam pisao u članku Windows 7 Tips and Tricks, podnaslov Zaustavite aplikacije koje zauzimaju memoriju.

Toliko za sad. U drugom djelu ovih malih upustava ću pisati o problemima sa internet konekcijom i o čišćenju virusa i spyware-a.

Do čitanja :)

[Revo Uninstaller]: https://www.revouninstaller.com/revo_uninstaller_free_download.html
[PC Decrapifier]: https://www.pcdecrapifier.com/
[CCleaner]: http://www.piriform.com/ccleaner
