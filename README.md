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

## b)  
    
Loin uuden tablen ja sinne muuttujan johon syötin 3 nimeä:

![kuva](https://user-images.githubusercontent.com/105205141/219024398-73672e24-ac7a-4bba-b674-843a9c1205e6.png)

Kokeilin SELECT -komennolla etsiä syöttämäni "matti" -nimen hakemalla kaikkia nimiä jotka alkavat "ma".

![kuva](https://user-images.githubusercontent.com/105205141/219025090-e78a96b2-af15-4d70-a9bd-b056f18b1857.png)

UPDATE -komennolla päivitin "matti"-nimen toiseksi: 

![kuva](https://user-images.githubusercontent.com/105205141/219025680-c5511280-cf3f-4909-8e45-2e17b06a7932.png)

DELETE -komennolla poistin "matti meikäläinen"-muuttujan kokonaan tablesta:

![kuva](https://user-images.githubusercontent.com/105205141/219025941-16ff921a-5c17-475c-b58d-971481b04316.png)



   
    
