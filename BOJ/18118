#include <bits/stdc++.h>
#include <unordered_set>
#include <unordered_map>
#include <random>
using namespace std;
#define ll long long
#define fr first
#define sc second
#define pll pair<ll, ll>
#define all(v) v.begin(), v.end()

int n, m;
ll dp[10][110000];

void solve(int tc) {
	cin >> n >> m;
	for (int i = 0; i <= n; i++)
		for (int j = 0; j <= m; j++)
			dp[i][j] = -1e9;

	dp[0][0] = 0;
	for (int i = 0; i < n; i++) {
		for (int j = 0; j < m; j++) {
			for (int k = 0; k < 10; k++) {
				dp[i + 1][(j * 10 + k) % m] = max(dp[i + 1][(j * 10 + k) % m], 10 * dp[i][j] + k);
			}
			dp[i + 1][(j * 100 + 11) % m] = max(dp[i + 1][(j * 100 + 11) % m], 100 * dp[i][j] + 11);
		}
	}
	cout << dp[n][0] << '\n';
}

int main() {
	ios::sync_with_stdio(false);
	cin.tie(0);
	if (1) {
		int T; cin >> T;
		for (int i = 1; i <= T; i++) solve(i);
	}
	else {
		solve(0);
	}
	return 0;
}
