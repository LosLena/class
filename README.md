class Animals:
  def __init__(self, voice, weight, name, vid):
    self.voice = voice # Голос
    self.name = name # имя
    self.vid = vid # класс животного
    self.weight = weight # вес 
  
  def feed(self):
    print(f"{self.name} - накормлен (a)")
  
  def animals_voice(self):
    print(f"Голос {self.name} звучит {self.voice} - это класс животного {self.vid}")


class Grup1_Animalf(Animals): # корову и козу доить
  def milk(self):
    if self.vid == "корова":
      print(f"Надоили {self.name} 10 л")
    else:
      print(f"Надоили {self.name} 2 л")


class Grup2_Animalf(Animals): # собирать яйца у кур, уток, гусей
    def collect_eggs(self):
      if self.vid == "куры":
        print(f"Собрали {self.name} 5 яиц")
      elif self.vid == "гуси": 
        print(f"Собрали {self.name} 1 яицо")
      else:
        print(f"Собрали {self.name} 2 яица")

class Grup3_Animalf(Animals): # овец стричь
    def shear_sheep(self):
      print(f"Состригли у овцы {self.name} 1 кг шерсти") 


# Создаем животных
cow = Grup1_Animalf(voice="Му-Му", weight=100, name="Манька", vid="корова")
goat1 = Grup1_Animalf(voice="Ме", weight=25, name="Рога", vid="коза")
goat2 = Grup1_Animalf(voice="Ме", weight=25, name="Копыта", vid="коза")
goose1 = Grup2_Animalf(voice="Га-га", weight=10, name="Серый", vid="гуси")
goose2 = Grup2_Animalf(voice="Га-га", weight=10, name="Белый", vid="гуси")
chicken1 = Grup2_Animalf(voice="Ко-ко", weight=7, name="Ко-ко", vid="куры")
chicken2 = Grup2_Animalf(voice="Ку-ка-ре-ку", weight=10, name="Кукареку", vid="куры")
duck = Grup2_Animalf(voice="Кря-кря", weight=10, name="Кряква", vid="утки")
sheep1 = Grup3_Animalf(voice="Бе", weight=10, name="Барашек", vid="овца")
sheep2 = Grup3_Animalf(voice="Бе", weight=10, name="Кудрявый", vid="овца")

def all_feet():
  print("Всех накормить:")
  cow.feed()
  goat1.feed()
  goat2.feed()
  goose1.feed()
  goose2.feed()
  chicken1.feed()
  chicken2.feed()
  duck.feed()
  sheep1.feed()
  sheep2.feed()
  

def milf_animals():
  print("Подоить животных:")
  cow.milk()
  goat1.milk()
  goat2.milk()


def shear_animals():
  print("Подстричь животных:")
  sheep1.shear_sheep()
  sheep2.shear_sheep()


def collect_animals():
  print("Соберем яйца")
  goose1.collect_eggs()
  goose2.collect_eggs()
  chicken1.collect_eggs()
  chicken2.collect_eggs()
  duck.collect_eggs()

def voice_animals():
  print("Голоса животных:")
  cow.animals_voice()
  goat1.animals_voice()
  goat2.animals_voice()
  goose1.animals_voice()
  goose2.animals_voice()
  chicken1.animals_voice()
  chicken2.animals_voice()
  duck.animals_voice()
  sheep1.animals_voice()
  sheep2.animals_voice()

def all_weight():
  weithts =int(cow.weight) + int(goat1.weight)+ int(goat2.weight) + int(goose1.weight) + int(goose2.weight) + int(chicken1.weight) + int(chicken2.weight) + int(duck.weight) + int(sheep1.weight) + int(sheep2.weight)
  print(f"Общий вес животных {weithts}")

def max_weight():
    weights = {'animal': cow.name, 'w': cow.weight},{'animal': goat1.name, 'w': goat1.weight},{'animal': goat2.name, 'w': goat2.weight}, {'animal': goose1.name, 'w':goose1.weight}, {'animal': goose2.name, 'w':goose2.weight}, {'animal': chicken1.name, 'w':chicken1.weight}, {'animal': chicken2.name, 'w':chicken2.weight}, {'animal': duck.name, 'w':duck.weight}, {'animal': sheep1.name, 'w':sheep1.weight}, {'animal': sheep2.name, 'w':sheep2.weight}
    
    max_weirgh13 = 0
    max_name =""
    for max_animals1 in weights:
      if max_weirgh13 < max_animals1['w']:
        max_weirgh13 = max_animals1['w']
        max_name = max_animals1['animal']
    
    print(f"Самое крупное животное на ферме {max_name} с весом {max_weirgh13}")

menu = int(input("Введите команду, что вы хотите делать со своей фермой: 1-накормить всех 2-подстричь овец 3-показать как звучат голоса животных 4-собрать яйца 5-подоить 6-общий вес животных 7- кто самое крупное и тяжелое животное : "))
if menu == 1: 
  all_feet()
elif menu == 2:
  shear_animals()
elif menu == 3:  
  voice_animals()
elif menu == 4:  
  collect_animals()
elif menu == 6:
  all_weight()
elif menu == 7:  
  max_weight()
elif menu == 5: 
  milf_animals()
else:
  print("Нет такого кода")
