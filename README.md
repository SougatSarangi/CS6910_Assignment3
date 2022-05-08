# CS6910_Assignment3
AUTHORS:  Sougat Kumar Sarangi (CE21D300) and Anuj Pandey (CS22Z009)

1. Run the following code to run at best model:
 
```
  model = test_on_dataset(language="hi",
                        embedding_dim=256,
                        encoder_layers=3,
                        decoder_layers=3,
                        layer_type="lstm",
                        units=256,
                        dropout=0.2,
                        attention=False)
```
2. Run the following sweep for Attention Sweep:

```
sweep_config4 = {
  "name": "Attention Sweep - Assignment3",
  "description": "Hyperparameter sweep for Seq2Seq Model with Attention",
  "method": "grid",
  "parameters": {
        "enc_dec_layers": {
           "values": [1, 2, 3]
        },
        "units": {
            "values": [128, 256]
        },
        "dropout": {
            "values": [0, 0.2]
        },
        "attention": {
            "values": [True]
        }
    }
}
```
3. Other sweep functions for different parameters are also available and has been separated into individual cells.
4. For getting the word cloud run the following code
```
visualize_model_outputs(model, n=20)
```
5. Change the location of Dakshina dataset in the following part to your local file location where you have stored it:
```
def get_data_files(language):

    template = "/content/drive/MyDrive/dakshina_dataset_v1.0/{}/lexicons/{}.translit.sampled.{}.tsv"

```
