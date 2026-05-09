# Pixels to Predictions

## Setup

### 1. Google Drive Folder Structure

```
MyDrive/
└── dl_finals/
    ├── train.csv
    ├── val.csv
    ├── test.csv
    ├── images/
    │   ├── train/
    │   ├── val/
    │   └── test/
    └── checkpoints/
        └── smolvlm-weights-final/   ← starting checkpoint
```

The notebook will create `dl_finals/checkpoints/smolvlm-weights-final-run/` for new weights and `dl_finals/submission.csv` for predictions automatically.

### 2. Runtime

## Running the Notebook

Run all cells in order.

## Output

Once inference completes, predictions are saved to:
```
/content/drive/MyDrive/dl_finals/submission.csv
```

---

## Resuming After a Colab Timeout

If your session disconnects mid-training:

1. Check `dl_finals/checkpoints/` for the last saved checkpoint folder.
2. Update `prev_check_dir` in the CFG cell to point to it.
3. Reduce `epochs` to however many are left.
4. Re-run from the CFG cell onward (skip the pip install if packages are still cached).
