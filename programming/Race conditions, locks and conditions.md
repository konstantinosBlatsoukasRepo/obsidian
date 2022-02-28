Race condition

Is a situation when two or more threads have access to same object and can modify the objects state in the same time, resulting in a incosistent state.


how to avoid them:

**Locks**

Reentrant lock example:


```java
public class Bank
{
   private Lock bankLock = new ReentrantLock();
   ...
   public void transfer(int from, int to, int amount)
   {
      bankLock.lock();
      try
      {
         System.out.print(Thread.currentThread());
         accounts[from] -= amount;
         System.out.printf(" %10.2f from %d to %d", amount, from, to);
         accounts[to] += amount;
         System.out.printf(" Total Balance: %10.2f%n", getTotalBalance());
      }
      finally
      {
         bankLock.unlock();
      }
   }
}

```

