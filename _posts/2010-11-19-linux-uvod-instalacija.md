---
layout: post
title:  "Linux uvod i instalacija"
date:   2010-11-19 15:53:34 +0200
categories: arhiva
---
Dosadili su Vam razni virusi/trojanci/crvići? Ne želite da se mučite s raznoraznim licencama? Želite jednostavan operativni sistem, za pregledavanje mail-ova, za surfanje, i još mnogo toga. Koji je uz to još i atraktivan i **besplatan**. Možda biste u tom slučaju trebali pokušati s linuxom :)

<img src="/assets/linux_instalacija_1.jpg" width="600" />

## Uvod

Linux je nastao početkom 90-tih godina. U ranijim danima je služio kao eskperimentalni sistem koji su koristili studenti, programeri i općenito ljudi jako orijentirani na rad s računaorm. No to se iz godine u godinu mijenjalo. Istina, jako sporo, ali se mijenjalo. Može se reći da danas za linux postoje svi programi za prosječnog kućnog korisnika. Svi programi za koje znate na Windowsu imaju alternativu na linuxu, neki čak i bolji nego na Windowsu. Najveće prednosti linuxa su: sigurnost, stabilnost i naravno činjenica da je besplatan. Postoji samo neznatan broj virusa, jer osnovni dizajn linuxa i prateći programi otežavaju ozbiljne upade u sistem.

## Distribucije

Neka definicija linux distribucije bi bila: 'Linux distribucija je operativni sistem sastavljen od linux kernela , GNU sistemskih i aplikacijskih programa, Xorg grafičkog servera i grafičkog okruženja.'  Od prvih početaka linuxa do danas se razvilo mnogo distribucija. Izrađivali su ih razne firme i timovi programera. Neke od najpoznatijih su: Slackware, Debian, Ubuntu, Mint, OpenSUSE, Red Hat itd. Nemoguće je utvrditi koja distribucija je najbolja, svaka ima svoje mane i svoje prednosti. Sve zavisi od osobe do osobe, i zahtjeva koje ta osoba ima.

## Instalacija

Nakon kratkog uvoda, i malo priče o distribucijama, možemo preći na samu instalaciju :) Izabrao sam Ubuntu distribuciju, iz razloga što je ona danas jedna od najviše korištenih distribucija. Možete je besplatno preuzeti sa http://www.ubuntu.com/desktop/get-ubuntu/download . Zadnja verzija je 10.10, koju ću ja kroz ovaj tutorijal i instalirati.

Nakon što bootate CD pojaviće se prvi prozor gdje če Vas pitati da li želite samo testirati Ubuntu (Try Ubuntu) ili ga instalirati.

<img src="/assets/linux_instalacija_2.jpg" width="600" />

Ja ću naravno kliknuti **Install Ubuntu**, a vi ako želite možete ga prvo testirati, da vidite je li to za Vas :) Kada kliknete install provjeriće ima li dovoljno prostora na disku, je li priključen na struju (ako je laptop u pitanju) i postoji li internet konekcija. Ispod toga su dva dugmića gdje možete izabrati da skinete i instalirate dodadne programe. Neću ih obilježiti, iz razloga što se ti programi mogu instalirati i nakon instalacije. Stoga idemo na **Forward**.

<img src="/assets/linux_instalacija_3.jpg" width="600" />

Sljedeće je alokacija prostora za Ubuntu. Pošto ga ja instaliram na virtualnu mašinu iskoristiću čitav slobodan prostor, i obilježiti **Erase and use the entire disk**.

Napomena:  Ubuntu, kao i svaki drugi operativni sistem, možete instalirati u [DualBoot] režimu, uz recimo Windows.

Ako želite dual boot onda ćete selektovati **Specify partitions manually (advanced)**, i alocirati prostor na disku za Ubuntu.

<img src="/assets/linux_instalacija_4.jpg" width="600" />

Kad alocirate prostor kliknite **Forward**, prikazaće vam prostor koji ste alocirali. Ako ste zadovoljni, kliknite **Install Now**.

<img src="/assets/linux_instalacija_5.jpg" width="600" />

Kreće instalacija. U toku instalacije će vam nuditi da izaberete vremensku zonu, layout tastature, i lične podatke (tipa username, password itd). To se sve popunjava u toku same instalacije.

<img src="/assets/linux_instalacija_6.jpg" width="600" />

<img src="/assets/linux_instalacija_7.jpg" width="600" />

<img src="/assets/linux_instalacija_8.jpg" width="600" />

Kad se završi kopiranje file-ova pokušaće se konektovati na internet da bi skinuo neke dodadne arhive (iskreno ne znam zašto to radi, na prijašnjim verzijama Ubuntu-a se to nije pojavljivalo). Samo kliknite na strelicu kraj **Retrieving file**, i onda desno na **Skip**.

<img src="/assets/linux_instalacija_9.jpg" width="600" />

Nakon uspješno završene instalacije, potrebno je još samo da restartujete računar i počnete koristiti Ubuntu.

Za kraj bi spomenuo još Udruženje linux korisnika Bosne i Hercegovine, koje ima jako dobar forum, gdje imate mnogo informacija u vezi linuxa, i gdje možete pitati ako negdje zapnete.

Link: http://www.linux.org.ba/

Do čitanja

[DualBoot]: https://en.wikipedia.org/wiki/Multi-booting
