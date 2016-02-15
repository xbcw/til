This will allow me to simplify my Actor classes for Terrornado.  Especially things like `Shock()`, `Freeze()`, `Throw()`, etc.

```
using UnityEngine;
using System.Collections;

//This is a basic interface with a single required
//method.
public interface IKillable
{
    void Kill();
}

//This is a generic interface where T is a placeholder
//for a data type that will be provided by the
//implementing class.
public interface IDamageable<T>
{
    void Damage(T damageTaken);
}
```

```
using UnityEngine;
using System.Collections;

public class Avatar : MonoBehaviour, IKillable, IDamageable<float>
{
    //The required method of the IKillable interface
    public void Kill()
    {
        //Do something fun
    }

    //The required method of the IDamageable interface
    public void Damage(float damageTaken)
    {
        //Do something fun
    }
}
```

[source](https://unity3d.com/learn/tutorials/modules/intermediate/scripting/interfaces)