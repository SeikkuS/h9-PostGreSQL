# h9-PostGreSQL

x) Yrityssoftaa. Keksi esimerkki palvelusta, jota käytetään wepissä selaimella, koodi ajetaan palvelimella ja taustalla on tietokanta. Mitä etuja tällä toteutustavalla on vaihtoehtoisiin toteutustapoihin verrattuna? (Tässä x-alakohdassa ei tarvitse tehdä testejä koneella tai toteuttaa mitään, pelkkä kuvittelu ja vastauksen kirjoittaminen riittää)
a) Postgre. Asenna PostgreSQL ja testaa se suorittamalla SQL-komento. (Jos teit jo tunnilla, tee uusi Linux-käyttäjä ja tälle tietokanta ja tietokantakäyttäjä.)
b) Crud. Kokeile CRUD (create, read, update, delete) kirjoittamalla SQL-käsin. (Artikkeli alla vinkeissä kertoo, kuinka tämä tehdään. Jos SQL on tuttua, voit keksiä tauluille ym omat aiheet ja nimet.)

## x)

15.2.2023. klo: 13.57

- www.twitch.tv, streamauspalvelu.

Tiedon tallentaminen tietokantaan mm. tavallisen tiedostoarkistoinnin sijasta helpottaa navigointia ja organisointia, sekä tekee tiedon tallentamisesta nopeampaa (automatisointi ja selkeät logiikat). Jos kyseessä on iso määrä erilaista dataa, tietokannan käyttäminen tekee asiasta suunnattomasti helpompaa. 

## a) 

15.2.2023. klo: 14.02

asensin itselleni PostGreSQL:n seuraavilla komennoilla

    sudo apt-get update
    sudo apt-get install -y postgresql

jonka jälkeen käynnistin postgresql:n

    sudo systemctl start postgresql

ja loin itselleni tietokannan ja käyttäjän ja avaan SQL promptin.

    sudo -u postgres createdb seikku
    sudo -u postgres createuser seikku
    psql
   
![kuva](https://user-images.githubusercontent.com/105205141/219023321-c47e880c-7648-4f2d-b125-d11edf03f583.png)
    
Loin uuden tablen ja sinne muuttujan

![kuva](https://user-images.githubusercontent.com/105205141/219024398-73672e24-ac7a-4bba-b674-843a9c1205e6.png)

    

   
    
