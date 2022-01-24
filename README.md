# Right rotate an array by interger value=d positions
<!-- # Right rotate an array by interger value=d positions
# C++ code -->
               
 
#include <iostream>

using namespace std;

void rev(int a[], int s, int n){
    int j=1;
    int n1=n-s;
    for (int i = 0; i < n1; i++) {
        if(i<n1/2){
            swap(a[i+s],a[n-j]);
            j++;
        }
    }
}


void R_rot(int a[], int d, int n){
    rev(a,0,n-d);
    rev(a,n-d,n);
    rev(a,0,n);
    for (int i = 0; i < n; i++) {
        cout<<a[i]<<" ";
    }
    
}

int main()
{
    int n=5, d=3;
    int a[n]={1,2,3,4,5};
    Rrot(a,d,n);
    return 0;
}
