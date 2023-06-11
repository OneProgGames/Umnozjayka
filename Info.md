Данное приложение для Android позволяет:

+ Тренировать навыки умножения и деления

![Картинка-1](https://github.com/ButterflyGamesDeveloper/Umnozjayka/blob/main/N1.jpg)

+ Выбирать количество примеров
![Картинка-2](https://github.com/ButterflyGamesDeveloper/Umnozjayka/blob/main/N2.jpg)

+ Смотреть, как улыбается котик, когда пример решён верно
![Картинка-3](https://github.com/ButterflyGamesDeveloper/Umnozjayka/blob/main/N5.jpg)


А это код для создания бесконечного движения рыбок!

```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class scroll : MonoBehaviour
{
    float move_speed = 50f;
    [SerializeField] Transform start;
    [SerializeField] Transform end;

    void Update()
    {
        transform.Translate(Vector2.right * move_speed * Time.deltaTime);
        if (transform.position.x >= end.position.x)
        {
            transform.position = new Vector2(start.position.x, transform.position.y);
        }
    }
}
```