# Environment Preparation HuggingeFace

1. create virtual environment

   ``` bash
   conda create -n huggingface python=3.10.11
   ```

2. install and set jupyter kernel

   ``` bash
   conda install ipykernel
   conda install -c conda-forge ipywidgets
   ```

   Add this environment to `jupyter`:

   ``` bash
   python -m ipykernel install --user --name=huggingface
   ```

3. install python-dotenv

   ``` bash
   pip install python-dotenv
   ```

4. install pytorch

   ``` bash
    conda install pytorch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2 pytorch-cuda=12.1 -c pytorch -c nvidia
   ```

5. install tensorboard

   ``` bash
   conda install tensorboard
   ```

6. Install Hugging Face libraries

   ``` bash
   pip install --upgrade \
    "transformers==4.36.2" \
    "datasets==2.16.1" \
    "accelerate==0.26.1" \
    "evaluate==0.4.1" \
    "bitsandbytes==0.42.0"
   ```

7. install peft & trl from github

   ``` bash
   pip install git+https://github.com/huggingface/trl@a3c5b7178ac4f65569975efadc97db2f3749c65e --upgrade
   pip install git+https://github.com/huggingface/peft@4a1559582281fc3c9283892caea8ccef1d6f5a4f --upgrade
   ```

8. install flash-attn

   ``` bash
   pip install 'pybind11>=2.12' 'numpy<2'
   pip install ninja packaging
   MAX_JOBS=4 pip install flash-attn --no-build-isolation
   ```

   

