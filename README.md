def szyfruj(slowo, klucz):
    szyfr = ""
    klucz = klucz % 26
    for litera in slowo:
        print(litera, ord(litera))
        kod = ord(litera) + klucz
        if kod > ord("z"):
            kod = kod - 26
        print(chr(kod))
        szyfr = szyfr + chr(kod)
    return szyfr


def odszyfruj(slowo, klucz):
    szyfr = ""
    klucz = klucz % 26
    for litera in slowo:
        print(litera, ord(litera))
        kod = ord(litera) - klucz
        if kod > ord("z"):
            kod = kod + 26
        print(chr(kod))
        szyfr = szyfr + chr(kod)
    return szyfr


with open("dane_6_2.txt") as dane:
    for wiersz in dane:
        print(odszyfruj(wiersz, 107))

with open("dane_6_1.txt") as dane:
    for wiersz in dane:
        print(szyfruj(wiersz, 107))
