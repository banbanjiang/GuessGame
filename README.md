# GuessGame
import java.util.Scanner;

public class Games {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner input = new Scanner(System.in);
		int userput;
		int random = (int)(Math.random()*10000);
		boolean gameover=false;
		while(!gameover) {
			System.out.println("请输入四个数字：");
			if(!input.hasNextInt()) {//hasNextint 是整数返回真，否则返回假
				System.out.println("输入的不是数字");
				input.close();
				return;
			}
		    userput = input.nextInt();
			if(userput<1000 || userput>9999){
				System.out.println("输入的不是四位数字");
			}
			if(userput > random) {
				System.out.println("数字过大，请重新输入");
			}
			else if(userput < random) {
				System.out.println("数字过小，请重新输入");
			}
			else {
				System.out.println("恭喜你猜对了");
				gameover = true;
			}
		}
		input.close();
	}

}
