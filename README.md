# Java_Day02
자바(Java)프로그래밍 초급과정 2일차 (4월11일, 9:00~16:30)

package p112;

public class InCreDeCreEx {

	public static void main(String[] args) {
		int x=10;
		int y=10;
		int z;
		
		System.out.println("=================");
		x++; //11
		++x; //12
		System.out.println("x="+x);
		
		System.out.println("=================");
		y--; //9
		--y; //8
		System.out.println("y="+y);
		
		System.out.println("=================");
		z=x++; // 연산자의 우선순위 여기선 대입(=)먼저
		//z=++x; //연산자의 우선순위 증감(++)먼저 한다음 대입
		System.out.println("z="+z);
		System.out.println("x="+x);
		
		x=y=z;
	}

}

package p114;

public class DenyLogicEx {
	public static void main(String ar[]) {
		boolean play=true;
		System.out.println(play);
		
		play=!play;
		System.out.println(play);
		
		play=!play;
		System.out.println(play);
	}
}

package p117;

public class CharOperEx {
	public static void main(String ar[]) {
		char c1='A'+1;
		System.out.println("c1="+c1);
		
		char c2='A';
		//char c3=c2+c1 
		int c3=c2+1;
		System.out.println("c3="+c3);
	}
}

package p118;

public class StringConCatEx {
	public static void main(String ar[]) {
		String str1="JDK"+11.0;
		String str2=str1+"특징";
		System.out.println(str2);
		
		String str3=3+3.0+"JDK";
		//3+3.0 까지는 산술연산, .0+"JDK"는 결합연산
		System.out.println(str3);
	
	}
}

package p119;

public class CompareOperEx {
	public static void main(String ar[]) {
		int num1 = 10;
		int num2 = 20;
		boolean result1 = (num1 == num2); //항상 왼쪽이 기준!
		System.out.println(result1);
		boolean result2 = (num1 != num2);
		System.out.println(result2);
		boolean result3 = (num1 >= num2);
		System.out.println(result3);
		boolean result4 = (num1 <= num2);
		System.out.println(result4);
		
		//p120
		String strVar1 = "홍길동";
		String strVar2 = "홍길동";
		System.out.println("문자열비교1:"+(strVar1==strVar2));
		System.out.println("문자열비교2:"+(strVar1.equals(strVar2))); //같지않다는 (!strVar1~~~)))
		//문자열에서 같은값을 표현할때 == 안씀, equals 사용
		
		//String strVar1 = new String ("홍길동");
		//String strVar2 = new String ("홍길동");
		//System.out.println("문자열비교1:"+(strVar1==strVar2));
		//system.out.println("문자열비교2:"+(strVar1.equals(strVar2)));
	}
}

package p123;

public class LogicOperEx {
	public static void main(String ar[]) {
		int charCode='A';
		
		
		if((charCode>=65)&(charCode<=90)) {
		 System.out.println("참");
		}
		
		if((charCode>=97)&&(charCode<=122)) {
			 System.out.println("거짓"); //참이 아니여서 결과 추출 X
			}
		
		int value = 6;
		if((value%2==0)&&(value%3==0)) {
			 System.out.println("2 또는 3의 배수");
		}
	}
}

package p124;

public class AssignOperEx {
	public static void main(String ar[]) {
		int result=0;
		result+=10; //result=result+10;
		System.out.println("결과값 : "+result);

	}

	
		
	public static void main2(String ar[]) {
		byte result=0;
		byte num=10;
		result+=num; //result=result+10; +=은 처음의 유형을 그대로 관리하기 위해 사용, 그래서 byte가 int로 변환되지 않고 사용가능
		System.out.println("결과값 : "+result);
	
	}
}

