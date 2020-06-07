# Caltech101

Model 7 and Modle 8 are based on Model 5

The training sequence:
  Model 7: "CNN7 try1 30E" --> "CNN7 try1 60E" --> "CNN7 try2" --> "CNN7 try3 60E"
          --> "CNN7 try4 70E" --> "CNN7 try5 70E" --> "CNN7 try5 70-100E" 
          --> "CNN7 try5 continue 1" --> "CNN7 try5 continue 2" --> "CNN7 try5 continue 3"
          
          The highest eval accuracy: 0.776 (210E in CNN7 try5 continue 3)
  
  Model 8: "CNN8 try1" --> "CNN8 try2" --> "CNN8 try3 90E" -->"CNN8 try3 0.757"
           --> "CNN8 continue1" --> "CNN8 continue2 0.79" --> "CNN8 continue3"
           
           The highest eval accuracy: 0.794 (180E in CNN continue 3)
