# Falsification Test Results

## Test 1: HLCI on Known Systems
============================================================
TEST 1: HLCI AUF BEKANNTEN SYSTEMEN
============================================================

System               HLCI       Expected       
------------------------------------------------------------
Fully Connected      0.9979     Low (ordered)  
Regular Lattice      0.4717     Low (ordered)  
Completely Random    0.9943     High (chaotic) 
Scale-Free           0.7565     ~0.27 (critical)

============================================================
VERDICT:
============================================================
❌ Ordered systems do NOT show low HLCI
✅ Random systems show HIGH HLCI
❌ Scale-free does NOT show ~0.27

❌ CONCLUSION: HLCI does NOT clearly distinguish regimes


** Process exited - Return Code: 0 **

  Random:       4.798

============================================================
TO TEST PROPERLY:
============================================================

1. Train all 3 architectures on MNIST (or CIFAR-10)
2. Use identical hyperparameters:
   - Learning rate: 0.001
   - Optimizer: Adam
   - Batch size: 64
   - Epochs: 50
3. Run 10 times each (different seeds)
4. Compare mean accuracy ± std

Expected if φ is real:
  φ-optimized >> powers-of-2 ≈ random

Expected if φ is NOT real:
  All three perform similarly (within ~1% accuracy)

📝 This test requires actual ML training
   Consider posting on r/MachineLearning for help


** Process exited - Return Code: 0 **
============================================================


## Test 2: Gamma Distribution  
============================================================
TEST 2: IST γ=2.236 SPEZIELL?
============================================================

Predicted γ = φ + 1/φ = 2.2361

Known power-law exponents:
Network Type              γ        Distance to 2.236   
------------------------------------------------------------
Citations                 3.000    0.764               
Internet                  2.100    0.136               
Proteins                  2.400    0.164               
Facebook                  2.300    0.064               
Twitter                   2.500    0.264               
Power Grid                2.700    0.464               
Neural (claimed)          2.240    0.004               
Mycelial (claimed)        2.250    0.014               
Cosmic (claimed)          2.220    0.016               
Actor Network             2.300    0.064               
Email Network             2.500    0.264               
Phone Calls               2.100    0.136               

============================================================
STATISTICS:
============================================================
Range: 2.100 - 3.000
Mean: 2.384
Std: 0.250
Predicted: 2.236

Mean distance from all networks to 2.236: 0.196

============================================================
VERDICT:
============================================================
⚠️  2.236 is somewhat central (marginally interesting)

🎯 CONCLUSION:
2.236 falls in common range - NOT particularly special


** Process exited - Return Code: 0 **


## Test 3: Architecture Analysis
============================================================
TEST 3: φ-OPTIMIZED DL ARCHITECTURES
============================================================

Architecture Comparison:
------------------------------------------------------------
φ-optimized:  [784, 484, 484, 484, 10]
  Ratios:     ['1.62', '1.00', '1.00', '48.40']
  Target φ:   1.62

Powers-of-2:  [784, 512, 256, 128, 10]
  Ratios:     ['1.53', '2.00', '2.00', '12.80']

Random:       [784, 600, 400, 200, 10]
  Ratios:     ['1.31', '1.50', '2.00', '20.00']

============================================================
ANALYSIS:
============================================================

Mean distance from φ (1.618):
  φ-optimized:  12.005
  Powers-of-2:  3.008
  Random:       4.798

============================================================
TO TEST PROPERLY:
============================================================

1. Train all 3 architectures on MNIST (or CIFAR-10)
2. Use identical hyperparameters:
   - Learning rate: 0.001
   - Optimizer: Adam
   - Batch size: 64
   - Epochs: 50
3. Run 10 times each (different seeds)
4. Compare mean accuracy ± std

Expected if φ is real:
  φ-optimized >> powers-of-2 ≈ random

Expected if φ is NOT real:
  All three perform similarly (within ~1% accuracy)

📝 This test requires actual ML training
   Consider posting on r/MachineLearning for help


** Process exited - Return Code: 0 **
