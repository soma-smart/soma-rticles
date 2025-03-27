# 7. Les languages non typés

```python
def add(left, right):
    return left + right

def concat(left, right):
    return left + right

add(1, 2)  # 3
concat("lorem", "ipsum")  # loremipsum
```

```python
def add(left: int, right: int) -> int:
    return left + right

def concat(left: str, right: str) -> str:
    return left + right

add("lorem", "ipsum")  # Marchera quand même !
concat(1, 2)  # Là aussi !
```