# 

```C++ runnable
#include <unordered_map>
#include <tuple>
using namespace std;
typedef tuple<int, string, string> myTuple_t;
typedef unordered_map<string, myTuple_t> myMap_t;

int main ()
{
    myMap_t MyMap;
    MyMap.insert({{"key1", make_tuple (1, "Joe", "17 Palace St.")}});
    MyMap.insert({{"key2", make_tuple (2, "Greg", "14 Tuxedo Blvd.")}});
    MyMap.insert({{"key3", make_tuple (3, "Beth", "244 Laurel Rd.")}});
    for (auto& x: MyMap)
        cout << get<0>(x.second) << get<1>(x.second) << get<2>(x.second);
    return 0;
}
