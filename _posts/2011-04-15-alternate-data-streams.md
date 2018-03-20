---
layout: post
title:  "Alternate Data Streams"
date:   2011-04-15 15:53:34 +0200
categories: arhiva
author: Edin Cenanovic
---
U NTFS file sistemu, file se sastoji od različitih file streamova. Jedan stream sadrži informacije o sigurnosti, drugi sadrži 'stvarne podatke' koje očekujete da se nalaze u fileu. Alternate Data Stream (u daljem tekstu ADS) je jedan od streamova koji je vrlo opasan. **On je skriven**. Možete imati file od 1 KB u 'standardnom' data streamu, i na njega prikačen ADS od stotinjak MB. File manager ili explorer će prikazivati onaj 1KB standardnog data streama.

<img src="/assets/asd_1.jpg" width="600" />

Ovo znači da se u ADS može sakriti prilično puno informacija, a da to niko neće primjetiti. Još jedna dobra stvar kod ADSa, za potencijalne maliciozne korisnike, je što se u ADS mogu ubacivati stvari bez administratorskih privilegija. Čak i pomoću Guest accounta to možete učiniti.

## MFT (master file table)

MFT je mjesto koje sadrži sve informacije o fileovima i direktorijima u NTFS file sistemu. MFT je ustvari relaciona baza podataka, sastavljena od tabela i raznih atributa različitih fileova (Slika 1). Prilikom kreiranja bilo kojeg filea na NTFS particiji, automatski se kreira i zapis tog filea u MFT.

<img src="/assets/asd_2.jpg" width="600" />

Nakon nekog vremena, sve više fileova i datoteka su pospremljene na file sistem. Samim tim raste i MFT, i performance hard diska se smanjuju. Zbog ovog problema operativni sistem rezerviše, pri prvom pokretanju NTFS file sistema, 12,5% za MFT. Ovaj prostor se naziva 'MFT Zona'. Naravno, MFT može premašiti veličinom i 'MFT Zonu'. U tom slučaju operativni sistem alocira još prostora na disku. Ovo praktično znači da je jedino ograničenje u rastu MFTa fizička veličina diska.

## Struktura i način zapisivanja ADSa

Struktura zapisa ADS je ista kao kod standardnih data streamova, osim što file s ADSom ima dva ili više data atributa, umjesto jednog. NTFS dopušta samo jedan neimenovan data atribut po zapisu, tako da svaki dodadni data atribut mora biti imenovan. Ovi dodatni data atributi sadrže ADS. Na Slici 2 pogledajte standardni data stream, a odma zatim, na Slici 3, pogledajte zapis sa ADSom. Pa uporedite.

<img src="/assets/asd_3.jpg" width="600" />

Zapisi izgledaju skoro isto, osim dodatka još jednog Data atributa u ADSu. Ime dodadnog data atributa je pohranjeno u ljubičastom dijelu (Slika 3).

## Legalno korištenje ADSa

Predstavljanjem Windowsa 2000, Mircosoft je dodao 'Summary' tab koji prikazuje opcije odabranog filea. Neke informacije tog taba uključuju naziv, subjekt i autora. Metadata ovih informacija je pohranjena upravo u ADS tog filea. U slučaju slika, thumbnail može biti smješten u ADS, radi bržeg prikazivanja slika kada je Windows Explorer u Thumbnail Viewu.

Ovo je samo jedna od stvari koja legalno koristi ADS, svakako da ih ima još mnogo više.

## Maliciozno korištenje ADSa

ADS je vrlo moćna stvar za maliciozne korisnike, jer je praktično nevidljiv. U njega se mogu sakriti razne informacije, maliciozni kod, mogu se čak vršiti DOS napadi.

Sakrivanje određenih informacija u ADS i nije toliko štetno kao npr. sakrivanje malicioznog koda. Jednostavnom komandom start se taj 'sakriveni' kod može pokrenuti i tim ugroziti sistem.

Najgore je što proizvođači antivirusnih alata nemaju namjeru tražiti maliciozni kod u ADSu, tako da su korisnici veoma 'ranjivi' kad je u pitanju malverizacija ADSa.

ADS također može služiti u kreiranju DOS napada na lokalnu mašinu. Kao što već znate sve što se nalazi u ADSu je 'nevidljivo', tako možemo npr. u ADS nekog .txt filea staviti HD film veličine 4GB, koji će ostati neprimjećen od sistema. Zamislite sad da se popunjava ADS sve dok ima prostora na fizičkom disku – klasični Denial of service napad :) Mašina će vam totalno usporiti, a vi pojma nemate zašto je usporila jer se sve čini uredu.

## Alati za pronalazak ADSa

Third-party alata za pronalazak ADSa ima nekoliko. Najpoznatiji su: LADS, Streams, CrucialADS, TDS-3. Svaki ovaj alat ima svoje prednosti i svoje mane. Možda najpoznatiji i najkorišteniji od ovih alata je LADS.

Komanda za korištenje LADSa je sljedeća:

    lads [Directoy] [/S] [/D] [/A] [/Xname]

Gdje **Directory** označava koji direktorij će se skenirati. Parametar **/S** će skenirati poddirektorije, **/D** stavlja LADS u debug mode, a **/A** će sabrati sve bajtove nađene u skrivenom streamu. **/Xname** služi za pronalazak skrivenih streamova s određenim imenom.

Output komande možete vidjeti na Slici 4.

<img src="/assets/asd_4.jpg" width="600" />
