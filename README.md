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

package p126;

public class ConditionalOperEx {
	public static void main(String ar[]) {
		int score=85;
		char grade=(score>90) ? 'A':(score>80) ? 'B':'C';
		System.out.println(score + "점은 " + grade + "등급입니다.");
	}
}

package p136;

public class IfEx {
	public static void main(String ar[]) {
		int score = 93;
		
		if(score>=90) {
			System.out.println("점수는 90보다 크고 A등급 입니다.");
		}else if(score>=80){
			System.out.println("점수는 80보다 작고 B등급 입니다");
		}else if(score>=70){
			System.out.println("점수는 70보다 작고 C등급 입니다");
		}else if(score>=60){
			System.out.println("점수는 60보다 작고 D등급 입니다");
		}else{
			System.out.println("점수는 50보다 작고 F등급 입니다");
		}	
//		if(score<90) {
//			System.out.println("점수는 90보다 작고 B등급 입니다.");
//		}
	}
}

package p140;

public class IfDiceEx {
	public static void main(String ar[]) {
		int num = (int)(Math.random()*45)+1; //0.0~0.9 
		//Math.random class는 크기를 가늠할수 없을 정도이기 떄문에 정수보다 크다
		//double num = (double)Math.random();
		System.out.println("난수발생 : " + num);
	}
}

package p142;

public class SwitchEx {
	public static void main(String ar[]) {
		int num = (int)(Math.random()*6) + 1;
		
		switch(num ) {
		case 1:System.out.println("1번");break;
		case 2:System.out.println("2번");break;
		case 3:System.out.println("3번");break;
		case 4:System.out.println("4번");break;
		case 5:System.out.println("5번");break;
		default:System.out.println("6번");break;
		}
	}
}

package p148;

public class ForPrintEx {
	public static void main(String ar[]) {
	
		int sum = 0;
		sum = sum +1;
		sum = sum +2;
		sum = sum +3;
		sum = sum +4;
		sum = sum +5;
		System.out.println("합:"+sum);
		
		// ↓ i=0 시작값(처음한번만 쓰고 안씀)(0부터 시작), i<=5 조건값(참일떄까지), i++ 증감식(조건이 참일때만 증감)
		for(int i=0; i<=5; i++) {
			System.out.println();
		}
	}
}

package p153;

public class ForMultipleEx {
	public static void main(String ar[]) {
		for(int i=2; i<=9; i++) {//조건값 i<3 도 가능 
			System.out.println("=== " + i + "단 ===");//바깥 for, 천천히 돌고
		for(int j=1; j<=9; j++) { //안쪽 for, 빠르게 돌고
			System.out.println(i + " x " + j + " = " + (i*j));
			}
		System.out.println();
		}
	}
}

package p154;

public class WhilePrintEx {
	public static void main(String ar[]) {
		
		int i=1;
		
//		while(i<=5) {
//			System.out.println("while()");
//			i++;
//		}
	
		do {
			System.out.println("do~while() 은 거짓이라도 한번은 실행된다.");
			i++;
		}while(i<=3);
	}
}

package p157;

public class BreakEx {
	public static void main(String ar[]) {
		while(true) {
			int num=(int)(Math.random()*6)+1;
			System.out.println("출력숫자 :"+num);
			if(num==6) {
				break;
			}
		}
		System.out.println("프로그램 종료!!");
	}
}

package p159;

public class ContinueEx {
	public static void main(String ar[]) {
		for(int i=1; i<=10; i++) {
			if(i%2 !=0) {
				continue;
			}
			System.out.println(i);
		}
	}
}

package p161;

public class 연습문제5번 {
	public static void main(String ar[]) {
		for (int i=1; i<=4; i++) {
			for(int j=1; j<=i; j++) {
				System.out.print("*");
				if(i==j) {
				System.out.println();
			}
			
		}
	}
		
	}
}

package p180;

public class ArrayCreEx {
	public static void main(String ar[]) {
		int[] scores= {83, 90, 87}; //배열의 범위를 지정해줄수있는 방법 //int scores [];
		
		//System.out.println("scores[0] :"+scores[0]);
//		System.out.println(scores.length);
		
		for(int i=0; i<scores.length; i++) {
			System.out.println("scores["+i+"] :"+scores[i]);
		}
	}
}
