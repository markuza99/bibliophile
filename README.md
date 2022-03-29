# Bibliophile

Autor - Petar Marković SW73/2018

# Opis problema

Bibliophile predstavlja veb aplikaciju koja služi za komentarisanje i ocenjivanje knjiga zasnovana na mikroservisnoj arhitekturi.

# Funkcionalnosti

## Neprijavljeni korisnik

Neprijavljeni korisnik može da se prijavi i registruje na sistem. Pored ovoga, on može da pregleda sve knjige koje se nalaze na aplikaciji i da ih sortira i pretražuje po različitim kriterijumima (naziv, autor, žanr).

## Prijavljeni korisnik

Pored pregleda knjiga, prijavljeni korisnik takođe ima pravo da oceni knjige u vidu komentara. Ovde korisnik može da knjigu oceni po različitim faktorima (priča, likovi, način pisanja), kao i da da svoj generalni komentar.

## Moderator

Moderator ima pravo da kreira nove knjige. Za svaku knjigu je neophodno napisati koji je autor, kom žanru spada, koliko stranica ima i kratak opis radnje. On takođe ima uvid u izvešaje vezane za knjige.

# Arhitektura sistema

**User service** - mikroservis namenjen za autentifikaciju i autorizaciju korisnika. Tehnologija: Go, PostgreSQL

**Book service** - mikroservis namenjen za knjige. Tehnologija: Rust, PostgreSQL

**Comment service** - mikroservis namenje za komentare. Tehnologija: Rust, PostgreSQL

**Report service** - mikroservis namenjen za izveštaje. Tehnologija: Rust, PostgreSQL

**Klijentska aplikacija** - aplikacija koja komunicira sa API gateway-om. Tehnologija: React






