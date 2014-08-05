Min-Max
=======
public class LVCCArrayCoronel {
    int max;
    int min;
    int[] numbers;
 
    public LVCCArrayCoronel (int[] numbers) {
        this.numbers = numbers;
        this.determineMin();
        this.determineMax();
    }
 
    private void determineMin() {
        int i;
        this.min = this.numbers[0];
        for (i = 1; i < this.numbers.length; i++) {
            if (this.numbers[i] < this.min) {
                this.min = this.numbers[i];
            }
        }
    }
 
    private void determineMax() {
        int i;
        this.max = this.numbers[0];
        for (i = 1; i < this.numbers.length; i++) {
            if (this.numbers[i] > this.max) {
                this.max = this.numbers[i];
            }
        }
    }
 
    public int getMin() {
        return this.min;
    }
 
    public int getMax() {
        return this.max;
    }
}
=============================================================================
public class LVCCArrayAppCoronel {
	private int min;
	private int max;

    public static void main(String[] args) {
        int[] numbers = { 18, 31, 16, 32, 16, 99, 51, 49, 90};

    LVCCArrayCoronel coronel = new LVCCArrayCoronel(numbers);

    	System.out.println("numbers: ");
    	for (int s = 0; s < numbers.length; s++) {
    		System.out.println(numbers[s] + " ");
    	}
        System.out.println("Smallest Number: " +coronel.getMin());
        System.out.println("Largest Number: " +coronel.getMax());
    }
}
