# CSE327_P4
Last practical homework for CSE 327!

## Exercise 3:
- run `python kbencoder.py -g --kb_path potter.txt`

## Exercise 7:
!python ../kbencoder.py --kb_path randomKB.txt --train_unification_model --embed_size 25 --embed_model_path rKB_model_e_size_25.pth
!python ../nnreasoner.py --embed_type unification -s --embed_size 25 --embed_model_path randomKB_400_e_size_25_model.pt
!python ../evaluate.py --kb randomKB.txt -s --embed_size 25 --embed_model_path randomKB_400_e_size_25_model.pt --scoring_model_path scoring_path_25.pt
!python ../evaluate.py --kb randomKB.txt -u --embed_size 25 --embed_model_path randomKB_400_e_size_25_model.pt --scoring_model_path scoring_path_25.pt
