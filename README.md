Code for paper [KNN-BERT: Fine-Tuning Pre-Trained Models with KNN Classifier](https://arxiv.org/abs/2110.02523 "KNN-BERT: Fine-Tuning Pre-Trained Models with KNN Classifier")

 `python3.8 -m venv venv`
 
 `source venv/bin/activate`
 
 `pip install -r requirements.txt`
 
 How to run the script after virtual environment is created: 
 `mkdir logs`
 
 `mkdir output`
 
`python run_cluster_bert.py --task exalt --validation_file exalt_emotion_validate.csv --train_file exalt_emotion_train.csv --model_name_or_path Twitter/twhin-bert-large --output_dir output/ --do_train --load_model_pattern knn_bert --do_eval --do_train --num_train_epochs 5 --per_device_eval_batch_size 16 --logging_steps 1000 --save_steps 0 --overwrite_output_dir --evaluation_strategy epoch --learning_rate 1e-5 --top_k 10 --queue_size 100000 --fitlog_dir ./logs`