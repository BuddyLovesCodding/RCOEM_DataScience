package SRCEM_pack1;

import java.util.ArrayList;
import java.util.Scanner;

public class lec4 {
public static void main(String[] args) {
//	int arr[] = {1,2,3};
//	int idx = 0;
//	combinationMainChalo(5 , arr , idx , "");
//	ArrayList<String> al = new ArrayList<>();
//	numberNikalo(0 , "23" , "" , al);
//	System.out.println(al);
	Scanner scn = new Scanner(System.in);
	int row = scn.nextInt();
	int col = scn.nextInt();
	char maze[][] = new char[row][col];
	for(int i = 0; i<maze.length ; i++) {
		for(int j = 0; j<maze[0].length ; j++) {
			maze[i][j] = scn.next().charAt(0);
		}
	}
	int visited[][] = new int[row][col];
	
	int ans = chaloBaharChalen(0,0,maze,visited,"",0);
	System.out.println(ans);
}

private static void combinationMainChalo(int n, int[] arr, int idx, String str) {
	
	if(n==0) {
		System.out.println(str);
		return;
	}
	if(n<0 || idx>arr.length) {
		return;
	}
		
	for(int i = idx ; i<arr.length ; i++) {
		combinationMainChalo(n-arr[i] , arr, i, str+arr[i]);
	}
	
}

  public static void numberNikalo(int idx , String digits , String path , ArrayList<String> al) {
	  
	  if(idx == digits.length()) {
//		  System.out.println(path);
		  al.add(path);
		  return;
	  }
	  
	  char ch = digits.charAt(idx);
	  String str = stringResptoChar(ch);
	  for(int i = 0; i<str.length() ; i++) {
		  numberNikalo(idx+1 , digits , path + str.charAt(i) , al);
	  }
  }
  
  public static String stringResptoChar(char ch) {
	  String arr[] = {"abc" , "def" , "ghi" , "jkl" , "mno" , "pqrs" , "tuv" , "wxyz"};
	  return arr[ch-'2'];
  }
  
  
  
//rat in a maze
  
  public static int chaloBaharChalen(int crow , int ccol , char[][] maze , int[][] visited , String path , int count) {
	  
	  if(crow>=maze.length || crow<0 || ccol>=maze[0].length || ccol<0 || maze[crow][ccol] == 'X' || visited[crow][ccol]==1) {
		  return count;
	  }
	  
	  if(crow == maze.length-1 && ccol == maze[0].length-1) {
		  
		  visited[crow][ccol]=1;
		  System.out.println("==================");
		  System.out.println(path);
		  printVisited(visited);
		  visited[crow][ccol]=0;
		  count++;
		  return count;
	  }
//	  System.out.println("yes");
	  visited[crow][ccol] = 1;
	  count = chaloBaharChalen(crow-1 , ccol , maze , visited , path + "U",count);
	  count = chaloBaharChalen(crow , ccol+1 , maze , visited , path + "R",count);
	  count = chaloBaharChalen(crow+1 , ccol , maze , visited , path + "D",count);
	  count = chaloBaharChalen(crow , ccol-1 , maze , visited , path + "L",count);
	  visited[crow][ccol] = 0;
	  return count;
	  
  }
  
  public static void printVisited(int[][]visited) {
	  for(int i = 0; i<visited.length ; i++) {
		  for(int j = 0 ; j<visited[0].length ; j++) {
			  System.out.print(visited[i][j]);
		  }
		  System.out.println();
	  }
  }
  
}

//5 4 
//O X O O
//O O O O 
//O O X O
//X O O O 
//X X O O

