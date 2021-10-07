1. Юсупов Карим Азатович
2. Группа: 11-111
3. Писал на паскале и питоне, паскаль изучали в школе, а питон изучал для егэ (опыт паскаля 60/40, питон 50/50). Также увлекался kali linux, но это нельзя назвать програмированием.




package C1W1;

import java.util.Scanner;
public class C1W1 {
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);
boolean b = true;
while (true) {
int n = sc.nextInt();
if (n == -1) {
break;
}
if (check(n) == false) {
b = false;
}
}
if (b == true) System.out.println("YES");
else System.out.println("NO");
}

public static boolean check(int n) {
for (int i = 1; i <= n; i++) {
if (checkSimple(i) == true && i % 10 == 1 && n % i == 0) {
return true;
}
}
return false;
}

public static boolean checkSimple(int i) {
if (i <= 1)
return false;
else if (i <= 3)
return true;
else if (i % 2 == 0 || i % 3 == 0)
return false;
int n = 5;
while (n * n <= i) {
if (i % n == 0 || i % (n + 2) == 0)
return false;
n = n + 6;
}
return true;
}
}
