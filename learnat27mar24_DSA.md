# Day one of 100 Day Challange Math related problems
### GCD or HCF Brute approach
```java 
public class Main {
  public static void main(String args[]) {
    int num1 = 3, num2 = 6;
    int ans = 1;
    for (int i = 1; i <= Math.min(num1, num2); i++) {
      if (num1 % i == 0 && num2 % i == 0) {
        ans = i;
      }
    }
    System.out.print("The GCD of the two number is "+ans);
  }
}
```

### GCD or HCF Optimal approach
```java
public class Main {
  static int gcd(int a, int b) {
    if (b == 0) {
      return a;
    }
    return gcd(b, a % b);
  }
  public static void main(String args[]) {
    int a = 4, b = 8;
    int ans = gcd(a, b);
    System.out.print("The GCD of the two numbers is "+ans);
  }
}

