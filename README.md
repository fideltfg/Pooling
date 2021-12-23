# Pooling
Object pooling scripts for Unity

This is a system to allow you to pool any object/prefab in unity.

How to:

1: Add the Pooler prefab to you scene.

2: Creat a prefab that you want to pool.

3: In your script create a variable to hold the prefab to be pooled.

4: Get a pooled instance of you object with the following code
GameObject pooledObject = Pooling.Pooler.root.GetPooledInstance(prefab);

5: Remember to activate the new game object
pooledObject.SetActive(true);

If this is the first time the code is called the pooler will creat a poola and start growing it as you call for more objects.
There is no limit to the number of prefabs you an pool or objects you can spawn.

To return an object to the pool simply disable to object created above. This will allow the Pooler to cleanup or re use the object.

This package also contains a sound pooler which acts more like an AudioSource with a built in playlist. 
