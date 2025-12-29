# Educational Codeforces Round 186 (Rated for Div. 2)

## \[A. New Year String]

### 题目描述

We will call a string consisting of characters 0, 2, 5, and/or 6 a New Year string if at least one of the two conditions is met:

it **contains the string 2026** as a continuous substring;
it does **not contain the string 2025** as a continuous substring.

**数据范围：**
4≤n≤20

### 解题思路

首先判断是否包含2026或不包含2025->new year string
反之 不包含2026且包含2025 变成new year string只需要把5改成6

---

### 算法实现



#### 一：遍历字符串使用substr寻找2025、2026



\#include <bits/stdc++.h>

using namespace std ;

\#define rep(i, a, b) for(int i = (a); i <= (b); i++ )

\#define per(i, a, b) for(int i = (a); i >= (b); i-- )

\#define endl '\\n'



void solve() {

    int n;

    cin >> n;

 

    string s;

    cin >> s;

 

    bool f2026 = false ;

    bool f2025 = false ;

 

    rep(i, 0, n - 4) {

    	string sub = s.substr(i, 4) ;

    	if(sub == "2026") f2026 = true ;

    	if(sub == "2025") f2025 = true ;

 	}

 

 	if(f2026 || !f2025) {

 		cout << "0" << endl ;

 	} else {

 		cout << "1" << endl ;

 	}

 

    return ;

}



signed main() {

    ios::sync\_with\_stdio(false) ;

    cin.tie(0) ;

    cout.tie(0) ;

 

    int t = 1 ;

    cin >> t ;

 

    while (t--) {

        solve();

    }

 

    return 0;

}



#### 二：使用C++23标准string中的contains函数



\#include <bits/stdc++.h>

\#define endl '\\n'

using namespace std ;



void solve() {

    int n;

    cin >> n;

 

    string s;

    cin >> s;

 

    if(s.contains("2026") || !s.contains("2025") ) {

        cout << "0" << endl ;

    } else {

        cout << "1" << endl ;

    }

 

    return ;

}



signed main() {

    ios::sync\_with\_stdio(false) ;

    cin.tie(0) ;

    cout.tie(0) ;

 

    int t = 1 ;

    cin >> t ;

 

    while (t--) {

        solve();

    }

 

    return 0;

} 





