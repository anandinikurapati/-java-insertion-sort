# -java-insertion-sort
# Algorithm of Insertion Sort
# Variable declared i=1
# 1.Traverse the Array till i<N
# 2.If arr[i]<arr[i-1] then arr[j]=value present after shifting the elements of the array from j to i-1.
# 3.Return the Sorted Array.
# approach1
public void insertionSort(int[] arr) {
    int n = arr.length;

    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

# approach2
class InsertionSort { 
	// Function to sort array using insertion sort 
	void sort(int arr[]) 
	{ 
		int n = arr.length; 
		for (int i = 1; i < n; ++i) { 
			int key = arr[i]; 
			int j = i - 1; 

			// Move elements of arr[0..i-1], that are 
			// greater than key, to one position ahead 
			// of their current position 
			while (j >= 0 && arr[j] > key) { 
				arr[j + 1] = arr[j]; 
				j = j - 1; 
			} 
			arr[j + 1] = key; 
		} 
	} 

	// A utility function to print array of size n 
	static void printArray(int arr[]) 
	{ 
		int n = arr.length; 
		for (int i = 0; i < n; ++i) 
			System.out.print(arr[i] + " "); 

		System.out.println(); 
	} 

	// Driver method 
	public static void main(String args[]) 
	{ 
		int arr[] = { 12, 11, 13, 5, 6 }; 

		InsertionSort ob = new InsertionSort(); 
		ob.sort(arr); 

		printArray(arr); 
	} 
}
