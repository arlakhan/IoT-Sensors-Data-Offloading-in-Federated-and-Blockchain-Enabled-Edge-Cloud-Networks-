This Python application simulates a Federated Learning system with IoT sensors, Blockchain, and Edge-Cloud offloading. It uses Flask to create a web service that allows communication with the system. Here's a breakdown of the key components:

IoT Sensors Simulation:

The system simulates 100 IoT sensors. Each sensor generates data, which is stored in a dictionary called SENSOR_DATA.
Blockchain for Data Integrity:

A Blockchain class is used to ensure the integrity of the sensor data. The data is hashed and added to a chain of blocks.
Each sensor's data is stored as a block in the blockchain, ensuring secure and immutable data storage.
Federated Learning Simulation:

Global Model: A simple neural network model is defined using TensorFlow (global_model) to simulate federated learning.
Training: The train_local_model function simulates local training on data received from sensors. Random data is used as training data, and the model is trained for a few epochs.
Aggregation: The aggregate_models function aggregates local model updates from both edge and cloud nodes to update the global model.
Flask API Routes:

/iot_data: Receives sensor data in JSON format and stores it both locally and in the blockchain.
/offload: Simulates offloading sensor data to edge and cloud networks by returning all the sensor data.
/federated_learning: Receives local model updates from edge/cloud nodes and aggregates them into the global model.
/blockchain: Returns the current state of the blockchain (all stored data).
/sensor_data: Returns all the sensor data collected by the system.
Ngrok for Exposing Flask App:

The ngrok tool is used to expose the Flask application over the internet by creating a public URL.
The Flask app runs on port 5000, and Ngrok creates a tunnel to provide an external URL to access the service.
Simulation of Sensor Data:

The simulate_sensor_data function generates random temperature data (between 20.0 and 30.0) for each sensor every second to simulate real-time data generation.
Flow:
IoT Data is received via the /iot_data endpoint, stored in SENSOR_DATA, and added to the blockchain.
Data Offloading happens via the /offload endpoint, which simulates sending data to the edge/cloud.
Federated Learning is triggered via the /federated_learning endpoint, where local updates from the edge and cloud nodes are aggregated to update the global model.
The Blockchain and Sensor Data can be queried through the /blockchain and /sensor_data endpoints, respectively.
Example Use Cases:
IoT Data Management: Collect and securely store data from a network of IoT sensors.
Federated Learning: Train models on edge and cloud devices without transferring raw data.
Blockchain Integration: Ensure data integrity by storing sensor readings on an immutable blockchain.
Edge-Cloud Data Offloading: Simulate offloading sensor data to the edge or cloud for further processing and training.
Running the Application:
The app is hosted using Flask, and a public URL is generated using Ngrok.
The Flask server runs on port 5000, and you can interact with it via the exposed Ngrok URL (printed in the console).
This system represents a simplified federated learning workflow with edge-cloud processing and blockchain for IoT applications. It can be extended with more complex models, security features, and real-world sensor data integration.


