```python
        logs = [(log[0], log[1], log[2]) for log in logs]
        logs = sorted(logs, key=lambda tup: tup[0])
```