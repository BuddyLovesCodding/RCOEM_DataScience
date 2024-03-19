package SRCEM_pack2;

import java.util.Arrays;
import java.util.HashMap;
import java.util.Stack;

public class lec6 {
	public static void main(String[] args) {
		
//		int given[] = {1,4,2,5,3,1,7,8,2,0};
//		Stack<Integer> st = new Stack<>();
//		int arr[] = new int[given.length];
//		nextGreaterDhundo(given , st , arr);
//		System.out.println(Arrays.toString(arr));
//		System.out.println(st);
		
//		Stack<Integer> st = new Stack<>();
//		HashMap<Integer , Integer> map = new HashMap<>();
//		int nums1[] = {4,1,2};
//		int nums2[] = {1,3,4,2};
//		nextGreater1leet(nums1 , nums2 , st , map);
		Stack<Integer> st = new Stack<>();
		int arr[] = {3,5,4,0,7,-1};
		boolean ans = Pattern_132( st , arr);
		System.out.println(ans);
		
		
		
	}
	public static void nextGreaterDhundo(int[] given , Stack<Integer> st , int[] arr) {
		
		
		for(int i =0; i<given.length ; i++) {
			
			while(!st.isEmpty() && given[st.peek()] < given[i]) {
				
				arr[st.pop()] = given[i];
				
			}
			
			
			st.add(i);
		}
		
		while(!st.isEmpty()) {
			
			arr[st.pop()] = -1;
		}
		
	}
	
	
public static void nextGreater1leet(int[] nums1 , int[] nums2 , Stack<Integer> st , HashMap<Integer , Integer> map) {
		
		
		for(int i =0; i<nums2.length ; i++) {
			
			while(!st.isEmpty() && nums2[st.peek()] < nums2[i]) {
				
//				arr[st.pop()] = given[i];
				map.put(nums2[st.pop()], nums2[i]);
				
			}
			
			
			st.add(i);
		}
		
		while(!st.isEmpty()) {
			
//			arr[st.pop()] = -1;
			map.put(nums2[st.pop()], -1);
		}
		System.out.println(map);
		
		for(int i =0; i<nums1.length ; i++) {
			
//			if(map.containsKey(nums1[i])) {
				int value = map.get(nums1[i]);
				nums1[i] = value;
//			}
			
		}
		System.out.println(Arrays.toString(nums1));
	}

public static boolean Pattern_132(Stack<Integer> st , int arr[]) {
//	{3,5,4,0,7,-1}
	int k = Integer.MIN_VALUE;
	for(int i = arr.length-1 ; i>=0 ; i--) {
			
		if(arr[i]<k) {
			return true;
		}
		
		while( !st.isEmpty() && st.peek()<arr[i]) {
			k = st.pop();
		}
		
		st.add(arr[i]);
	}
	
	
	return false;
}
}
