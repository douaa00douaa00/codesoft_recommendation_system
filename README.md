# codesoft_recommendation_system
from nltk.corpus import wordnet
import re
respond=input("Hi!,I am a small chatbot that helps you pick a good movie . Do you need help? (Y/N) :")
respond=respond.lower()

film={'Drama':{"dune","Alice Doesn't Live Here Anymore ","Carol","The Devil All the Time","The Irishman ","la la land"},
            'Adventure':{'jungle cruise','the call of the wild','chupa','jumanji','damsel','slumberland','mowgli'},
            'Action':{'carter','heart of stone','lost bullet','aka','the gray man','lucy','kandahar'},
            'Comedy':{'click','medellin','bad trip','do revenge','lift','you again','free guy','the man from toronto'},
            'detective':{'seven','zodiac','mystic river','insomnia','memento','the long goodbye'},
            'science-fiction':{'transcendence','robot','arrival','lucy','oxygen','paradise','the midnight sky','tau','in time','limitless'},
            'horror':{"1922","Nun","life","viking wolf","nightbooks","the conference","the silence","shaitaan"},
            'documentary':{"the social dilemma","the deepest breath",'a secret love','stutz','fyre','bitconned','a secret love','tell me who I am','we are one'},
            'cartoon':{'Dora','shark tale','the boss baby','the sea beast','the bad guys','the book of life ','the emoji movie','minions'},
            'historical':{'the king','outlaw king','mudbound','1922','july','the two pops','narvik','unbroken','13th','Blonde'},
            }
while True:
    if (respond=="y" or respond=="yes"):
        gender=input("What gender of movies you like the most ? :")
        gender=gender.lower()
        found_genre = False
        for genre, movies in film.items():
            if genre.lower() == gender.lower():
                found_genre = True
                print(f"Genre: {genre}")
                for movie in movies:
                    print(f"- {movie}")
        if not found_genre:
            print("Genre not found.")
        else:
            print("I recommend you to watch them !")
            break
    else:
        print("Alright !, see you later!")
        break
