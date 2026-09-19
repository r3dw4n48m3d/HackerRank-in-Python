# HackerRank Problem

## Problem Title : Nested Lists
### Problem Link : https://www.hackerrank.com/challenges/nested-list/problem?isFullScreen=true



```python
def find_second_lowest_grade(records):
    scores = []
    names = []

    for record in records:
        scores.append(record[1])

    sorted_score = sorted(set(scores))

    second_lowest_score = sorted_score[1]

    for score in records:
        if score[1] == second_lowest_score:
            names.append(score[0])

    names = sorted(names)

    for name in names:
        print(name)




if __name__ == '__main__':
    records = []
    for _ in range(int(input())):
        name = input()
        score = float(input())

        records.append([name,score])


    find_second_lowest_grade(records)



```
