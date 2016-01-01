package binarymadness;

import java.util.Scanner;

public class Binary_Madness {

	public static void main(String[] args) 
	{
		long[] a = new long[100000];
		int length = 0;
		long Decx=0;
		long temp = 0, Binx = 0;
		boolean x1 = true, x2 = true;
		@SuppressWarnings("resource")
		Scanner x = new Scanner(System.in);
		while (x1||x2) 
		{
			int temp1 = 0;
			
				System.out
						.println("Please enter a Binary number between (00000000-11111111) :");
				
				while (!x.hasNextLong()) 
				{
					System.out
							.println("ILLEGAL ENTRY,Please donot type Characters.");
					System.out
							.println("Please enter a Binary number between (00000000-11111111) :");
					x.next();
				}
				Binx = x.nextLong();
				temp = Binx;
				length = LongLength(Binx);
				if (length > 8) 
				{
					System.out
							.println("*Please enter the value in the range {00000000-11111111}");
					
				} 
				else 
				{
					x2 = false;
				}
			
			// This for loop breaks down the given long number into its digits
			for (int i = 0; i >= 0; i++) 
			{
				a[i] = temp % 10;
				temp = temp / 10;
				if (temp == 0) 
				{
					i = -2;
				}
			}
			// This forloop checks weather the number is a binary number or not
			for (int k = 0; k < length; k++) 
			{
				if (a[k] > 1 || a[k] < 0) 
				{
					temp1++;
				}
			}
			if (temp1 > 0) 
			{
				System.out
						.println("*The number which is entered is not a Binary Number");
				System.out.println("*Please enter a Binary Number."
						+ "You can only enter 0's and 1's ");
			}

			else 
			{
				x1 = false;
			}
		}
		
		for(int b=0;b<length;b++)
		{
			Decx  = Decx+a[b]*exp(b);
		}
		System.out.println("The Decimal Value for "+Binx+" is: "+Decx);
			

	}

	private static long exp(int b) {
		int[] c={1,2,4,8,16,32,64,128};
		return c[b];
	}

	private static int LongLength(long binx) {
		int Length = 0;
		for (int m = 0; m >= 0; m++) {
			binx = binx / 10;
			Length++;
			if (binx == 0) {
				m = -2;
			}
		}
		return Length;
	}
}
