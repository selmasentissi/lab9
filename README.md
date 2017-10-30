# lab9
public class DelimiterChecker {
	
	static String test = " { bonjour les amis}";
	static int opener = 0;
	static int closer = 0;	
	static int ch = test.length()-1;
	
	
	public static void main( String [] args )
	{
		DelimiterChecker();
		result();
		if (result() == true)
			System.out.println(" Complete braces");
		else
			System.out.println("You need to correct braces");
			
	}

	private static void DelimiterChecker() {
		
do 
		{
		if ( test.charAt(ch) == '{')
		{	opener++;
			
		}
		ch--;
		}
while ( test.length()>1);
		
		int ch1 = test.length()-1;
	do 	
		{
			if (test.charAt(ch1) == '}')
			{
				closer ++;	
			}
			ch1--;
			}	
	while (test.length()>1);
	}
	public static boolean result ()
	{
		if (opener == closer)
			return true;
		else
			return false;		
	}
	
	
}
