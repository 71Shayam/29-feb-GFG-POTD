	long long sumBitDifferences(int arr[], int n) {
	    // code here
	     long long hai=0,nhiHai=0,ans=0,num=1 ;
	    for(int i=0;i<32;i++){
	        for(int j=0;j<n;j++){
	            if(arr[j]&num)hai++;
	            else nhiHai++;
	        }
	        ans+=2*hai*nhiHai;
	        num<<=1;
	        hai=0;
	        nhiHai=0;
	    }
	    return ans;
	}
