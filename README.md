# qcnn-syndrome-decoding
1.QCNN-based syndrome decoding for the 3-qubit repetition code. Noisy QEC data is generated in Qiskit to benchmark QCNN against a classical NN for parity classification. Results show QCNN is more robust under noise and captures quantum correlations more effectively.

2.Project Summary:
This project explores syndrome decoding in the 3-qubit repetition code using both Quantum Convolutional Neural Networks (QCNNs) and classical neural networks. A noisy quantum error correction dataset is generated using Qiskit by simulating encoding, bit-flip errors, and syndrome extraction. Both models classify error parity from syndrome measurements under clean and noisy inputs.

3.Pipeline Overview:
The implementation consists of the following stages:
Generate noisy QEC syndrome data from the 3-qubit bit-flip code
Train a classical neural network as a baseline decoder
Build a QCNN using parameterized quantum circuits
Evaluate both models on clean and noisy data
Compare robustness and accuracy 

4.Model Descriptions:

Classical Neural Network:
A simple feedforward MLP is trained on syndrome bits using binary classification. 

QCNN Model:
QCNN uses Ry encoding, entanglement via two-qubit unitaries, and a pooling structure to extract parity information from quantum inputs. 

5.Results:
The comparison demonstrates that both models perform well on clean data, but QCNN is more robust under noise. 

Condition	     Classical NN	 QCNN
Clean accuracy	0.937	       0.937
Noisy accuracy	0.847	       0.874
QCNN showed a smaller accuracy drop, indicating better generalization and noise tolerance.

6.Conclusion:
QCNNs can provide advantages in syndrome decoding tasks, demonstrating stronger robustness against noisy data compared to classical neural networks.
