# Image Captioning on Flickr8k Using Encoder-Decoder Models

### Download Flickr8k
Download the [Flickr8k Dataset](https://www.kaggle.com/datasets/adityajn105/flickr8k), and unzip into a `flickr8k` directory

### Set up virtual environment
    python3 -m venv venv
    . venv/bin/activate

### Install requirements
    pip install -r requirements.txt

### Download spacy vocab
    python -m spacy download en_core_web_sm

### Run training loop
    python main.py

### Choosing the model type
We provide both LSTM and GRU based models. Please see `model.py` and `model_gru.py` respectively.

### Evaluating Models
- We have a notebook comparing the epoch losses of each model in `model_comparison_graphs.ipynb`.

Please see the `results/` directory for epoch loss data in csv files. We've included 
`.ipynb` notebooks for each model to analyze various metrics and run inference.

    1. `resnext_gru_eval_3_layer.ipynb`
    2. `resnext_lstm_eval_single_layer.ipynb`
    3. `resnext_lstm_eval_3_layer.ipynb`
    4. `resnext_gru_eval_single_layer.ipynb`


`eval.ipynb` is provided as a reference template notebook for evaluating a model.

NOTE: `.pt` model files/weights are available upon request. We have NOT included
them in this repository due to the size of the model files exceeding GIT allowable limits.
