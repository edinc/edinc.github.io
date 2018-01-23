---
layout: post
title:  "[HOW TO] Integracija SATA drivera u Windows XP"
date:   2010-10-29 15:53:34 +0200
categories: arhiva
---
Da li Vam se ikad desilo da prilikom instalacije Windows Xp-a dođe do greške 'Setup did not find any hard disk drives installed in your computer' ?!

<img src="/assets/sata_xp_1.jpg" width="600" />

Predstaviću Vam jedno od mnogih načina kako riješiti ovaj problem. Naime, ovo se dešava jer Windows ne može pronaći SATA drivere za Vaš hard disk.

Za integraciju SATA drivera u Windows XP instalacioni CD ću koristiti program nLite ( možete ga preuzeti sa stranice: http://www.nliteos.com ).

Prvo što morate uraditi jeste naći drivere za vaš hard disk,i skinuti ih. Nakon toga ubacite Windows XP CD i kopirajte kompletan sadržaj foldera u neki proizvoljni folder ( ja sam sadržaj foldera kopirao u jedan folder na Desktopu, kako ga nebi poslije morao tražiti puno).

Kada skinete i instalirate nLite pojaviće se sljedeći prozor

<img src="/assets/sata_xp_2.jpg" width="600" />

Klikom na **Next** dolazimo do prozora gdje se 'učitava' sadržaj Windows CD-a, koji ste predhodno kopirali sa CD-a. Kliknete **Browse** i jednostavno nađete destinacijski folder, i **OK**.

<img src="/assets/sata_xp_3.jpg" width="600" />

Kad skenira podatke ispisaće vam o kojoj verziji XP-a se radi, na kojem je jeziku, koji Service Pack je integrisan, i još neke informacije. Kliknite **Next**.

Pojavio se prozor Presets koji slobodno možete preskočiti, jer prvi put pravite CD/Image s nLite-om, tako da ovo preskačemo i idemo **Next**.

<img src="/assets/sata_xp_4.jpg" width="600" />

Došli smo do Task Selection dijela, gdje birate šta će vaša modifikovana verzija Windowsa sadržavati. Pošto ovdje obrađujem samo integraciju drivera kliknite na **Drivers** i **Bootable ISO**, pa **Next**.

<img src="/assets/sata_xp_5.jpg" width="600" />

Otvoriće se prozor Drivers u kojem ćete naći prethodno skinute drivere i 'ubaciti ih', i to na sljedeći način: kliknite **Insert** -> **Single driver** -> pronađite folder u kom su driveri i odaberite njihov .inf file.

<img src="/assets/sata_xp_6.jpg" width="600" />

Napomena: Koristio sam Intelove SATA drivere za ovaj Tutorijal, Vi ćete naravno korisiti odgovarajuće drivere za vaš hard disk.

Nakon što ste otvorili .inf file drivera ponudiće vam drivere za različite hard diskove ( što ne mora značiti da će i vama otvoriti mnogo drivera, sve zavisi od proizvođača hard diska i samih drivera). Izaberete odgovarajući, i **OK**, pa **Next**.

<img src="/assets/sata_xp_7.jpg" width="600" />

Sad će vas pitati da li želite startati proces integracije drivera. Naravno kliknite **Yes**, i driveri će se integrisati u 'vašu' verziju Windowsa.

<img src="/assets/sata_xp_8.jpg" width="600" />

Kad završi integraciju, samo je još ostalo da napravite image novomodifikovanog Windowsa ili da ga spržite na CD. Ja ću odabrati opciju da napravim ISO image. U polje **Label** unosite ime image-a, pa zatim kliknete na **Make ISO**. Pitaće vas za ime image-a i gdje će ga spremiti.

<img src="/assets/sata_xp_9.jpg" width="600" />

ISO image 'vašeg' Windows XP-a možete jednostavno spržiti s svakim novijim software-om za prženje DVD/CD-ova.

I to bi već bilo to. Ako ste navedene korake odradili ispravno moći te instalirati svoju modifikovanu verziju Windows XP-a.
