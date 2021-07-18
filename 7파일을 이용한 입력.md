파일의 
package jeongmin7;

import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class main {

	public static void main(String[] args) {
		File file = new File("input.txt");        input.txt 파일 file에 할당
		try {
			Scanner sc = new Scanner(file);         file의 값을 입력값으로 할당
			while(sc.hasNextInt())                  
			{
				System.out.println(sc.nextInt()*100); 출력값에 100을 곱함
			}
		} catch (FileNotFoundException e) {
			System.out.println("파일을 읽어오는 도중 오류가 발생했습니다.");   파일을 찾을수 없을 시 문장 출력
		}
		

	}

}
