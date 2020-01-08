## Интегралы
### Свойства определенного интеграла 

1. $\int\limits_a^b c \cdot f(x) dx = c \cdot \int\limits_a^b f(x) dx$
2. $\int\limits_a^b f_1(x) + f_2(x) dx = \int\limits_a^b f_1(x) dx + \int\limits_a^b f_2(x) dx$
3. $\int\limits_a^b f(x) dx = - \int\limits_b^a f(x) dx$
4. $\int\limits_a^b f(x) dx = \int\limits_a^c f(x) dx + \int\limits_c^b f(x) dx$, $c \in (a; b)$
5. *Th. о среднем* $\int\limits_a^b f(x) dx = f(c) \cdot (b - a)$, $c \in [a;b]$. Доказывается по теорее лагранда ($F(b) - F(a) = F'(c) \cdot (b - a)$)
6. Если $f(x)$ на $[a;b]$ сохраняет знак, то $\int\limits_a^b f(x) dx$ имеет тот же знак.
7. Если $f_1(x) \leq f_2(x)$, то $\int\limits_a^b f_1(x) dx \leq \int\limits_a^b f_2(x) dx$, и т.д.

#### Подстановка в определенном интеграле. 

$x = \phi(t)$ и производная непрерывны на $t \in [\alpha; \beta]$; мн. значений при $t \in [\alpha; \beta]$ - отрезок $[a; b]$; $phi(a) = \alpha ...$

$$
\int\limits_a^b f(x) dx = \int\limits_{\alpha}^{\beta} {f(\phi(t)) \cdot \phi'(t)} d{t}
$$

<!-- #### Приложения определенного интеграла. -->

### Несобственный интеграл

#### I рода

$$
\int\limits_{a}^{+\inf} {f(x)} d{x} = \lim_{b \to \inf} \int\limits_{a}^{b} {f(x)} d{x} 
$$
остальные анологично. на $(-\inf; +\inf)$ создается разрыв (разбиение на сумму) в точке $c$.

<!-- #### Cходимость -->

#### II рода

$$
\int\limits_a^b f(x) dx = \lim_{\epsilon \to 0} \int\limits_{a}^{b - \epsilon} {f(x)} d{x}
$$
остальные анологично. если разрыв функции, то создается разрыв интегралла в точке $c$.

<!-- #### Сходимость -->

### Интегралы, зависящие от параметра.

Если функция $f(x; \alpha)$ непрерывна в замкнутом прямоугольнике $a \leq x \leq b$ , $c \leq \alpha \leq d$ и имеет в нём непрерывную частную производную по параметру $\alpha$, то на $[c; d]$ имеем:

$$
\forall{y \in [c;d]} \; \exist I(y) = \int\limits_a^b f(x; y) dx, \text{тогда} \;
I'_{\alpha} = \int\limits_{a}^{b} {f'_{\alpha}(x; \alpha)} d{x}
$$

для несобственных требуется равномерная сходимость.

### Двойной интеграл

$$
\iint\limits_{D} f(x;y)dx dy = \int\limits_a^b dx \int\limits_{\phi_1(x)}^{\phi_2(x)} {f(x;y)} d{y}
$$
свойства анологичны свойствам определенного интеграла.

#### Замена переменных

Определим замену $x = \phi(u; v)$ и $y = \psi(u; v)$.

$I \ne 0$ и $f(x;y)$ то справедлива замена:
$$
I(u; v) = 
\begin{vmatrix}
   \frac{\partial x}{\partial u}  & \frac{\partial x}{\partial v} \\
   \frac{\partial y}{\partial u}  & \frac{\partial y}{\partial v} 
\end{vmatrix}; \; \;
\iint\limits_D f(x;y) dx dy = \iint\limits_{D^*} f(\phi(u; v);\psi(u; v)) \cdot|I(u;v)| du dv 
$$

Подярные: $x = r \cos{\alpha}$, $y = r \cos{\alpha}$ и $I = r$.

#### Приложения
### Тройной интеграл

$$
\iiint\limits_{V} {f(x;y;z)} dx dy dy = \iint\limits_{D} \left( {\int\limits_{z_1(x;y)}^{z_2(x;y)} {f(x;y;z)} d{z}} \right) ds, \; D \text{ ограничена } \alpha_1(x) \text{ и } \alpha_2(x)
$$


свойства анологичны свойствам определенного интеграла.

#### Замена переменных. Цилиндрические и цилиндрические координаты

Определитель аналогичен двойному интегралу (столбцы $u, v, w$, строки $x, y, z$). И замена тоже аналогична.

Цилиндрические: $x = r \cos{\alpha}$, $y = r \sin{\alpha}$, $z = z$, $I = r \geq 0$
Сферические: $x = \rho \cos{\alpha} \sin{\theta}$, $y = \rho \sin{\alpha} \sin{\theta}$, $z = \rho \cos{\theta}$ и $I = - \rho^2 \sin{\theta}$


#### Приложения

### Криволинейный интеграл
#### I рода

*Th.* Если $f(x;y)$ непрерывна в каждой точке прямой (т.е.$\exist$ касательная).

свойства аналогичны. + $\int\limits_{L} dl = l$ - длинна кривой.

 - параметрическое $x = x(t), y = y(t), t \in [\alpha; \beta]$ - $x и y$ - непрерывно дифф. $A \text{ соотв. } \alpha, B - \beta$, то $f(x;y) = f(x(t);y(t))$, $dl = \sqrt{x'^2_t + y'^2_t}dt$
 - явное $x = x, y = \alpha(x)$, отсальное выводиться из определения выше ($x' = 1$).
 - $r = r(\alpha), f(r \cos{\alpha}; r \sin{\alpha}$, $dl = \sqrt{r^2 + (r'_{\alpha})^2} d\alpha$

#### II рода

Во втором роде $dl$ заменена на $dx$ или $dy$ (проекция). Сумма двух новых (по $x$ и $y$) - общей вид.

Свойства:
 - $\int_{AB} = - \int{BA}$; 
 - можно разделять на сумму; 
 - Если перпендикулярно $\overline{OX}$ или $\overline{OY}$, то соответсв. инт. = 0; 
 - Этот интеграл не зависит от пути:
$$
\oint\limits_{AmCnA} = \int\limits_{AmC} + \int\limits_{CnA}
$$ 

#### Формула Грина

*Th.* Если функции $P(x;y)$ и $Q(x;y)$, $\frac{\partial P}{\partial y}$ и $\frac{\partial Q}{\partial x}$ непрерывныф в $D$, то ..., где $L$ - граница $D$ (направление (положительное) такое, что при инт. область остается слева). 
$$
\iint\limits_{D} {( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} )} dx dy = \oint\limits_L {Pdx + Qdy}
$$
Для доказательсва подсчитайте разность, получится определения криволин. интегралов.

#### Криволинейные интегралы, не зависящие от пути интегрирования. 

### Поверхностный интеграл
#### I рода

$$
\iint\limits_{S} {f(x;y;z)} ds = \iint\limits_{D} {f(x;y; z(x;y)) \cdot \sqrt{1 + {z'_x}^2 + {z'_y}^2}} dx dy
$$
существуют и с подстановкой в $x$ и $y$. $D$ - проекция плоскости на соотв. координатную плоскость.

Док-во: $\Delta T_i \approx \Delta S_i$, где $T$ - "косательная плоскость", а $S$ - кусок функции. $\Delta T_i \cos{\gamma_i} = \Delta \sigma_i$ - проекция $T$ на $D$, $\gamma$ - угол между нормалью и плоскостью. $\vec{n_i} = (-z'_x, -z'_y, -1)$ $\Rightarrow$ $\cos{\gamma} = \frac{kn}{|k||n|} = 1 / \sqrt{1 + {z'_x}^2 + {z'_y}^2 }$, тогда $\Delta T = ..$ и получаем формулу.

#### II рода

Во втором роде $ds$ заменена на $dx dy$, $dy dz$ или $dx dz$ (проекция). А сумма трех интегр. - общий вид.

 - $\iint$ = $+$ если верхняя сторона (направл. $\cos \gt 0$), $-$ - нижняя.
 - $\iint c(f + g) = c(\iint f + \iint g)$
 - Разделять на сумму 
 - Если $S$ - цилиндр. поверхность с образующими $||$ оси, то соотв. $\iint = 0$. 

$$
\iint\limits_{S} P dydz + Q dxdz+ Z dxdy = \plusmn \iint\limits_{D_{yz}} P(x(y;z); y; z) dy dz + ...
$$

#### Свяь между 1 и 2

$$
\iint\limits_{S} P dydz + Q dxdz+ Z dxdy = \iint\limits_{S} {(P \cos{\alpha} + Q \cos{\beta} + R \cos{\gamma}}) \, ds 
$$

#### Формула Остроградского

*Th.* $P(x;y;z), Q(x;y;z), R(x;y;z)$ непрерывны с частн. производ. первого порядка в $V$, то ..., где $S$ - граница $V$, и интгр. по внешней стороне.

$$
\iiint\limits_{V} {( \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z} )} dx dy dy  = \iint\limits_{S} { P\, dydz + Q\, dxdz + R\, dxdy} 
$$

Док-во $\iiint = \iint_{S_1} + \iint_{S_2} + (\iint_{S_3 \text{внешняя сторона (цилиндр)}} = 0) = \iint_S$ считаем внутренний предел для каждой производной.

#### Формула Стокса

*Th.* $P(x;y;z), Q(x;y;z), R(x;y;z)$ непрерывны с частн. производ. первого порядка в ориентированной $S$, то ..., где $L$ - граница $S$, и интгр. по полож. направлению (слева).

$$
\iint\limits_{S} 
 \left({\frac {\partial Q}{\partial x}} - {\frac {\partial P}{\partial y}}\right)\, dxdy
+ \left({\frac {\partial R}{\partial y}} - {\frac {\partial Q}{\partial z}}\right)\, dydz 
+ \left({\frac {\partial P}{\partial z}} - {\frac {\partial R}{\partial x}}\right)\, dzdx 
 = \oint \limits_L Pdx+Qdy+Rdz.
$$

## Поля
### Скалярное поле

Если каждой точке $M$ заданной области пространства поставлено в соответствие некоторое  число $u$, то в этой области задано скалярное поле. Другими словами, скалярное поле — это функция, отображающая $\mathbb{R} ^{n}$ в $R$. 

$U(x;y;z) = c$ - поверхность уровня. $U(x; y) = c$ - линия.

#### Производная по направлению

Для поля $U$ производная по направлению $\lambda = |M M_1| = \sqrt{{\Delta x}^2 + {\Delta y}^2 + {\Delta z}^2}$, где приращение $\Delta U = U(M_1) - U(M)$, производная $\frac{\partial U}{\partial \lambda}$.

$$
\Delta U = \frac{\partial U}{\partial x} \cdot \Delta x + \frac{\partial U}{\partial y} \cdot \Delta y + \frac{\partial U}{\partial z} \cdot \Delta z + \epsilon_1 \Delta x + \epsilon_2 \Delta y + \epsilon_3 \Delta z 
$$
где, $\epsilon$ - б.м.ф при $\Delta \lambda \to 0$. $\;\Delta (x/y/z) = \Delta \lambda \cos(..)$.  
$\frac{\partial U}{\partial \lambda} = \frac{\partial U}{\partial x} \cos{\alpha} + ...$ В плоском поле $\cos{\beta} = \cos({\pi\over{2}} - \alpha) = \sin{\alpha}, \cos{\gamma} = 0$

#### Градиент скалярного поля

Градиент - вектор, указывающий на наибыстрейшее возрастание функции. $grad U = (\frac{\partial U}{\partial x}; \frac{\partial U}{\partial y}; \frac{\partial U}{\partial z} ) \Rightarrow \frac{\partial U}{\partial \lambda} = \vec{e} \operatorname{grad}{U}$.

 - Градиент направлен по нормали к поверхности уровня
 - Сложение, умножение, деление, как у производной
 - $\operatorname{grad}{F(U)} = \frac{\partial f}{\partial U} \operatorname{grad}{U}$

### Векторное поле

Векторное поле $\vec{a} = \vec{a}(M) = P(x; y; z) \vec{i} + Q(x;y;z) \vec{j} + R(x;y;z) \vec{k}$ — это отображение, которое каждой точке рассматриваемого пространства ставит в соответствие вектор с началом в этой точке.

Вектоная линия - линия, которой колинеарны вектора. $\frac{dx}{P} = \frac{dy}{Q} = \frac{dz}{R}$

#### Поток

Разобъем $S$; $\vec{a}(M_i) \cdot n_i$, где $\vec{n_i}$ - вектор нормали поверхности.

$П = \iint\limits_{S} \vec{a}(M) \cdot \vec{n} \, ds = \iint\limits_{S} (P \cos{\alpha} + Q \cos{\beta} + R \cos{\gamma}) ds = \iint\limits_{S} Pdydz + Qdxdz + Rdxdy$

#### Дивергенция

$$\operatorname{div}{\vec{a}(M)} = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}$$

 - $\vec{a} = const \Rightarrow \operatorname{div}{a} = 0$
 - $\operatorname{div}{c \cdot \vec{a} + \vec{b}} = c \cdot \operatorname{div}{\vec{a}} + \operatorname{div}{\vec{b}}$
 - $\operatorname{div}({U \cdot \vec{a}}) = U \cdot \operatorname{div}{\vec{a}} + \vec{a}\operatorname{grad}{U}$

Свойства доказываются с помощью определений

#### Теорема Остроградского – Гаусса

$$
\iint\limits_{S} {a_n} ds = \iiint\limits_{V} {\operatorname{div}{a}} dv, \; \text{где } a_n \text{ - проекция вектора на нормаль}
$$

#### Циркуляция

$$
Ц = \oint\limits_L \vec{a} \vec{dr} = \oint\limits_L Pdx + Qdy + Rdz \\
\vec{a} \vec{dr} = |\vec{dr}| \cdot \vec{a}_{\vec{dr}} = a_{\tau} \cdot dl = Pdx + Qdy + Rdz 
$$

Если $L$ в силовом поле, то $Ц$ - это работа силы $\vec{a}$ при перемещении материальной точки вдоль $L$.

#### Ротор

$\operatorname{rot}{a} =$ в формуле стокса скобки $=$ определитель по $i,j,k$, операторам частных произв. и $P, Q, R$.

 - $a = const \Rightarrow \operatorname{rot}{a} = 0$
 - $\operatorname{rot}{(c \vec{a} + \vec{b})} = c \cdot \operatorname{rot}{a} + \operatorname{rot}{b}$
 - $\operatorname{rot}({U \cdot \vec{a}}) = U \cdot \operatorname{rot}{\vec{a}} + \operatorname{grad}{U} \times a$
  
$\operatorname{rot}{a}$ - вектор, порпорциональный вектору угловой скорости в векторном поле скоростей.

##### Теорема Стокса

$$
\oint\limits_L a_{\tau} dl = \iint\limits_{S} {\operatorname{rot}_n{\vec{a}}} ds 
$$

### Соленоидальное векторное поле и его свойства

Векторное поле $\vec{a}$ называется соленоидальны, если через любую замкнутую поверхность $S$ его поток равен нулю.

$\operatorname{div}\vec{a} = 0$. $\exist \vec{b} : \vec{a} = \operatorname{rot}{\vec{b}}$. $\vec{b}$ - векторный потенциал.

### Потенциальное векторное поле.

$\operatorname{rot}{\vec{a}} = 0 \Rightarrow \vec{a}$ - потенциальное поле.

- Ц = 0
- потенциальное поле $= \operatorname{grad}{U(x;y;z)}$