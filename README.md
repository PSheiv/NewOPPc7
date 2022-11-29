# Lesson_7

Установить библиотеку protobuf.

С помощью компилятора protobuf в отдельном пространстве имен сгенерировать классы 
FullName с полями имя, фамилия, отчество (отчество опционально).
Student с полями полное имя, массив оценок, средний балл.
StudentsGroup с полем массив студентов.


Создать класс StudentsGroup (без использования protobuf), который реализует интерфейсы:
class IRepository {
	virtual void Open() = 0; // бинарная десериализация в файл
	virtual void Save() = 0; // бинарная сериализация в файл
};


class IMethods {
	virtual double GetAverageScore(const FullName& name) = 0;
	virtual string GetAllInfo(const FullName& name) = 0;
	virtual string GetAllInfo() = 0;
};

