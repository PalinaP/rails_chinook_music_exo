# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


Exo 2 : Chinook Music

Pour cet exercice, je vais te refiler une BDD sur laquelle tu vas bosser… ce qui devrait te rappeler un exercice d'hier ! Mais plutôt que de se passer des fichiers de BDD, je vais te faire re-créer cette BDD via un seed.
2.2.1. Création des models

Crée une nouvelle application Rails. Tu vas maintenant générer un nouveau model Album dont les attributs seront les suivants :

    title qui porte le titre de l'album et est de type string.
    artist qui porte nom de l'artiste et est de type string.

Ensuite tu vas faire un second model Track avec les attributs :

    title qui porte le titre de la chanson et est de type string.
    album qui porte le titre de l'album et est de type string.
    artist qui porte le nom de l'artiste et est de type string.
    duration qui porte la durée de la chanson (en millisecondes) et est de type integer.
    size qui porte la taille (en octets) de la chanson et est de type integer.
    price qui porte le prix de la chanson et est de type float.

Pense bien à passer les migrations et n'hésite pas à tester le bon fonctionnement des 2 models en console.
2.2.2. Seed de la BDD de travail

Maintenant, tu vas coller le code suivant dans ton seeds.rb puis lancer un $ rails db:seed. Attention, je te préviens, les arrays sont très longs 😇

Album.destroy_all
Track.destroy_all

album_array = [{title:'For Those About To Rock We Salute You', artist:'AC/DC'},{title:'Balls to the Wall', artist:'Accept'},{title:'Restless and Wild', artist:'Accept'},{title:'Let There Be Rock', artist:'AC/DC'},{title:'Big Ones', artist:'Aerosmith'},{title:'Jagged Little Pill', artist:'Alanis Morissette'},{title:'Facelift', artist:'Alice In Chains'},{title:'Warner 25 Anos', artist:'Antônio Carlos Jobim'},{title:'Plays Metallica By Four Cellos', artist:'Apocalyptica'},{title:'Audioslave', artist:'Audioslave'},{title:'Out Of Exile', artist:'Audioslave'},{title:'BackBeat Soundtrack', artist:'BackBeat'},{title:'The Best Of Billy Cobham', artist:'Billy Cobham'},{title:'Alcohol Fueled Brewtality Live! [Disc 1]', artist:'Black Label Society'},{title:'Alcohol Fueled Brewtality Live! [Disc 2]', artist:'Black Label Society'},{title:'Black Sabbath', artist:'Black Sabbath'},{title:'Black Sabbath Vol. 4 (Remaster)', artist:'Black Sabbath'},{title:'Body Count', artist:'Body Count'},{title:'Chemical Wedding', artist:'Bruce Dickinson'},{title:'The Best Of Buddy Guy - The Millenium Collection', artist:'Buddy Guy'},{title:'Prenda Minha', artist:'Caetano Veloso'},{title:'Sozinho Remix Ao Vivo', artist:'Caetano Veloso'},{title:'Minha Historia', artist:'Chico Buarque'},{title:'Afrociberdelia', artist:'Chico Science & Nação Zumbi'},{title:'Da Lama Ao Caos', artist:'Chico Science & Nação Zumbi'},{title:'Acústico MTV [Live]', artist:'Cidade Negra'},{title:'Cidade Negra - Hits', artist:'Cidade Negra'},{title:'.........



  album_array.each_with_index do |album, index|
    Album.create(album)
    puts "#{index} albums créés"
  end

  tracks_array.each_with_index do |track,index|
    Track.create(track)
    puts "#{index} pistes créés"
  end

2.2.3. Questions

Maintenant que ta BDD est prête, tu vas répondre aux questions ci-dessous :
a) Niveau facile

    Quel est le nombre total d'objets Album contenus dans la base (sans regarder les id bien sûr) ?
    Qui est l'auteur de la chanson "White Room" ?
    Quelle chanson dure exactement 188133 milliseconds ?
    Quel groupe a sorti l'album "Use Your Illusion II" ?

b) Niveau Moyen

    Combien y a t'il d'albums dont le titre contient "Great" ? (indice)
    Supprime tous les albums dont le nom contient "music".
    Combien y a t'il d'albums écrits par AC/DC ?
    Combien de chanson durent exactement 158589 millisecondes ?

c) Niveau Difficile

Pour ces questions, tu vas devoir effectuer des boucles dans la console Rails. C'est peu commun mais c'est faisable, tout comme dans IRB.

    puts en console tous les titres de AC/DC.
    puts en console tous les titres de l'album "Let There Be Rock".
    Calcule le prix total de cet album ainsi que sa durée totale.
    Calcule le coût de l'intégralité de la discographie de "Deep Purple".
    Modifie (via une boucle) tous les titres de "Eric Clapton" afin qu'ils soient affichés avec "Britney Spears" en artist.

