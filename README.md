
# 📘 Programmation Orientée Objet (POO) en Python

Bienvenue dans cette introduction complète à la **programmation orientée objet (POO)** en Python. Ce cours vous guide étape par étape à travers les concepts fondamentaux de la POO en Python, avec des exemples pratiques, des analogies claires et une progression pédagogique adaptée à tous ceux qui veulent maîtriser ce paradigme essentiel.

---

## 📚 Table des matières

1. Qu'est-ce que la POO ?
2. Définir une classe en Python
3. Instancier une classe
4. Attributs de classe vs attributs d'instance
5. Méthodes d'instance
6. Méthodes spéciales (`__init__`, `__str__`)
7. Héritage entre classes
8. Surcharge et extension de méthodes avec `super()`
9. Exemple pratique : Parc à chiens 🐶
10. Conclusion

---

## ❓ Qu'est-ce que la POO ?

La **programmation orientée objet** est un paradigme qui consiste à structurer un programme en **objets**, représentant des entités du monde réel. Chaque objet a :

- des **attributs** (données, état)
- des **méthodes** (comportements, fonctions)

Les **4 piliers** de la POO :

- **Encapsulation** : cacher les détails internes et protéger les données.
- **Héritage** : réutiliser du code à partir d'une classe parente.
- **Abstraction** : se concentrer sur ce qui est important pour l’utilisateur.
- **Polymorphisme** : permettre à différents objets de partager la même interface.

---

## 🧱 Définir une classe en Python

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

---

## 🐶 Instancier une classe

```python
miles = Dog("Miles", 4)
print(miles.name)  # Miles
print(miles.age)   # 4
```

---

## 🔁 Attributs de classe vs d'instance

```python
class Dog:
    species = "Canis familiaris"  # Attribut de classe

    def __init__(self, name, age):
        self.name = name          # Attribut d'instance
        self.age = age
```

- **Attribut de classe** : partagé par toutes les instances.
- **Attribut d'instance** : spécifique à chaque objet.

---

## 🔧 Méthodes d'instance

```python
class Dog:
    def speak(self, sound):
        return f"{self.name} says {sound}"
```

Utilisation :

```python
miles = Dog("Miles", 4)
print(miles.speak("Woof"))  # Miles says Woof
```

---

## ⚙️ Méthodes spéciales

### `__init__`  
Constructeur qui initialise les données à la création de l’objet.

### `__str__`  
Retourne une représentation lisible :

```python
def __str__(self):
    return f"{self.name} is {self.age} years old"
```

---

## 🧬 Héritage entre classes

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

class Bulldog(Dog):
    pass

jim = Bulldog("Jim", 5)
```

- La classe enfant hérite des attributs et méthodes de la classe parent.

---

## 🔄 Surcharge et extension de méthodes avec `super()`

```python
class JackRussellTerrier(Dog):
    def speak(self, sound="Arf"):
        return super().speak(sound)
```

✅ `super()` permet d’appeler la méthode du parent tout en personnalisant le comportement.

---

## 🧪 Exemple pratique : Parc à chiens 🐶

```python
class Dog:
    species = "Canis familiaris"

    def __init__(self, name, age):
        self.name = name
        self.age = age

    def speak(self, sound):
        return f"{self.name} barks: {sound}"

class Bulldog(Dog):
    pass

class JackRussellTerrier(Dog):
    def speak(self, sound="Arf"):
        return super().speak(sound)

miles = JackRussellTerrier("Miles", 4)
print(miles.speak())  # Miles barks: Arf
```

---

## ✅ Conclusion

Dans ce cours, vous avez appris à :

- Définir une classe avec `class`
- Créer des objets avec des **attributs** et **méthodes**
- Distinguer **attributs de classe** et **attributs d’instance**
- Ajouter des comportements personnalisés via des **méthodes**
- Étendre une classe grâce à l’**héritage**
- Appeler les méthodes du parent avec **`super()`**

---

## 📽 Cours recommandé

🎥 *Intro to Object-Oriented Programming in Python – Real Python*  
https://realpython.com/courses/oop-python/

---

## 👨‍🏫 Auteur

**Jean Marie Daniel Vianney Guedegbe**  
Senior Backend Developer | Passionné de Python, Clean Architecture, et pédagogie technique

GitHub : [@gdaniel-dev](https://github.com/gdaniel10027)  

---

## 🌟 Tu veux soutenir ce projet ?

- ⭐ Étoile ce dépôt sur GitHub
- 🔁 Partage avec tes amis développeurs
- 📩 Rejoins ma newsletter pour d'autres astuces Python !

---

© 2025 | Tous droits réservés - Jean Marie Daniel Vianney Guedegbe
