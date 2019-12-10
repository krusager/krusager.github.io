## Начало работы с GitHub

https://guides.github.com/

## Docker repository
https://hub.docker.com/repository/docker/krusager/docrep


## Sum-of-two
import random

class SumOfTwo():
  def randNum():
    return random.randint(0, 99)

  def find_sum(data, targetSum):
    """'find_sum' function returns indexes of two numbers whose sum is equal to the number in the 'targetSum' variable"""
    targetListOfIndexes = []
    i = 0
    while (i < len(data)-1):
      if data[i] + data[i+1] == targetSum:
        # print('\t fit!', data[i], '+', data[i+1], '\t[', i, ',', i+1, ']')
        coupleOfIndex = (i, i+1)
        targetListOfIndexes.append(coupleOfIndex)
      i += 2  
    if not targetListOfIndexes:
      return 'coupleOfIndex is not found'
    return targetListOfIndexes   


if __name__ == '__main__': 
  targetSum = int(random.randint(0, 55))
  print('TargetSum=', targetSum)  
  print('*----------------------------*')

  cortegePi = (3,4,1,5,9,2,6,5,7,9,3,2,7,4,5,9,8,0,6,5,3,6,5,3,5,2,3,8,4,7)
  print('Indexes from cortege:\n', SumOfTwo.find_sum(cortegePi, targetSum))
  print('*----------------------------*')

  randList = []
  listSize = SumOfTwo.randNum()
  i = 0
  while (i < listSize):
    randList.append(SumOfTwo.randNum())
    i += 1
  print('Indexes from randList:\n')
  print(SumOfTwo.find_sum(randList, targetSum))




  





  
    

