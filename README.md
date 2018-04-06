# Rise of the Machines

This project has been heavily influenced by [this](https://github.com/arbox/machine-learning-with-ruby) awesome list. It has a ton of resources for those looking to get involved in machine learning in Ruby.

# Setup

Run `git clone https://github.com/lnchambers/rise_of_the_machines.git`

Run `bundle` in the root directory

Unzip the CSV files by running `unzip data/test.csv.zip` and `unzip data/train.csv.zip`

# Usage Instructions

Run the program using `ruby lib/neural_net.rb` from the root directory.

You can add many options to this command. They are listed below.

- `--alpha` sets the alpha as a float. The default is 0.05

- `--hidden_func` sets the hidden function. The functions are listed below. The default is `rect_lin`

- `--output_func` sets the output function. The functions are listed below. The default is `softmax`
  
  * Functions
    
    - `sin`, `sigmoid`, `tanh`, `rect_lin`, and `softmax`
    
- `--hidden_nodes` sets the amount of hidden nodes. Default is 300

- `--mode` sets the program to either train of eval. 

This will load the csv files into a data file that will be used to train the program. It will run by default through 60,000 iterations, but you can change this by changing the `i > 60000` on line 190 in neural_net.rb.

After the program is finished training, it will create a `w1.txt` and a `w2.txt` file. These are the saved trained values and will be used for the eval purposes. Run `ruby lib/neural_net.rb --mode eval` to test the trained values against the test.csv files. This creates a `test_results.csv` file that you can look at to check accuracy.

# Break Things

Please feel free to edit anything and see the effects of what it does. Break it and learn how to build it better.
