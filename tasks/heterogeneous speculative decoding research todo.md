---
tags:
  - task
finished: false
start-date: 2024-04-21
deadline: 2024-04-26T16:55:00
---
# 🎞️Resource: 
1. 
# 🎢Log:
1. 

# 😅Questions:
- [ ] 
# 🧑‍💻TODOs:
- [ ] set up the tree attention code in heterogeneous way implement the naive tree attention and the basic speculative decoding verification, need do comparison later anyways  📅 2024-04-21 
- [ ] create  a data set to check the difference of acceptance between eta sampling and reject sampling  📅 2024-04-22 
- [ ] experiment different ways of dynamic tree construction and compare the result to reject sampling, use reject sampling as what? it is hard to say, because reject sampling prefer greedy, we will see later  📅 2024-04-25
# ✨How to Solve this task:
### break down in 3 steps: 
1. first understand jack's code 
2. write my code, and document it well 
3. find standard way to evaluate llm result quality. 

---
## details

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
|     |     |     |     |     |
|     |     |     |     |     |
1. the code is runing 
	1. I need to change the verification in strategy 
- [ ] need to figure out why current experiment even load in 8 bit for llama 7b is run out of space, just compare 68m and 168m model is not helpful, may use tinyllama instead  📅 2024-04-22 
- [ ] think about how to make the generation and verification separately 📅 2024-04-22 
1. also need sending the k-configuration as well 

### change on verification:
#algorithm :
1. need to change the verification step so it will considered the longest acceptace sequence 
	1. do this in simplest format
		1. duplicate the probability?
		2. or just let the verification function return the accepted candidates 
	2. may be not considering heterogeneous, make the function return the longest tree first. 
make tree-attention heterogeneous is more difficult than  i thought because the kv cache is hard to update 
==or is it possible to update the kv cache through the verified tokens?==

I must admit, even just modifying the verification function is pretty challenging, 😢 
- [ ] need finish verify single layer function today! 📅 2024-04-22 
# 🪙Conclusion & how to improve: