### 07/17/26
#### LoRA Fine-Tuning
Based on Mundy's recommendation, I learned about lora today. Now, previously, the only lora I knew of was "LoRa" in the context of long range radio transmissions. this lora stands for Low-Rank Adaptation. Its for fine-tuning an LLM much more effeciently than standard fine tuning, thus allowing us to fine tune very large models.

The idea of lora depends on the rank of a matrix. The rank of a mtraix is the maximum number of linearly independent rows or columns in the matrix. Rememebr column *a* is dependent to column *b* if there exists *a*=c*b*

If we can take our linearly dependent columns, we can reduce the dimension of the matrix while also keeping most of its information. For example, we can decompose a 3x3 matrix into a 3x1 matrix multiplied by a 1x3 matrix, effectively reducing the weights from 9 to 6. 

#### Promise theory
not really sure how this differs from just the idea of a promise, or what it could be used for

#### Chomsky heirarchy
Looking into promise theory brought me here.
