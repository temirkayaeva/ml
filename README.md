# Решающие списки

Решающий список (decision list, DL) — это наиболее простой логический алгоритм, как по своей структуре, так и по способу построения.

Решающий список — это алгоритм классификации a: X → Y , который задаётся набором закономерностей ϕ1(x),..., ϕT (x), приписанных к классам c1,..., cT ∈ Y соответственно, и вычисляется согласно алгоритму.

__1: для всех t = 1,..., T

__2: если ϕt(x) = 1 то

__3: вернуть ct;

__4: вернуть c0.

«Особый ответ» c0 означает отказ алгоритма от классификации объекта x.

## Жадный алгоритм построения решающего списка

Алгоритм на каждой итерации строит ровно одно правило ϕt, выделяющее максимальное число объектов некоторого класса ct и минимальное число объектов всех остальных классов. Для этого на шаге 4 производится поиск наиболее информативного правила ϕt ∈ Φ, допускающего относительно мало ошибок. Семейство правил Φ может быть каким угодно, лишь бы для него существовала эффективная
процедура поиска закономерностей. После построения правила ϕt выделенные им объекты изымаются из выборки и алгоритм переходит к поиску следующего правила ϕt+1 по оставшимся объектам. В итоге выборка оказывается покрытой множествами вида {x: ϕt(x) = 1}. Поэтому решающий список называют также __покрывающим набором закономерностей или машиной покрывающих множеств (set
covering machine, SCM)__.
