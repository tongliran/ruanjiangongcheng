# 单元测试
  时间：2020/09/14
----
## 1.作为软件开发人员，我们为什么要写单元测试？
   1、单元测试记录软件系统内部和外部的结构;  
　　2、单元测试帮助你和其他开发者迅速地看到是否“升级”的代码打乱了已有的代码;  
　　3、单元测试是你的软件原理bug—所有的问题都会在编写测试时解决掉;  
　　4、单元测试结合“code coverage”会让提升你软件的质量;  
　　5、单元测试可以在开发过程中显著提高团队信心——如果所有的测试通过了，则意味着所有的特性顺利运行，每个人都工作得很出色。  
　　6、单元测试提高了效率——你不再需要恼人的手工测试，而且代码变动后，你只需要开启单元测试并且查看红/绿栏即可。  
　　7、还有很重要的一点是：单元测试可以作为DOCUMENTATION(无论是辅助的还是主要的)。
## 2.请大家自行查找冒泡排序算法的原理，并用Java语言实现，并根据测试用例对算法编写单元测试。并说明你使用了哪些测试用例？
 
 **代码：**  
 (''')  
 
 import org.junit.Test;
 
 public class t {
 
	//语句覆盖
	@Test
	public void test1() {
		int[] arr= {4,3,2,1};
		test t=new test();
		t.BubbleSort(arr);
	}
	
	//判定覆盖
	@Test
	public void test2() {
		int[] arr= {1,2,3,4};
		test t=new test();
		t.BubbleSort(arr);
	}
	@Test
	public void test3() {
		int[] arr= {4,3,2,1};
		test t=new test();
		t.BubbleSort(arr);
	}
	
	//条件覆盖
	@Test
	public void test4() {
		int[] arr= {1,2,3,4};
		test t=new test();
		t.BubbleSort(arr);
	}
	@Test
	public void test5() {
		int[] arr= {4,3,2,1};
		test t=new test();
		t.BubbleSort(arr);
	}
	
	//路径覆盖
	@Test
	public void test6() {
		int[] arr= {1,2,3,4};
		test t=new test();
		t.BubbleSort(arr);
	}
	@Test
	public void test7() {
		int[] arr= {4,3,2,1};
		test t=new test();
		t.BubbleSort(arr);
	}
	
}


class test {

	public void BubbleSort(int[]arr) {
		
		for(int i=0;i<arr.length-1;i++) {
			for(int j=0;j<arr.length-1-i;j++) {
				if(arr[j]>arr[j+1]) {
					int temp=arr[j];
					arr[j]=arr[j+1];
					arr[j+1]=temp;
				}
			}
			
		
		for(int i1=0;i1<arr.length;i1++)
				System.out.print(arr[i1]+" ");
		System.out.println();
		}
	}
	
}

   (''')
  
   **流程图：**  
   
  ![冒泡排序流程图](https://github.com/tongliran/phoato/blob/master/冒泡排序流程图.png)  
  
  **测试用例**  
  用例编号|输入|输出|用例说明
  -------|----|----|-------
   --1-- |arr={4,3,2,1}|1,2,3,4|语句覆盖
   --2-- |arr={1,2,3,4}|1,2,3,4|判定覆盖
   --3-- |arr={4,3,2,1}|1,2,3,4|判定覆盖
   --4-- |arr={1,2,3,4}|1,2,3,4|条件覆盖
   --5-- |arr={4,3,2,1}|1,2,3,4|条件覆盖
   --6-- |arr={1,2,3,4}|1,2,3,4|路径覆盖
   --7-- |arr={4,3,2,1}|1,2,3,4|路径覆盖
   
   
   
   
  
