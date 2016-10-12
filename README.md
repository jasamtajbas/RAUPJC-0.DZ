# JMBAG
0036496118

# Pitanje 1:
  U bin folderu sada se nalazi fajl ClassLibrary1.dll tj. asemblij Class Libraryja kojeg smo stvorili.
  Nakon micanja .dll i pokretanja .exe, na ekranu je bilo ispisano "Unhandeled exception" s kraćim opisom. Nedugo nakon toga, program se srušio. Srušio se zato što više nema asemblija koji je ključan za njegovo funkcioniranje (tj. ispis teksta). Program se poušava referencirati na klasu u ClassLibrary1 asembliju, a ne može ga naći u GAC-u budući da smo taj asemblij kreirali sami i nije unaprijed ugrađen u Windows.
  Mislim da je najsigurnije da Vam pošaljem sve. Ako pak moramo uvesti restrikciju, šaljem .exe fajl u kojem je metoda main te sve .dll asemblije na čije se klase moj program referencira

# Pitanje 2:
  Aplikacija je, unatoč mojoj izričitoj naredbi "Rebuild ConsoleApplication", presložila cijelo rješenje ("solution") i ispisala novi string.
  To se dogodilo jer sam tražio da se presloži konzolna aplikacija, samim time, preslaguje se i sve na što se ona referencira

# Pitanje 3:
  Ispisalo se: "Pero: Hello World"

# Pitanje 4:
  Pero Class Library asemblij je u obliku .dll fajla sada dostupan i u bin folderu

# Pitanje 5:
  Program normalno radi, kao da ništa nisam obrisao.
  I program i build normalno rade jer se konzolna aplikacija više ne referencira na prvotnu (obrisanu) referencu PeroClassLibrary već na novonastalu smještenu u bin folderu

# Pitanje 6:
  Build proces je ponovno preuzeo NodaTime asemblij.
  Packages direktorij se u slučaju brisanja isto tako vraća i u njega stavlja obrisani asemblij.
