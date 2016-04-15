# Practice
samples for Java project


problem：
测试将一个浮点数分解成整数部分和小数部分；
测试把一个数字字符串变成汉字字符串

code：
/*
import java.util.Arrays;
public class Main {
		
	/*
	 * 定义将数字转为人民币读法的类Num2Rmb--Main
	 * 属性：0-9的汉字，十百千的单位
	 * 方法：将浮点数转为整数和小数	divide()；
	 *     将数字字符串转为汉字读法	toHanStr()
	 */
	//public class Num2Rmb
	//{
	private String[] hanArr = {"零","壹","贰","叁","肆","伍","陆","柒","捌","玖"};
	private String[] unitArr = {"十","百","千","万"};
	
	public String[] divide(double num){
		//将浮点数强制转换为long型，即得到整数部分
		long zheng = (long)num;
		//浮点数减去整数部分，再乘以100后取整得到2位小数，四舍五入
		long xiao = Math.round((num-zheng)*100);
		String[] result = new String[2];
		result[0] = zheng+"";
		result[1] = String.valueOf(xiao);
		return result; 
	}
	public String toHanStr(String str){
		String result = "";
		//读取字符串的各位char型减去48得到整形
		for(int i=0; i<str.length(); i++){
			int num = str.charAt(i) - 48;
			if(i!=str.length()-1 && num!=0){
				result += hanArr[num] + unitArr[str.length()-2-i];
			}else if(i==str.length()-1 && num==0){
				;
			}else{
				result += hanArr[num];
			}
		}
		return result;
	}
	//}
	
	public static void main(String[] args){
		//just for test
		//首先创造Num2Rmb的引用类型
		Main n2r = new Main();
		double num = 123456.789;
		System.out.println(Arrays.toString(n2r.divide(num)));
		System.out.println(n2r.toHanStr("90210"));
	}
}
*/
