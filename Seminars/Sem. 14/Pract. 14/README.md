
### Задача:
Реализирайте класов бар, в който се продават нормални напитки и алкохолни напитки. Трябва да имате функции за зареждане на напитки от бара и взимане на напитка от бара.
При зареждането се посочва и броят на артикулите, които се зареждат. Ако не се каже брой - зарежда се 1 артикул.

При взимането на напитка от бара: Избира се тип (нормална или алкохолна) и се връща най-отдавна заредената в бара. 
Във всеки момент трябва да могат да се взимат статистика за бара - брой продадени артикула oт всеки тип и сумарно продадени мл.

**Напитката** има име (низ с произволна дължина, само от латински символи, в който първият символ е главен), количество (в мл [200, 1000]), а **алкохолната напитка** има *име (низ с произволна дължина, само от латински символи, в който първият символ е главен),  количество (в мл [200, 1000]) и процент алкохол [5, 98]*.

Примерен интерфейс:
 ```c++

int main()
{
	Bar b;

	b.addDrink("Coke", 330, 2); //2x Coca cola 330 ml

	b.addDrink("Fanta", 500);   //1x Fanta 500 ml

	b.addAlocoholDrink("Zagorka", 500, 5); //1x Zagorka, 5% alc,  500 ml

	b.getAcloholDrink(); // Zagorka 
	
	b.getDrink() // Coke
	b.getDrink() // Coke
	b.getDrink() // Fanta
	
	b.getAlocholDrinksSold(); // 1
	b.getDrinksMlSold(); // 830

}
 ```