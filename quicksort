#include <iostream>
#include <sstream>
using namespace std;
void quickSort(int m[], int l, int h) {
	int i = l, j = h;
	int tmp;
	int pivot = m[(l + h) / 2];
	while (i <= j) {
		while (m[i] < pivot)
			i++;
		while (m[j] > pivot)
			j--;
		if (i <= j) {
			tmp = m[i];
			m[i] = m[j];
			m[j] = tmp;
			i++;
			j--;
		}
	}
	if (l < j)
		quickSort(m, l, j);
	if (i < h)
		quickSort(m, i, h);
}

int main() {
	int a; string line, o;
	getline(cin, o);
	istringstream stream(o);
	if (!(stream >> a || a > 0)) {
		cout << "An error has occuried while reading input data.";
		return 0;
	}

	getline(cin, line);
	istringstream arr(line);
	int *m = new int[a];

	for (int i = 0; i < a; i++) {
		if (!(arr >> m[i] || m[i] >= 0)) {
			cout << "An error has occuried while reading input data.";
			return 0;
		}
	}
	quickSort(m, 0, a - 1);
	for (int i = 0; i < a; i++) { cout << m[i] << ' '; }
	return 0;
}
