Person 클래스 생성
package jeongmin16;

public class Person {
	private String name;
	private int age;
	private int height;
	private int weight;
	
	public String getName() {   // 마우스 우클릭-source-generate getter and setter
		return name;            // 을 활용하여 각 변수에 접근할수 있는 함수 생성
	}
	public void setName(String name) {
		this.name = name;
	}
	public int getAge() {
		return age;
	}
	public void setAge(int age) {
		this.age = age;
	}
	public int getHeight() {
		return height;
	}
	public void setHeight(int height) {
		this.height = height;
	}
	public int getWeight() {
		return weight;
	}
	public void setWeight(int weight) {
		this.weight = weight;
	}
	public Person(String name, int age, int height, int weight) {    // 마우스 우클릭-source-generator constructor using field
		super();                                                    // 를 통해 생성자를 만들어 각 변수를 초기화
		this.name = name;
		this.age = age;
		this.height = height;
		this.weight = weight;
	}
  
  Student 클래스 생성 및 Person 클래스와 상속

package jeongmin16;

public class Student extends Person {

	private String studentId;
	private int grade;
	private double GPA;
	
	public String getStudentId() {
		return studentId;
	}
	public void setStudentId(String studentId) {
		this.studentId = studentId;
	}
	public int getGrade() {
		return grade;
	}
	public void setGrade(int grade) {
		this.grade = grade;
	}
	public double getGPA() {
		return GPA;
	}
	public void setGPA(double gPA) {
		GPA = gPA;
	}
	public Student(String name, int age, int height, int weight, String studentId, int grade, double gPA) {
		super(name, age, height, weight);
		this.studentId = studentId;
		this.grade = grade;
		GPA = gPA;
	}                        
	
	public void show() {           //조회시 나오는 목록 작성
		System.out.println("학생 이름 :"+getName());
		System.out.println("학생 나이:"+getAge());
		System.out.println("학생 키 :"+getHeight());
		System.out.println("학생 몸무게 :"+getWeight());
		System.out.println("학생 StudentID : "+getStudentId());
		System.out.println("학생 학년 :"+getGrade());
		System.out.println("학생 학점 :"+getGPA());
	}
	
}

인스턴스 입력 및 출력
package jeongmin16;

public class main {

	public static void main(String[] args) {
		Student student1= new Student("홍길동",29,175,70,"20170101",1,4.5);
		Student student2= new Student("이순신",30,170,70,"20170102",1,4.0);
		student1.show();
		student2.show();

	}

}



  
	
