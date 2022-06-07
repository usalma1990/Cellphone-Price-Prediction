# INTRODUCTION
Machine learning is a field of computer science that gives computers the ability to learn without being explicitly programmed. Machine learning can be categorized into supervised and unsupervised machine learning. 
Supervised ML Contains labelled data and target. It involves somehow modeling the relationship between measured features of data and some label associated with the data; once this model is determined, it can be used to apply labels to new, unknown data. This is further subdivided into classification tasks and regression tasks: in classification, the labels are discrete categories, while in regression, the labels are continuous quantities. Cellphone price prediction falls under classification task. 
Supervised ML examples include image classification, house price prediction, weather forecasting etc 
Unsupervised ML has no labelled data. Various unsupervised ML examples include recommendation system, Targetted Marketing, Customer Segmentation etc

The dataset used for cellphone price prediction is mobile_price.csv

##Specification of Cell phone

battery_power : Energy stored by battery measured in mAh
blue : Contains bluetooth, yes or no 
clock_speed :	speed at which microprocessor works 
dual_sim	: Has dual sim, yes or no 
fc	: Front Camera mega pixels  
four_g	: Supports 4G, Yes or no 
int_memory	: Internal Memory in Gigabytes
m_dep	: mobile depth in centimeters
mobile_wt :	mobile weight 
n_cores	: Number of cores present in processor 
pc	: Primary camera mega pixels 
px_height :	Height of the pixel resolution
px_width : Width of the pixel resolution
ram	: Capacity of Random Access Memory in Megabytes
sc_h :	Height of mobile screen in centimeters 
sc_w :	Width of mobile screen in centimeters 
talk_time :	Time duration of single battery charge 
three_g :	Supports 3g signal, yes or no 
touch_screen :	Supports toch screen, yes or no 
wifi :	Enabled with wifi signal, yes or no
price_range : Cellphone price range from 0 to 3 


##Defining Variables

y <- dependent variable = target variable = price_range 
x <- independent variable = predictor variable = battery_power, blue, clock_speed, dual_sim, fc, four_g, int_memory, m_dep, mobile_wt, n_cores, pc, px_height, px_width, ram, sc_h, sc_w, talk_time, three_g, touch_screen and wifi. 

##Feature Selection

Heatmap is used to identify the features that are related to target variable and the same is plotted using seaborn library. Here, it has been observed that RAM is highly correlated with price range followed by battery_power, pixel width and height 

##Modelling 

Random Forest Algorithm gives and accuracy of 86.83%

##Hyperparameter tuning

Inorder to get better outcome, hyperparameter tuning is performed. Here, different values are set for random_state to check which value gives maximum accuracy. Here, random_state=10


##Model Evaluation

The cellphone price model is evaluated based on accuracy. Here, crosstab has been used. 
