# AliceTechnoComposer

## Overview
This project aims to help DJs find suitable techno tracks for her DJ sets using AI. DJs usually spends hours on SoundCloud and YouTube, but maybe it could've been more efficient

## Objective
The goal is to finetune the existing MusicGen model using a dataset of songs Alice has previously played, obtained from her USB. This project aims to see if the model can learn Alice's musical preferences and generate tracks that align with her taste.

## Methodology
1. **Data Preprocessing**
   - Converted MP3 files to WAV files.
   - Cut WAV files into 10-second segments and used the first 20 seconds for the training dataset.
   - All WAV files are labeled "techno" and associated with a hash value of "Alice_hash".
2. **Model Training**
   - Extended finetuning of the MusicGen model.
   - Exploring "generate_continuity" to extend songs and "generate_unconditional" for new music creation.

## Challenges
- Extensive data preprocessing and debugging were required.
- Approximately 15-20 hours spent debugging and retraining the MusicGen code.
- Colab Pro GPU was necessary due to performance issues with the standard GPU.

## Evaluation
### Objective Metrics
- Frechet Audio Distance (FAD): Measures the similarity between real and generated audio samples.
- KL Divergence: Measures the statistical difference between predicted audio features of generated and real audio.

### Subjective Metrics
- Alice will provide feedback on generated music based on the following categories:
  - **Category A**: Alice_Hash (Pretrained + Alice_dataset)
  - **Category B**: Alice_Hash (Only Pretrained)
  - **Category C**: Techno (Pretrained + Alice_dataset)
  - **Category D**: Techno (Only Pretrained)

## Results
- **Category D** achieved the highest score, followed by Category C, Category A, and Category B.
- Categories A and B had distinct styles as anticipated, but Category A's quality was low and overpowering.
- Category C, tuned specifically for Alice's dataset, performed better with a higher score.

## Conclusion
This project explored the use of MusicGen to streamline Alice's music curation process. Although the model showed signs of learning, overfitting was detected, and subjective evaluation indicated room for improvement in audio quality and alignment with Alice's desired techno vibe.

## Future Work
- Increase the dataset size for better training.
- Utilize larger pretrained models for more complex learning.

## Links
- [Audio Samples](https://drive.google.com/drive/u/2/folders/1p3A9WAN2MfhQveneWGjX3ETGQywVIvpU)

## References
- Copet, J., Kreuk, F., Gat, I., Remez, T., Kant, D., Synnaeve, G., & Adi, Y. (2023). Simple and Controllable Music Generation. Thirty-seventh Conference on Neural Information Processing Systems.
- Lyryx (2023).
