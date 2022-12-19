# Sorting and Searching
ขอเสริมนิดหนึ่ง เท่าที่เราเคยถามรุ่นพี่ IOI มา การเก็บข้อมูลโดยใช้ vector (dynamic array) หรือการใช้ array ถ้ากำหนดขนาดของชุดข้อมูลตั้งแต่เริ่มแล้ว operation พื้นฐานของข้อมูลทั้งสองชุดจะใช้เวลาเท่ากัน
```cpp
int arr[size];
for(int i = 0; i < size; i++) {
  cin >> arr[i]; // get
}
arr[0] = 1; // set value
arr[1] = 2;
arr[2] = 5;
cout << arr[0]; // call value
sort(arr, arr + size); // sorting
```
```cpp
vector<int> vec(size);
for(int i = 0; i < size; i++) {
  cin >> vec[i]; // get
}
vec.at(0) = 1; // set value
vec.at(1) = 2;
vec.at(2) = 5;
cout << vec.at(0); // call value
sort(vec.begin(), vec.end()); // sorting
```
<br>ยกเว้นกรณีการใช้ push_back ของ vector เพราะต้องเสียเวลาประกาศพื้นที่เพิ่ม
```cpp
vector<int> vec;
for(int i = 0; i < size; i++) {
  int k;
  cin >> k;
  vec.push_back(k);
}
```
<br>แต่ส่วนตัวรู้สึกว่าการใช้ vector มีข้อดีเยอะกว่ามาก เนื่องจาก vector มี stl ให้ใช้งานหลากหลาย และ iterator ของ vector ก็ยังใช้งานง่ายกว่าด้วย
```cpp
vector<int>::iterator itr_1 = lower_bound(vec.begin(), vec.end(), 5);
vector<int>::iterator itr_2 = upper_bound(vec.begin(), vec.end(), 5);
```
