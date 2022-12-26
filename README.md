# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #4 выполнил(а):
- Филоник Кирилл Русланович
- РИ210931

Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Познакомиться с принципами работы перцептона, проанализировать его работу и построить визуальную модель работы в Unity

## Задание 1
### В проекте Unity реализовать процеатон, который умеет производить вычесление элементарных логических функций.

- Логическая операция **OR** 

  ![image](https://user-images.githubusercontent.com/105949115/209485282-e3b5020f-badc-45a0-98a6-1381b2a748ab.png)

  - Значения для тренеровок:
  
  ![image](https://user-images.githubusercontent.com/105949115/209484731-24f52868-3b97-4d7b-9c2f-f9c10cb142b9.png)
  
  Тест обученного перцептрона:
  
  ![image](https://user-images.githubusercontent.com/105949115/209484765-fd0caa0b-4f5c-4a51-ab63-7356bc1a7351.png)
  
  Вывод: прецептрон прошел все тесты, для этого ему потребовалось 3 эпохи


- Логическая операция **AND**

  ![image](https://user-images.githubusercontent.com/105949115/209485325-b484a904-856e-4bf2-a7a7-0890a188aa25.png)

  - Значения для тренеровок:
  
  ![image](https://user-images.githubusercontent.com/105949115/209485404-4b5e3d0d-ec76-470f-9531-4d4b0def625f.png)
  
  Тест обученного перцептрона:
  
  ![image](https://user-images.githubusercontent.com/105949115/209485399-aaf2f8d9-e3b3-4cad-88f7-66c003b4d841.png)
  
  Вывод: прецептрон прошел все тесты, для этого ему требовалось от 6 до 8 эпох

- Логическая операция **NAND**

  ![image](https://user-images.githubusercontent.com/105949115/209485444-33c95b38-50fb-4ca4-910b-7a4cf8d7ddbe.png)

  - Значения для тренеровок:
  
  ![image](https://user-images.githubusercontent.com/105949115/209485507-27c9467c-6a58-440a-b1c1-8eac9738781d.png)
  
  Тест обученного перцептрона:
  
  ![image](https://user-images.githubusercontent.com/105949115/209485499-c5546be6-6587-4f1c-8236-e5cad3f87f14.png)
  
  Вывод: прецептрон прошел все тесты, для этого ему требовалось от 3 до 5 эпох


- Логическая операция **XOR**

  ![image](https://user-images.githubusercontent.com/105949115/209485529-8d1347c6-59b2-4c8c-9ef1-40658ea2af64.png)

  - Значения для тренеровок:
  
  ![image](https://user-images.githubusercontent.com/105949115/209485634-312c293e-d42e-4d3b-b1fb-def1c216e75c.png)
  
  Тест обученного перцептрона:
  
  ![image](https://user-images.githubusercontent.com/105949115/209485624-4ba1db2a-3747-419d-bef2-ac7513e3ac6b.png)
  
  Вывод: прецептрон не прошел тесты, изначально допустимое количество эпох для обучения было 8, но даже после увеличения этого значения до 16, процептон не смог корректно обучиться и соответственно пройти тесты. Исходя из этого можно сделать вывод, что одиночный процептрон не умеет решать нелинейные задачи.


## Задание 2
### Простроить графики зависимости количества эпох от ошибки обучения. Указать от чего зависит необходимое колиство эпох обучения.

Для каждой элементарной логической функции я сделал выборку из трех попыток обучить процептрон и составил ![таблицу и график зависимости количества эпох от ошибки обучения](https://docs.google.com/spreadsheets/d/11GmiUibKbhMJujov385QJ8vmGHJKkuKN_cg7g2zHpcs/edit?usp=sharing)

![image](https://user-images.githubusercontent.com/105949115/209506258-9c704f65-1433-4a17-8412-4e0ca2f0fb82.png)

![image](https://user-images.githubusercontent.com/105949115/209505609-87d45926-2796-42cd-b487-a289364ba1e8.png)

![image](https://user-images.githubusercontent.com/105949115/209506040-4e0ff82a-268a-4e45-8020-f10f250ae2fa.png)

**Вывод**: самая легкоя логическая функция для прецептрона - OR, для нее максимум потребовалось 4 эпохи, для NAND и AND стоит выбрать большее колчиство эпох воизбежание ошибок, в среднем по графиком можно заметить, что количство ошибок после первой эпохи росло и затем уменьшалось, для XOR же росло.

Необходимое количество эпох обучения зависит от количства ошибок, их должно уменьшаться и прийти к нулю, если задача линейная, иначе процептрон не сможет ее решить. По количству ошибок на первых эпохах можно понять, что для обучению процептрону необходимо больше эпох.

## Задание 3
### Построить визуальную модель работы перцептрона на сцене Unity 

Я создал новый С# скрипт CubeGame.cs. Он отслеживает соприкосновение двух кубов, каждый из которых помечен, как "верный или не верный", при их контакте он высчитывает значение перцептрона, и если оно равно false, то оба объекта удаляются.

```cs

using UnityEngine;

public class CubeGame : MonoBehaviour
{
    [SerializeField] public bool IsTrueCube;
    [SerializeField] private Perceptron perceptron;

    void OnCollisionEnter(Collision other)
    {
        if(other.gameObject.GetComponent<CubeGame>() != null)
        {
            var otherGameCube = other.gameObject.GetComponent<CubeGame>();
            var isTrueOtherNumValue = otherGameCube.IsTrueCube ? 1 : 0;
            var isTrueThisNumValue = IsTrueCube ? 1 : 0;

            if (perceptron.CalcOutput(isTrueThisNumValue, isTrueOtherNumValue) == 0)
            {
                Destroy(gameObject);
                Destroy(other.gameObject);
            }
        }
    }
}

```

Каждый из кубов имеет Box Colider и Rigidbody для отслеживания их коллизии и симуляции физического поведения объектов.

![image](https://user-images.githubusercontent.com/105949115/209523065-dbec6d06-b103-4fb0-961e-d6e1469c7ab4.png)


На сцене находятся четыре пары кубов, красный обозначает - false, а зеленый - true.

![image](https://user-images.githubusercontent.com/105949115/209523217-319275fc-42f1-41a9-9471-551c8c1db31a.png)

Далее можно увидеть результат работы перцетрона, на первой иллюстрации он высчитал работу OR, AND и NAND.

![image](https://github.com/mushr0o0m/DA-in-GameDev-lab4/blob/main/OR.gif)

![image](https://github.com/mushr0o0m/DA-in-GameDev-lab4/blob/main/AND.gif)

![image](https://github.com/mushr0o0m/DA-in-GameDev-lab4/blob/main/NAND.gif)


## Выводы



## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
