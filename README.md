# Csharp_Sem_3
// ДЗ

// Задача 1: Задайте одномерный массив из 10 целых чисел от 1 до 100. Найдите количество элементов
// массива, значения которых лежат в отрезке [20,90]. 

// массив [10 21 14 93 23] => 2

/*
int ReadInt(string text)
{
Console.Write(text);
return Convert.ToInt32(Console.ReadLine());
}
int[] GenerateArray(int size, int leftRange, int rightRange)
{
int[] tempArray = new int[size];
Random rand = new Random();
for (int i = 0; i < size; i++)
{
tempArray[i] = rand.Next(leftRange, rightRange + 1);
}
return tempArray;
}
void PrintArray(int[] array)
{
System.Console.WriteLine("[" + string.Join("  ", array) + "]");
}

// Основной код

int size = ReadInt("Введите размер массива: ");
int[] myArray = GenerateArray(size, 1, 100);
PrintArray(myArray);
int count = 0;

for (int i=0; i < myArray.Length; i++)
 {
    if (myArray[i] > 20 && myArray[i] < 90)
    count++;
 }

PrintArray(myArray);

Console.WriteLine($" => {count}");
*/


// Задайте массив на 10 целых чисел. Напишите программу, которая определяет
// количество чётных чисел в массиве.
// массив [6 7 19 34 3 1 4 7 9 1] => 3
// массив [1 8 43 4 55 60 3 2 1 3] => 4

/*
int ReadInt(string text)
{
Console.Write(text);
return Convert.ToInt32(Console.ReadLine());
}
int[] GenerateArray(int size, int leftRange, int rightRange)
{
int[] tempArray = new int[size];
Random rand = new Random();
for (int i = 0; i < size; i++)
{
tempArray[i] = rand.Next(leftRange, rightRange + 1);
}
return tempArray;
}
void PrintArray(int[] array)
{
System.Console.WriteLine("[" + string.Join(", ", array) + "]");
}

// Основной код


int size = ReadInt("Введите размер массива: ");
int[] myArray = GenerateArray(size, 0, 100);

int[] numeven = new int[size];
int count = 0;

for (int i=0; i < myArray.Length; i++) 
{
if (myArray[i] % 2 == 0)
count++;
}
PrintArray(myArray);
Console.WriteLine($"всего {myArray.Length} чисел => {count} из них чётные");
*/


// Задайте массив из вещественных чисел с ненулевой дробной частью. Найдите разницу между
// максимальным и минимальным элементов массива.
// массив [2.2 0.4 9.11 7.2 78.98] => 78.58
// массив [1.22 4.5 3.33] => 3.28



// Основной код

double[] array = new double [5];

Random rand = new Random();
double min = double.MinValue;
double max = double.MaxValue;

for (int i=0; i < array.Length; i++)  
{
    array [i] = Math.Round(rand.Next(0,10) + rand.NextDouble(), 2);
}
{
if (array [4] > max)
        {
            max = array [4];
        }
    if (array [4] < min)
        {
            min = array [4];
        }
}
Console.WriteLine(string.Join(" ", array));
Console.WriteLine($"всего {array.Length} чисел. Максимальное значение = {max}, минимальное значение = {min}");
Console.WriteLine($"Разница между максимальным и минимальным значением = {max - min}");


