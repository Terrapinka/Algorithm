public class Array_consolidated {
	public static void main(String[] args) {
		int arrfirst[] = { 0, 1, 2, 5, 6, 10, 12, 13, 15, 16 };
		int arrsecond[] = { 3, 4, 7, 8, 9, 11, 14, 17};
		int i,j,s;	// индексы массивов i(arrfirst), j(arrsecond), s(consolidated)
		int k,n,m;	// длины массивов n(arrfirst), m(arrsecond), k(consolidated)
		n = arrfirst.length;
		m = arrsecond.length;
		k = n + m;
		int arrconsolidated[] = new int[k];
//вывод массива arrfirst на экран
		System.out.print("arrfirst:  ");
		for (i = 0; i < arrfirst.length; i++) {
			System.out.print(arrfirst[i] + " ");
		}
		System.out.println("");

// вывод массива arrsecond на экран
		System.out.print("arrsecond: ");
		for (j = 0; j < arrsecond.length; j++) {
			System.out.print(arrsecond[j] + " ");
		}
		System.out.println("");

// объединение массивов
		System.out.print("arrconsolidated: ");
		i = 0;
		j = 0;

		for(s = 0; s < k; s++) {
			if((i < n) && (j < m)) {
				if(arrfirst[i] < arrsecond[j]) 
					arrconsolidated[s] = arrfirst[i++];
				else arrconsolidated[s] = arrsecond[j++];
			}
			else if(i < n) arrconsolidated[s] = arrfirst[i++];
			else arrconsolidated[s] = arrsecond[j++];
			System.out.print(arrconsolidated[s]+" ");
		}
