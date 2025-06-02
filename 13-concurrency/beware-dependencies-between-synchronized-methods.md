# Beware Dependencies between Synchronized Methods

Dependencies between synchronized methods cause subtle bugs in concurrent code.

## More than one synchronized method on the same class?&#x20;

Your system may be written incorrectly.

{% hint style="success" %}
**Recommendation**:

There will be times when this is not possible. If so, use the following techniques:
{% endhint %}

### Client-Based Locking

Have the Client lock the server before calling the first method. Make sure the lock's extent includes code calling the last method.

### Server-Based Locking

Within the Server create a method that locks the server, calls all the methods, and then unlocks. Have the client call this new method.

### Adapted Server

Create an intermediary  that performs the locking. This is an example of server-based locking where the original server cannot be changed.
