# 1ctop
  /// Как организовать цикл в 1с 8.3, 8.2
 
    // Для Цикл
    Для Счетчик = 1 По 5 Цикл
        Сообщить(Счетчик); // 1 2 3 4 5
    КонецЦикла;
 
    // Для Каждого Цикл
 
    Дни = Новый Массив();
    Дни.Добавить("Понедельник");
    Дни.Добавить("Вторник");
    Дни.Добавить("Среда");
 
    Для Каждого Элемент Из Дни Цикл
        Сообщить(Элемент); // Понедельник Вторник Среда
    КонецЦикла;
 
    // Пока Цикл
    Счетчик = 0;
    Пока Счетчик < Дни.Количество() Цикл        
        Сообщить(Дни[Счетчик]); // Понедельник Вторник Среда
        Счетчик = Счетчик + 1;     
    КонецЦикла;     
 
    /// Как организовать обратный цикл в 1с 8.3, 8.2     
 
    Счетчик = Дни.Количество() - 1;     
    Пока Счетчик >= 0 Цикл
        Сообщить(Дни[Счетчик]); // Среда Вторник Понедельник
        Счетчик = Счетчик - 1;
    КонецЦикла;
 
    /// Как прервать цикл в 1с 8.3, 8.2
 
    Для Счетчик = 1 По 5 Цикл
        Если Счетчик > 2 Тогда
            Прервать;
        КонецЕсли;
        Сообщить(Счетчик); // 1 2
    КонецЦикла;
 
    /// Как принудительно продолжить цикл в 1с 8.3, 8.2
 
    Для Счетчик = 1 По 5 Цикл
        Если Счетчик <> 3 Тогда
            Продолжить;
        КонецЕсли;
 
        Сообщить(Счетчик); // 3
    КонецЦикла;   
 
КонецПроцедуры
 
/// Скачать и выполнить эти примеры на компьютере

============================================================================================
Практическая №1
Шаг1 = 10;
Шаг2 = 10;
Для Шаг1 = 10 По 100 Цикл
	Для Шаг2 = 10 По 100 Цикл
		Шаг3 = (101 - Шаг2) - (101 - Шаг1);
		Если Шаг3 = 20 Тогда          
			Сообщить(Строка(Шаг1) + " - " + Строка(Шаг2) + " = " + Строка(Шаг3));			
		КонецЕсли;
	КонецЦикла;
КонецЦикла;
==============================================================================================
Практическая №2
Сообщить((2<3) ИЛИ (2<4) И (2<5));
Сообщить((2<3) ИЛИ (2<4) И (2>5));
Сообщить((2>3) ИЛИ (2>4) И (2>5));
=============================================================================================
Практическая №3
А1 = 0; А2 = 0; А3 = 0;
ВвестиЧисло(А1);ВвестиЧисло(А2);ВвестиЧисло(А2);
А4 = А1 + А2 + А3;
Если А4 >= 36 Тогда 
	ОткрытьЗначение("Ваше число больше и равно 36");
Иначе
	ОткрытьЗначение("Упс...");
КонецЕсли;
