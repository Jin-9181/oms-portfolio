# leetcode – April


## number. name

- Difficulty :
- Main ideas :
- Lessons leanred : 

---

## number. name

- Difficulty :
- Main ideas :
- Lessons leanred : 


## ✅ 0001. Two Sum
- 🔗 링크: [https://leetcode.com/problems/two-sum](https://leetcode.com/problems/two-sum)
- 📚 난이도: Easy
- 🧩 핵심 아이디어:
  - 반복문 + dict (해시맵)으로 target - num을 동시에 추적
- 💡 배운 점:
  - enumerate(), dict 활용법, 시간복잡도 생각
- ⏱ 시간복잡도: O(n)
- 📦 공간복잡도: O(n)

```python
def twoSum(nums, target):
    hashmap = {}
    for i, num in enumerate(nums):
        if target - num in hashmap:
            return [hashmap[target - num], i]
        hashmap[num] = i