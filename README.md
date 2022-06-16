# Programs-Python

rep = int(input("voulez vous chiffrer ou déchiffrer un message ?   1 = chiffrer  2 = déchiffrer"))

if rep == 1 :

    Message_crypter = input("quelle est votre mot à chiffrer ?")
    cle = int(input("quelle est la clé de chiffrage ?"))

    crypter = Message_crypter.upper()                             # .upper() met le message en majuscule avant de le crypter
    longueur = len(crypter)
    MessageCrypte=""

    for i in range(longueur):
        if crypter[i] ==' ':
            MessageCrypte +=' '
        else:
            asc = ord(crypter[i]) + cle                          # la fonction ord() accepte une chaîne de longueur unitaire comme argument et renvoie l' équivalence Unicode de l'argument passé
            MessageCrypte += chr(asc+26*((asc<65)-(asc>90)))     

    print("Le mot est" , MessageCrypte)

if rep == 2 :

        Message_crypter = input("quelle est votre mot à déchiffrer ?")
        cle = int(input("quelle est la clé de chiffrage ?"))

        crypter = Message_crypter.upper()                             # .upper() met le message en majuscule avant de le crypter
        longueur = len(crypter)
        MessageCrypte=""

        for i in range(longueur):
            if crypter[i] ==' ':
                MessageCrypte +=' '
            else:
                asc = ord(crypter[i]) - cle                          # la fonction asc() renvoit la table ascii
                MessageCrypte += chr(asc+26*((asc<65)-(asc>90)))

        print ("Le mot est" , MessageCrypte)

