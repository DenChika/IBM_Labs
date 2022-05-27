# IBM1
## Цель работы
Разобраться с кубитом, что это, как выглядит его построение.\
Разобрать один или несколько операторов.
## Введение в теорию
Начнём с понятия кубит. По сути, это квантовая версия бита. Каждый кубит представлен в виде линейной комбинации |0> и |1> состояний:

![image](https://user-images.githubusercontent.com/79001610/170662629-75b39bbb-79f2-40bf-bc7f-c00ca8edb61a.png)

Эта линейная комбинация равна:

![image](https://user-images.githubusercontent.com/79001610/170670924-4d4c9654-8169-4161-898d-0c6a09b63c95.png)

Причём

![image](https://user-images.githubusercontent.com/79001610/170671047-1a69e4e6-cf46-4eae-a3cc-7e14b471bd13.png)

, где $\alpha $ и $\beta $ - комплексные числа. Или

![image](https://user-images.githubusercontent.com/79001610/170671394-b7cb2d00-43bb-45ec-ac33-3ea5bfc253a9.png)

Отсюда видно, что |$\alpha^{2} $| - вероятность того, что кубит будет в состоянии |0>, а |$\beta^{2} $| - вероятность того, что кубит будет в состоянии |1>.

В IBM Quantum квантовые компьютеры используют _сверхпроводящий трансмонный кубит_. Данная система не является естественным кубитом, он лишь приблизительный. 
![image](https://user-images.githubusercontent.com/79001610/170669259-4c282a10-74d9-49f1-a253-ff85ae3f2ffc.png)
В IBM Quantum есть множество операторов - унитарные матрицы 2х2, и несколько из них мы разберём подробно.
## Оператор NOT
![image](https://user-images.githubusercontent.com/79001610/170669558-5b4b9a61-2834-475a-a789-820d02e38516.png)

По своей сути NOT просто переводит кубит в противоположное состояние.

![image](https://user-images.githubusercontent.com/79001610/170669966-c3eb4488-8d79-452e-b2c0-790f46e1eff2.png)

## Оператор Н (Hadamard)
![image](https://user-images.githubusercontent.com/79001610/170670209-0792b0f5-0961-48ba-9fb3-7b10e5c6c93d.png)

![image](https://user-images.githubusercontent.com/79001610/170670632-ad6f0491-42c4-4b23-9494-7018cbfa6270.png)

Нетрудно показать, что вероятности находиться в состоянии |0> или в состоянии |1> в данном случае у кубита будут равны 0.5, если кубит идеален, однако если мы поставим измерение к этому кубиту, то вероятности будут немного различаться, это связанно со внешними условиями, так как наш кубит был определён изначально не идеальным.
## Квантовая фаза
![image](https://user-images.githubusercontent.com/79001610/170673050-53399068-a461-4f30-86ee-2ee85add86be.png)

![image](https://user-images.githubusercontent.com/79001610/170673148-4cbad6fc-45f2-49ae-9ae7-dc0e49a5cca4.png)

![image](https://user-images.githubusercontent.com/79001610/170673222-0769a8d7-7f56-46e5-861b-1ec93dd52bf2.png)

Оператор Р - обобщение всех операторов поворота фазы, просто в нём мы указываем угол, на который фазу хотим повернуть. Унитарная матрица выглядит так:

![image](https://user-images.githubusercontent.com/79001610/170673480-9686ae0e-bca9-4139-acd3-3987eaf05ea5.png)

![image](https://user-images.githubusercontent.com/79001610/170676265-49a6e7ae-ec2f-4139-a1d0-96087f0865d6.png)

## Усовершенственные однокубитные операторы
![image](https://user-images.githubusercontent.com/79001610/170674122-957971d7-3128-4836-b279-d5bc8e6d9fc6.png)

Ссылка на вывод представления кубита: https://ru.wikipedia.org/wiki/Сфера_Блоха

По сути сфера Блоха - способ визуализации состояний кубита в виде точек на сфере.

![image](https://user-images.githubusercontent.com/79001610/170674755-eb0d6d1c-96fe-443f-be56-1aed736a7b20.png)

Унитарная матрица выглядит так:

![image](https://user-images.githubusercontent.com/79001610/170674903-286d8ca1-d598-46d9-b955-b9534381073f.png)

При $\lambda = \pi/2 $ и $\phi = -\pi/2 $ мы получаем поворот состояния вокруг оси x:

![image](https://user-images.githubusercontent.com/79001610/170675539-addd1d3b-0a81-4ac1-9538-8a75ff4b4dc3.png)

При $\lambda = 0 $ и $\phi = 0 $ мы получаем поворот состояния вокруг оси y:

![image](https://user-images.githubusercontent.com/79001610/170675713-1f3e9b90-bbca-43d4-8b29-2e639584cfaf.png)

При $\lambda = 0 $ и $\theta = 0 $ мы получаем поворот состояния вокруг оси z:

![image](https://user-images.githubusercontent.com/79001610/170675886-f3388527-2f6c-4c1d-b1e7-16c5867c06e1.png)

С помощью оператора U можно описать любой поворот состояния кубита.
## Оператор CNOT

Этот оператор навешивается на 2 кубита: целевой и управляющий.

![image](https://user-images.githubusercontent.com/79001610/170677716-b3b96807-6165-4f20-8d0d-17dd997a50ea.png)

Если управляющий кубит находится в состоянии |1>, то на целевой навешивается оператор NOT. Если же состояние кубита неопределено, то CNOT создаёт запутанность.
## Вывод
Мы разобрались с таким понятием как кубит, поняли из чего он состоит. Так же выяснили, что такое операции над ними и как его можно повернуть на любой угол в пространстве.

_Ссылка на IBM Quantum_: https://quantum-computing.ibm.com/composer/files/e36d87eb5983d034a0e85fbefda2dad5
