# Описание репозитория

## Подзаголовок репозитория

***
***
***

* Файл с главой
* main
* файл с описанием

'''
здесь просто какой-то код
from classes.player import Player
import utils

print("Ввведите имя игрока")  #приветствие
user_name = input().title()
print(f"Привет, {user_name}!")

user = Player(user_name, [])  #присваиваем класс пользователю

words_for_playing = utils.load_random_word()  #Создаем экземпляр для класса BasicWords

print(f"Составьте {words_for_playing.count_word()} слов из слова {words_for_playing.word.upper()}")
print("Слова должны быть не короче 3 букв")
print('Чтобы закончить игру, угадайте все слова или напишите "stop"')
print("Поехали, ваше первое слово?")

работаем пока количество унаданных и западанных слов не сравняются
while user.count_words() != words_for_playing.count_word():
    user_answer = input().lower()  # получили слово от пользователя
    if user_answer in ["stop", "стоп"]:
        break
    elif len(user_answer) < 3:
        print("слишком короткое слово\nследующее слово ")
    elif user.is_check_word(user_answer) is False and words_for_playing.is_correct(user_answer) is True:
        print("верно\nследующее слово ")
        user.add_new_word(user_answer)
    elif user.is_check_word(user_answer):
        print("уже использовано\nследующее слово ")
    elif not words_for_playing.is_correct(user_answer):
        print("неверно\nследующее слово ")

print(f"Игра завершена, вы угадали {user.count_words()} слов!")
'''
