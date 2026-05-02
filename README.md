# CSE327 P4
#### Rachel McIntosh (rem526@lehigh.edu), Zoe Ford (zmf227@lehigh.edu), Joelle Dizon (jkd227@lehigh.edu)
Last practical homework for CSE 327!

## Description:
We created a custom Harry Potter KB (potter.txt), as well as randomly generated KBs of varying sizes (200, 300, and 400 rules) to test the performance of different NN architectures and embedding sizes.

## Exercise 3:
- run `python kbencoder.py -g --kb_path potter.txt` (to test the properties)

## Exercise 5 & 6:
- run `!python ../../kbencoder.py --generate_kb --num_rules {new size} --new_vocab --save_vocab`
- run the two training steps & the evaluation (`../kbencoder.py --train_unification_model` and `../nnreasoner.py`

## Exercise 7:
(These aren't quite right, I needed to edit some of the file path names, but can update those if we need)
```
!python ../kbencoder.py --kb_path randomKB.txt --train_unification_model --embed_size 25 --embed_model_path rKB_model_e_size_25.pth
!python ../nnreasoner.py --embed_type unification -s --embed_size 25 --embed_model_path randomKB_400_e_size_25_model.pt
!python ../evaluate.py --kb randomKB.txt -s --embed_size 25 --embed_model_path randomKB_400_e_size_25_model.pt --scoring_model_path scoring_path_25.pt
!python ../evaluate.py --kb randomKB.txt -u --embed_size 25 --embed_model_path randomKB_400_e_size_25_model.pt --scoring_model_path scoring_path_25.pt
```
