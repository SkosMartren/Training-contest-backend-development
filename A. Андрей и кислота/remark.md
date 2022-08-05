Примечательно, что данный код
```objectivec
#include<iostream>
#include<algorithm>
#include<vector>

using namespace std;

int main() {

	int n;
	cin >> n;

	vector <int64_t> v(n);

	for (auto& a_i : v) {
		cin >> a_i;
	}

	cout << ((is_sorted(v.begin(), v.end())) ? v[n - 1] - v[0] : -1);

	return 0;
}
```
принимает тестирующая система, в то время как такой код
```objectivec
#include<iostream>
#include<algorithm>
#include<vector>

using namespace std;

int main() {

	int n;
	cin >> n;

	vector <uint64_t> v(n);

	for (auto& a_i : v) {
		cin >> a_i;
	}

	cout << ((is_sorted(v.begin(), v.end())) ? v[n - 1] - v[0] : -1);

	return 0;
}
```
Валиться на 3 тесте:  
3  
3 2 1  
