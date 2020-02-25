# Regex-Practice #Java Programming

1.Program for URL Matching


package com.practice;

import java.util.ArrayList;
import java.util.List;

public class regexUrl {

	public static void  main(String[] args)
	{
		String s1="https://www.youtube.com";
		String s2="www.youtube.com";
		String s3="youtube.com";
		String s4="youtube";
		List<String>strings=new ArrayList<>();
		
		strings.add(s1);
		strings.add(s2);
		strings.add(s3);
		strings.add(s4);
		
		
		String regex="^(https://)?(www.)?[a-zA-Z0-9]{1,20}(.com)$";
		
		for(int i=0;i<strings.size();i++)
		{
			String curr=strings.get(i);
			if(curr.matches(regex))
				System.out.println("Matched");
			else
				System.out.println("Not Matched");
		}
		
	}
}

Output:

Matched
Matched
Matched
Not Matched
