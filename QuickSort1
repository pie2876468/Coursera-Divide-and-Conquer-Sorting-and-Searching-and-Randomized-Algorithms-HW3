#include <iostream>
#include <fstream>
using namespace std;
std::ifstream infile("IntegerArray.txt");

long long int QuickSort1(int *a, int start, int end, int pivotindex){
//	cout << "   start :  " << start << "   end :  " << end << "   pivotindex :  " << pivotindex << endl;
	int pivot = a[pivotindex];
	int i;
	int j;
	int tmp;
	int count = end-start;
//	cout << "count:  " << count << endl;
	if (start == end){
		return 0;
	}

	else if ((end-start)==1){
		if(a[start]>a[end]){
			tmp = a[end];
			a[end]= a[start];
			a[start] = tmp;
		}
		return 1;
	}
//*/
	else if ((end-start)>1){

	i = (start +1);
	for (j=(start+1);j<=end;j++){

		if (a[j]<pivot){
			tmp = a[i];
			a[i]=a[j];
			a[j]=tmp;
			i++;
		}
	}
	tmp = a[i-1];
	a[i-1] = pivot;
	a[pivotindex] = tmp;
	
	long long int left;
	long long int right;
	
	int leftarrayrightedge;
	leftarrayrightedge = i-2;
	int rightarrayleftedge;
	rightarrayleftedge = i;
	if(leftarrayrightedge<start){
		leftarrayrightedge = start;
	}
	if(rightarrayleftedge>end){
		rightarrayleftedge = end;
	}
//	cout << "Left subarray" << endl;
//	cout << "   start :  " << start << "   end :  " << leftarrayrightedge << "   pivotindex :  " << start << endl;
	left = QuickSort1(a,start,leftarrayrightedge,start);
//	cout << "Right subarray" << endl;
//	cout << "   start :  " << rightarrayleftedge << "   end :  " << end << "   pivotindex :  " << rightarrayleftedge << endl;
	right = QuickSort1(a,rightarrayleftedge,end,rightarrayleftedge);
//	cout << "Next Loop" << endl;
//	left  =0;
//	right =0;
	return left+right+count;
	}
}

int main(){
//load file
	int in;
	int inputsize = 10000;
	int input[inputsize];
	int loadindex = 0;
	while (infile >> in){
    input[loadindex] = in;
    loadindex++;
	}
//load file end*/
// test case;

//  int d[100] = {4, 80, 70, 23, 9, 60, 68, 27, 66, 78, 12, 40, 52, 53, 44, 8, 49, 28, 18, 46, 21, 39, 51, 7, 87, 99, 69, 62, 84, 6, 79, 67, 14, 98, 83, 0, 96, 5, 82, 10, 26, 48, 3, 2, 15, 92, 11, 55, 63, 97, 43, 45, 81, 42, 95, 20, 25, 74, 24, 72, 91, 35, 86, 19, 75, 58, 71, 47, 76, 59, 64, 93, 17, 50, 56, 94, 90, 89, 32, 37, 34, 65, 1, 73, 41, 36, 57, 77, 30, 22, 13, 29, 38, 16, 88, 61, 31, 85, 33, 54};
//  int sd=100;
	int d[8]= {3,8,2,5,1,4,7,6};
	int sd =8;
  long long int sumi = 0;
 // sumi =  QuickSort1(d,0,(sd-1),0);
  sumi =  QuickSort1(input,0,(inputsize-1),0);

  cout <<"total comparisons :  " << sumi << endl;
/* 
  int i =0;
  while (i<sd){
  cout << d[i] << endl;
  i++;
}
//*/
/*
  int i =0;
  while (i<inputsize){
  cout << input[i] << endl;
  i++;
}
//*/
return 0;
}
