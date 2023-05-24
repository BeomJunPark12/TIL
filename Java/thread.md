# 스레드란?

스레드란 프로세스(실행중인 프로그램)내에서 실제로 작업을 수행하는 주체를 의미함

모든 프로세스에는 한 개 이상의 프로세스가 존재하여 작업을 수행

두 개 이상의 스레드 -> 멀티스레드

# 스레드 생성과 실행
자바에서는 스레드를 생성할 때 두 가지 방법이 있다

1. Runnable 인터페이스를 구현하는 방법
2. Thread 클래스를 상속받는 방법

Thread클래스를 상속받으면 다른 클래스를 상속받을 수 없기 때문에 Runnable인터페이스를 구현하는 방법이 일반적이다.

```java
class ThreadWithClass extends Thread {

    public void run() {

        for (int i = 0; i < 5; i++) {

            System.out.println(getName()); // 현재 실행 중인 스레드의 이름을 반환함.

            try {

                Thread.sleep(10);          // 0.01초간 스레드를 멈춤.

            } catch (InterruptedException e) {

                e.printStackTrace();

            }

        }

    }

}

 

class ThreadWithRunnable implements Runnable {

    public void run() {

        for (int i = 0; i < 5; i++) {

            System.out.println(Thread.currentThread().getName()); // 현재 실행 중인 스레드의 이름을 반환함.

            try {

                Thread.sleep(10);

            } catch (InterruptedException e) {

                e.printStackTrace();

            }

        }

    }

}

 

public class Thread01 {

    public static void main(String[] args){

        ThreadWithClass thread1 = new ThreadWithClass();       // Thread 클래스를 상속받는 방법

        Thread thread2 = new Thread(new ThreadWithRunnable()); // Runnable 인터페이스를 구현하는 방법

 

        thread1.start(); // 스레드의 실행

        thread2.start(); // 스레드의 실행

    }

}

```
