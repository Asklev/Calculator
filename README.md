```
#include <iostream>
#include <string>
using namespace std;

float calculating() {
	float n1, n2;
	string znak;
	string checker;
	float ans;
	cout << "Input number for example (12 (+,-,/,*) 4)"<<endl;
	cin >> n1 >> znak >> n2;

  if (znak == "-") {
		ans = n1 - n2;
	}
	else if (znak =="+") {
		ans = n1 + n2;
	}
	else if(znak=="/") {
		if (n1 == 0 or n2 == 0) {
			cout << "Impossible" << endl;
			return 0;
		}
		else {
			ans = n1 / n2;
		}
	}
	else if (znak=="*") {
		ans = n1 * n2;
	}
	else if (znak=="/" and n1 == 0) {
		checker = "Impossible";
	}

  cout << "Answear is: " << ans << endl;
	return 0;
}

int main() {
	calculating();
	return 0;
}
```
