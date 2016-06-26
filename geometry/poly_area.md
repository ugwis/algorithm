# 多角形ポリゴンの面積を求める
```
double polygon_area(vector<pair<int, int>> v) {
	// O(n)
	double ret = 0.0;
	v.emplace_back(make_pair(v[0].first,v[0].second));
	for (int unsigned i = 0; i < v.size()-1; i++) {
		ret += v[i].first*v[i + 1].second - v[i].second*v[i + 1].first;
	}
	return abs(ret) / 2;
}
```
