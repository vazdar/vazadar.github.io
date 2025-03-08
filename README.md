/*     vector
cú pháp : vector <kiểu dữ liệu > biến ;
vd vector<int> a;
a.push_back(x) : đẩy vào sau 
a.push_bash(100) : đẩy 100 vào  a 
và các phần tử dùng như mảng 

vd push_back(100)
push_back(200)

a => a[100 , 200 ,...]

để biết có bn phần tử a.size() ;

interator : như người đứng ngoài quan sát vào các giá trị của a
a.begin = > trỏ vào giá trị đầu 
a.end => trỏ và giá trị sau 200 < o có giá trị > 

a.begin() + x = a[x] 

 vector<int> a;
    a.push_back(100) ;
    a.push_back(202);
    cout << a[0] << " " << a[1] << endl; // in ra 
    cout << a.size() << endl;
    for ( auto it = a.begin() ; it != a.end() ; it++){
        cout << *it <<" ";
    } 
    // :: là toán tử phạm vi || it là đặt tên 
    // auto thay đc các kiểu dữ liệu , vector , pair 
    
    
    
int n ; cin >> n ;
    vector<int > a(n); // khai báo như này thì vector a có n phần tử 
    vector < int> a( n , 100) ; // gán hết 100 cho n phần tử => n phần tử == 100 
    for (int i = 0 ; i <n ; i++ ){
        // int tmp ; cin >> tmp;
        // a.push_back(tmp);
        cin >> a[i] ; // nếu khai báo a có n phần tử thì nhập luôn 
    }
    for ( int i = 0 ; i < a.size() ; i++){
        cout << a[i] << " ";
    }
    cout << endl;
    for ( int x : a){
        cout << x << " ";
    }
    
    // nếu muốn mở rộng thì a.push_back(x) bình thường 
    
    a.push_back(2);
    cout << endl << a.size() << endl;
    return 0;
*/



/*    PAIR 
cấu trúc : pair < int ,long long > a;
==> Biến a có thể lưu 2 giá trị 
đầu tiên : frist 
thứ 2 : second 

ex : pair<int , int > a;
mảng : pair < int ,int > a[100];
    cin >> a.frist ;
    cin >> a.second ;
    cout << a.first << " " << a.second;

    note 
    
pair < int , pair < int , int >> a;

cout << a .frist;
cout << a.second.frist ;
cout << a.second.second ;


các hàm cần nhớ
push_back(x);
size();
a.pop_back();// xóa phần tử ở cuối vector
aresa - xóa 1 phần tử 

*/


/* MEMSET 
cú pháp : memset( tên mảng , giá trị muốn gán cho mảng , kích thước của mảng )

chỉ gán tất cả giá trị 0 or -1 

int a[100];
    memset( a , 0 , sizeof(a));
    for ( int x : a ){
        cout << x << " ";
    }
    
    
*/



#include<bits/stdc++.h>

using namespace std ;

int main(){
    vector<int> a(10);
    
    for ( int i = 1 ; i <= 10 ; i++){
        a[i-1] = i ;
    }
    for ( int x : a ){
        cout << x << ' ';
    }
    a.pop_back();// xóa phần tử cuối 
    
    cout << endl << a.size() << endl;
    
    a.erase( a.begin() + 4); // xóa phần tử ở vị trí 5 khi biết iterator ( vị trí của nó trong vector ) 
    // xóa vị trí 5 
    
    // muốn xóa 1 đoạn [x , y] => a.begin() + x --> a.begin() + y + 1 
    a.erase( a.begin() + 4 , a.begin() + 6 + 1 );
    
    a.insert(a.begin() + 3 , 1000); // thêm 1000 vào chỉ số 3 

    // xóa đoạn 6 -> 8 
    for ( int x : a ){
        cout << x <<' ';
    }
    cout << endl;
    a.clear(); // dọn sạch " rỗng "
    
    cout << a.size() << endl;
}