![Federated Learning and Blockchain](https://github.com/user-attachments/assets/f80a56ec-3246-44df-838a-dc598de7949a)


Simulation Results

Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.50388034, 0.51845474, 0.61328347, 0.3628226 , 0.52360033,
       0.26367163, 0.37984917, 0.45891489, 0.55070689, 0.6515985 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.33693224, 0.55808519, 0.40792452, 0.41084449, 0.32148075,
       0.38299692, 0.53287264, 0.48390555, 0.6398581 , 0.65993694])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.73258705, 0.54740021, 0.41866624, 0.36165553, 0.32904938,
       0.46017284, 0.49819374, 0.62627855, 0.61206825, 0.4615961 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.49172636, 0.59415255, 0.27127203, 0.74549922, 0.56176308,
       0.48929114, 0.5295078 , 0.53474989, 0.7010335 , 0.50309197])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.52104366, 0.49951101, 0.52942471, 0.5468374 , 0.59043823,
       0.60624688, 0.50809669, 0.52512106, 0.43418452, 0.52475732])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.58046983, 0.62161764, 0.58309188, 0.30694468, 0.49481373,
       0.48787944, 0.5479942 , 0.49540908, 0.61669572, 0.46973774])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.3918127 , 0.43563791, 0.56769814, 0.42044945, 0.43669728,
       0.50805523, 0.50891735, 0.3818822 , 0.42621431, 0.52106645])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.33990968, 0.51521081, 0.58577522, 0.56819538, 0.61166511,
       0.26724357, 0.52144195, 0.41990499, 0.27899154, 0.36290931])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.55630149, 0.28265224, 0.46748686, 0.58170757, 0.48083509,
       0.37247631, 0.44124991, 0.38170584, 0.52355687, 0.57913725])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.44878274, 0.31153632, 0.32840528, 0.37068369, 0.53256408,
       0.48702747, 0.41671238, 0.43249619, 0.6503377 , 0.41586497])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.36486318, 0.53186278, 0.40864291, 0.51802833, 0.53510275,
       0.3443319 , 0.65124657, 0.5375518 , 0.37991998, 0.50781037])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.44701884, 0.73459317, 0.43475992, 0.34019925, 0.54957084,
       0.51873864, 0.50584697, 0.3698268 , 0.52049639, 0.62426796])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.46261356, 0.56159243, 0.48709793, 0.5450494 , 0.56272817,
       0.50957481, 0.56075195, 0.54903846, 0.46294318, 0.51914108])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.46908718, 0.41771813, 0.45838138, 0.49967885, 0.42788494,
       0.41767325, 0.57711823, 0.45359438, 0.33417394, 0.44354345])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.38775832, 0.50991339, 0.45946852, 0.29046441, 0.52094602,
       0.62746702, 0.5282245 , 0.42997236, 0.50979084, 0.46975258])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.34730157, 0.58939611, 0.52143857, 0.4969069 , 0.68613798,
       0.51319158, 0.48588814, 0.47191294, 0.45845462, 0.45807474])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.25369247, 0.64998774, 0.60836579, 0.53911509, 0.48418095,
       0.35674037, 0.35738304, 0.38256387, 0.55061722, 0.53961921])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.27942255, 0.723435  , 0.38195413, 0.74445096, 0.41648367,
       0.73672962, 0.56407424, 0.44474082, 0.58326527, 0.66895012])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.43634113, 0.27786799, 0.44661617, 0.46251073, 0.57490484,
       0.62961525, 0.56666715, 0.37393652, 0.42357753, 0.51831813])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.65442737, 0.5278054 , 0.62743466, 0.44941664, 0.52918113,
       0.39612552, 0.49763278, 0.3501695 , 0.49922431, 0.55235712])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.69477492, 0.40368339, 0.55343847, 0.3398333 , 0.50786765,
       0.43960767, 0.56625891, 0.55041185, 0.56615404, 0.40884133])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.46664333, 0.41215502, 0.61035122, 0.31439037, 0.7234629 ,
       0.49738709, 0.58477522, 0.41847251, 0.50319671, 0.46152181])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.39416016, 0.41262119, 0.30180475, 0.37167451, 0.52221121,
       0.29570501, 0.52406772, 0.58055779, 0.69751105, 0.38548654])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.4625652 , 0.32529661, 0.46586085, 0.58508907, 0.49471374,
       0.53958763, 0.47085593, 0.5956072 , 0.61625613, 0.48430751])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.4851961 , 0.4638162 , 0.42910563, 0.57630358, 0.61469707,
       0.39391871, 0.52382414, 0.42258855, 0.70520922, 0.35336752])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.5513165 , 0.35438848, 0.58330471, 0.41149356, 0.51308042,
       0.61338868, 0.76933952, 0.56236144, 0.64790726, 0.4226729 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.56531771, 0.57369099, 0.51211209, 0.33340763, 0.39872762,
       0.66584157, 0.35576099, 0.28824924, 0.62099385, 0.35257943])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.69261028, 0.56207608, 0.35993705, 0.40938063, 0.61752644,
       0.44371725, 0.7941975 , 0.57786986, 0.45427368, 0.62317315])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.4597332 , 0.60423777, 0.52585564, 0.6425453 , 0.47459134,
       0.61490016, 0.35124165, 0.23790505, 0.65688606, 0.22222295])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.47922836, 0.35688316, 0.54625895, 0.36540474, 0.47311128,
       0.38496015, 0.52477628, 0.46582498, 0.55088785, 0.5143395 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.44114469, 0.31880205, 0.50384047, 0.44986436, 0.55261042,
       0.64279483, 0.52766207, 0.43538583, 0.60269281, 0.69696567])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.43847005, 0.59628294, 0.45742584, 0.58822351, 0.61039432,
       0.51015835, 0.48563717, 0.29641967, 0.5030749 , 0.58534837])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.47780936, 0.46780252, 0.66642894, 0.4975966 , 0.36643525,
       0.50991807, 0.50417923, 0.53590127, 0.35981719, 0.51297495])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.59064038, 0.52332153, 0.35206692, 0.42616622, 0.7317563 ,
       0.54573502, 0.39300929, 0.4202158 , 0.29945808, 0.60549713])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.58578814, 0.24337762, 0.46637174, 0.39260509, 0.54571952,
       0.49391489, 0.74797144, 0.33697297, 0.58251603, 0.63305629])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.54041206, 0.49552092, 0.42739849, 0.56384444, 0.49470631,
       0.52462525, 0.63838949, 0.61880214, 0.53503654, 0.49672679])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.27116033, 0.3653877 , 0.4202583 , 0.44065452, 0.43001821,
       0.33388024, 0.57778284, 0.50458555, 0.63927725, 0.58050785])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.55763415, 0.43590216, 0.64010294, 0.5622663 , 0.64450579,
       0.54575686, 0.57347124, 0.52165687, 0.47162362, 0.35705428])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.67112294, 0.31291549, 0.6020475 , 0.36288874, 0.48541108,
       0.50581037, 0.46274846, 0.50776042, 0.45576506, 0.57915085])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.49849101, 0.54752731, 0.6287632 , 0.60374316, 0.4362134 ,
       0.48667813, 0.72245543, 0.55932037, 0.39370072, 0.34105409])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.55023867, 0.49810248, 0.6730887 , 0.46834719, 0.61246965,
       0.51859584, 0.34829151, 0.56144771, 0.65021272, 0.7560617 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.53635951, 0.50251345, 0.64536132, 0.29184806, 0.42803192,
       0.52999105, 0.66375929, 0.66329207, 0.44962273, 0.50078834])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.46934847, 0.34110902, 0.36644284, 0.50143895, 0.52748799,
       0.52827543, 0.59159949, 0.53076624, 0.26351844, 0.50236955])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.76830831, 0.41222842, 0.73539061, 0.48330654, 0.38397096,
       0.45278983, 0.41486568, 0.7946502 , 0.63471092, 0.49417217])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.48257146, 0.40953799, 0.53947086, 0.56658316, 0.59199948,
       0.48619502, 0.44926209, 0.64603631, 0.41301933, 0.58768184])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.48323859, 0.42885284, 0.45346316, 0.31197786, 0.51821085,
       0.6003585 , 0.50079624, 0.46780008, 0.72248351, 0.5941856 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.43728757, 0.43579061, 0.58937675, 0.65125725, 0.62040619,
       0.50649181, 0.32852558, 0.52392317, 0.52923685, 0.24287244])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.47284342, 0.74105396, 0.53766529, 0.66548593, 0.58084194,
       0.43720023, 0.51053337, 0.46014378, 0.46632793, 0.66925705])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.59329869, 0.47597403, 0.57027617, 0.54328496, 0.44334415,
       0.53578831, 0.63829672, 0.53967575, 0.54808592, 0.38655361])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.46344926, 0.2888609 , 0.50783492, 0.48060937, 0.55092132,
       0.44285555, 0.32704093, 0.4722753 , 0.45566158, 0.42293998])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.47542671, 0.37330959, 0.45014762, 0.33059665, 0.31354098,
       0.52540023, 0.56724199, 0.4099807 , 0.56420733, 0.45557863])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.45598989, 0.47602975, 0.64198568, 0.45826389, 0.52163763,
       0.44137625, 0.57708093, 0.58850649, 0.46591972, 0.4483595 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.46180052, 0.49684772, 0.49355656, 0.61066542, 0.71483778,
       0.44865877, 0.5798959 , 0.50290731, 0.4250957 , 0.49771491])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.52705883, 0.48943627, 0.73062841, 0.50900117, 0.42410408,
       0.48269771, 0.41788141, 0.43875733, 0.51650945, 0.35205137])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.54522772, 0.39194997, 0.42226048, 0.53491787, 0.52158069,
       0.42271806, 0.57649353, 0.5123364 , 0.59126952, 0.61076757])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.48298895, 0.40081737, 0.5677577 , 0.42118355, 0.34730868,
       0.35649422, 0.4533738 , 0.47518059, 0.37270278, 0.6656764 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.51408562, 0.64840551, 0.30897072, 0.35185478, 0.48258005,
       0.75305225, 0.52408909, 0.62917627, 0.44110725, 0.38339839])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.42304102, 0.49362059, 0.39447749, 0.46466812, 0.44316354,
       0.37254705, 0.37555887, 0.6083769 , 0.30736211, 0.6121628 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.55751691, 0.49637137, 0.56505988, 0.49269752, 0.54933994,
       0.45496015, 0.53313935, 0.4267788 , 0.56164406, 0.45557831])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.54875225, 0.74330805, 0.624052  , 0.6695421 , 0.56138363,
       0.55975045, 0.69465654, 0.49473227, 0.40071989, 0.40535356])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.58085855, 0.38981691, 0.56699308, 0.44027151, 0.57108594,
       0.52343392, 0.45695046, 0.65875942, 0.55735072, 0.51607133])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.44754076, 0.60345912, 0.51057101, 0.46649519, 0.39192677,
       0.33974465, 0.33997207, 0.41709245, 0.58812275, 0.40927115])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.42829782, 0.67601863, 0.43028806, 0.43059996, 0.77207059,
       0.44757884, 0.51366504, 0.39493508, 0.55718766, 0.59677545])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.39307115, 0.51246755, 0.41591518, 0.7058836 , 0.54570859,
       0.39511464, 0.46719692, 0.61974959, 0.61830983, 0.48469307])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.55628616, 0.55631256, 0.44978531, 0.65227244, 0.44647154,
       0.4810895 , 0.31984439, 0.4265326 , 0.55056737, 0.48840163])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.56585238, 0.22847854, 0.56218946, 0.30567911, 0.54743555,
       0.62081009, 0.26900565, 0.52096428, 0.56281071, 0.53237466])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.50277955, 0.46434673, 0.55844707, 0.43330634, 0.54982258,
       0.40682199, 0.38578287, 0.38491194, 0.46074881, 0.5236631 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.68937234, 0.71412794, 0.59691996, 0.52404295, 0.26299467,
       0.31967581, 0.41485666, 0.52627092, 0.58064477, 0.4835617 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.5617403 , 0.32100839, 0.59220839, 0.5371429 , 0.35705766,
       0.4672517 , 0.66921638, 0.58081112, 0.48973149, 0.52471121])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.40094761, 0.61615531, 0.2783937 , 0.67104562, 0.59042491,
       0.62817319, 0.70240199, 0.37304177, 0.48656055, 0.55445956])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.42510506, 0.42775617, 0.45632848, 0.48080155, 0.43302311,
       0.50464936, 0.38178633, 0.61894023, 0.52770168, 0.41510924])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.43561828, 0.54573503, 0.64788951, 0.38246383, 0.26190476,
       0.46253772, 0.5951533 , 0.45362023, 0.52129236, 0.4505202 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.40722972, 0.51768396, 0.57528662, 0.5127938 , 0.66625441,
       0.48027465, 0.66954456, 0.36339212, 0.77166859, 0.22787256])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.21184084, 0.53326039, 0.62948078, 0.69784933, 0.53516226,
       0.4956796 , 0.42494818, 0.70044588, 0.50841967, 0.590557  ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.6968188 , 0.19465736, 0.40379874, 0.64494996, 0.53829432,
       0.80179955, 0.51969549, 0.39610917, 0.55449828, 0.53583429])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.53197889, 0.46954508, 0.47441161, 0.3833976 , 0.46460753,
       0.58705697, 0.39976781, 0.40162728, 0.45301196, 0.50505929])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.34846795, 0.61729137, 0.59561134, 0.27741947, 0.43995626,
       0.79150671, 0.42225437, 0.38329232, 0.41169397, 0.34610366])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.39277421, 0.46952792, 0.28932008, 0.66903194, 0.44907416,
       0.46541068, 0.59746319, 0.54199361, 0.54677473, 0.27147509])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.44812116, 0.49034928, 0.53277829, 0.44061293, 0.70432788,
       0.44877091, 0.52457901, 0.50145953, 0.36319624, 0.51571291])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.65392098, 0.5066492 , 0.42571619, 0.46097226, 0.48659003,
       0.60377345, 0.42343384, 0.4529754 , 0.54992765, 0.4120187 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.62575115, 0.37844444, 0.42579384, 0.58544781, 0.39120193,
       0.36170157, 0.62369224, 0.40241894, 0.58503801, 0.39526642])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.62028929, 0.2224012 , 0.23724795, 0.68514688, 0.38027835,
       0.51576998, 0.63242365, 0.33233438, 0.56204827, 0.585076  ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.54448792, 0.56464041, 0.3948368 , 0.58926922, 0.44512365,
       0.39339016, 0.29739488, 0.61266335, 0.30208447, 0.45322382])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.58071001, 0.70385752, 0.51228063, 0.5199309 , 0.46823517,
       0.50900628, 0.35383497, 0.64643379, 0.56719561, 0.4498439 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.55920223, 0.53695462, 0.40005147, 0.53688475, 0.51090358,
       0.56827277, 0.39928811, 0.2307249 , 0.63253958, 0.2622077 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.66680815, 0.42765174, 0.5016823 , 0.52887755, 0.58300142,
       0.40648871, 0.56069485, 0.30266983, 0.58715534, 0.51754571])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.64883777, 0.4777011 , 0.67983192, 0.67131062, 0.59371652,
       0.39282501, 0.54364992, 0.41385107, 0.4584761 , 0.39865335])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.37469614, 0.5974113 , 0.56764992, 0.51971372, 0.5322149 ,
       0.31877908, 0.51771394, 0.78973468, 0.38111454, 0.6464885 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.48503676, 0.69824476, 0.56436121, 0.64005734, 0.53457463,
       0.35355393, 0.28799136, 0.5315627 , 0.51722521, 0.46994257])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.46249487, 0.37480493, 0.54671717, 0.30555384, 0.45627487,
       0.50144842, 0.42135679, 0.47847147, 0.41914674, 0.52969035])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.5913736 , 0.66137372, 0.43666042, 0.4096399 , 0.59701843,
       0.66412859, 0.46768952, 0.4746355 , 0.57022198, 0.54590106])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.53899   , 0.45756029, 0.52540486, 0.5018635 , 0.41260885,
       0.49222037, 0.62062111, 0.61026018, 0.47275515, 0.45117525])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.35662342, 0.6332342 , 0.55086999, 0.43178234, 0.42819709,
       0.43990416, 0.47352123, 0.50033383, 0.56231997, 0.32780132])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.36565041, 0.39244403, 0.42574737, 0.50651151, 0.39907271,
       0.67269149, 0.46268985, 0.42274519, 0.48723807, 0.4940526 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.40156624, 0.45319088, 0.33451231, 0.3734716 , 0.6055042 ,
       0.48134587, 0.57732725, 0.47615795, 0.53054054, 0.61059858])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.53200762, 0.66050174, 0.54858528, 0.2964193 , 0.46056163,
       0.55813262, 0.49348184, 0.270729  , 0.34335035, 0.4761224 ])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.414504  , 0.3854842 , 0.56241034, 0.48406395, 0.54842827,
       0.6397159 , 0.34472029, 0.52738193, 0.57492373, 0.52159167])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.5041232 , 0.3670404 , 0.45361322, 0.61061937, 0.60415935,
       0.37949602, 0.44038888, 0.6726564 , 0.61765047, 0.71662966])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.67693424, 0.38470212, 0.3924416 , 0.21942519, 0.63556259,
       0.50647792, 0.55895341, 0.44587861, 0.76176326, 0.57225778])}
Edge edge_1 updated model with local data.
Edge edge_2 updated model with local data.
Edge edge_3 updated model with local data.
Edge edge_4 updated model with local data.
Edge edge_5 updated model with local data.
Cloud cloud_1 updated model with local data.
Cloud cloud_2 updated model with local data.
Global model updated: {'weights': array([0.59518428, 0.47431568, 0.37774782, 0.43026521, 0.60235788,
       0.36772061, 0.34896952, 0.72732512, 0.5490691 , 0.32000092])}
