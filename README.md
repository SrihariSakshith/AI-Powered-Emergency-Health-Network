# AI-Powered Emergency Health Network

## Introduction  
The AI-Powered Emergency Health Network is a real-time emergency response system designed to enhance healthcare accessibility, efficiency, and coordination. It provides live information on hospital availability, resources, and emergency services using AI and real-time data.

## Features  
- 🔹 AI-Powered Chatbot: Delivers intelligent, instant responses regarding hospitals and medical support.  
- 🔹 Live Hospital Database: Real-time display of hospital equipment, tests, and resource availability.  
- 🔹 User-Friendly Interface: Intuitive UI tailored for patients, hospital managers, and responders.  
- 🔹 Secure Data Management: Ensures the privacy and security of patient and hospital data.  
- 🔹 Geo-Location Based Search: Quickly find nearby hospitals and emergency facilities.

## Technologies Used  
- Frontend: React.js, HTML, CSS  
- Backend: Node.js, Express.js  
- Database: MongoDB Atlas  
- AI/ML: Natural Language Processing (NLP) for chatbot functionality  

## Demo & Links  
- ▶️ Demo Video : https://youtu.be/59m6fwLmNJI  
- 🚀 MVP        : https://ai-powered-emergency-health-network-frontend.vercel.app/  

## Installation

### Prerequisites  
- Node.js and npm installed  
- MongoDB Atlas account set up  

### Steps  
1. **Clone the Repository**  
   ```bash
   git clone https://github.com/SrihariSakshith/AI-Powered-Emergency-Health-Network.git
   ```

2. **Navigate to the Project Directory**  
   ```bash
   cd AI-Powered-Emergency-Health-Network
   ```

3. **Running the Application**

   The project is divided into frontend and backend. You need to run both separately.

   ### Frontend
   - Navigate to the frontend directory (if applicable).
   - Install dependencies:
     ```bash
     npm install
     ```
   - Start the frontend:
     ```bash
     npm start
     ```

   ### Backend
   - Navigate to the backend directory (if applicable).
   - Create a `.env` file in the backend root directory with the following variables:
     ```
     DATABASE_NAME="YourDatabaseName"
     MONGODB_URI="YourMongoDBAtlasURI"
     GEMINI_API_KEY="YourGeminiAPIKey"
     MONGO_URI="YourMongoDBAtlasURI"
     NODE_ENV=production
     PORT=3001
     ```
     > **Note:**  
     > - Do **not** use real API keys in the README.  
     > - The API keys/URIs mentioned above are for connecting to MongoDB Atlas and any additional APIs required by the backend.
     > - Please provide your own MongoDB Atlas connection strings and Gemini API Key as needed.

   - Install dependencies:
     ```bash
     npm install
     ```
   - Start the backend:
     ```bash
     npm start
     ```
## Database Structure

To ensure the code runs smoothly, please set up your database with the following structure. This project expects a relational database (such as MySQL or PostgreSQL) with tables as described below (adjust names/types if you use a different DBMS):

### Example Tables

#### Users
| Column Name     | Data Type    | Description                 |
|-----------------|-------------|-----------------------------|
| id              | INT/UUID    | Primary Key                 |
| name            | VARCHAR     | User's full name            |
| email           | VARCHAR     | User's email address        |
| password_hash   | VARCHAR     | Hashed password             |
| role            | VARCHAR     | (patient/doctor/admin/etc.) |

#### EmergencyRequests
| Column Name     | Data Type    | Description                     |
|-----------------|-------------|---------------------------------|
| id              | INT/UUID    | Primary Key                     |
| user_id         | INT/UUID    | Foreign key to Users            |
| status          | VARCHAR     | (pending/active/closed)         |
| location        | VARCHAR     | Location coordinates/address    |
| timestamp       | DATETIME    | Time of emergency request       |

#### Hospitals
| Column Name     | Data Type    | Description                |
|-----------------|-------------|----------------------------|
| id              | INT/UUID    | Primary Key                |
| name            | VARCHAR     | Hospital name              |
| address         | VARCHAR     | Hospital address           |
| phone           | VARCHAR     | Contact number             |
| capacity        | INT         | Current available capacity |

#### Ambulances
| Column Name     | Data Type    | Description                |
|-----------------|-------------|----------------------------|
| id              | INT/UUID    | Primary Key                |
| driver_name     | VARCHAR     | Ambulance driver name      |
| status          | VARCHAR     | (available/busy/offline)   |
| location        | VARCHAR     | Current ambulance location |

> **Note:**  
> - You may need to create additional tables for messages, logs, or other features depending on your project’s requirements.
> - If you are using an ORM (like SQLAlchemy, Django ORM, etc.), make sure your model definitions match the above schema.
> - Update your database credentials and connection settings in the project’s configuration files as needed.

4. **Access the Website**  
   - Once both frontend and backend are running, open [http://localhost:3000/](http://localhost:3000/) in your browser to view the application.

## Usage  
- 👤 As a Patient: Search nearby hospitals, view available equipment/resources, request help.  
- 🏥 As a Hospital Manager: Update and manage hospital resources, handle emergency cases.  

## Contributing  
We welcome contributions!  

1. Fork the repository  
2. Create a feature branch  
   ```bash
   git checkout -b new-feature
   ```  
3. Commit your changes  
   ```bash
   git commit -m 'Add new feature'
   ```  
4. Push to your branch  
   ```bash
   git push origin new-feature
   ```  
5. Create a pull request  

## License  
This project is licensed under the MIT License.

## Contact  
For questions or feedback, contact:  
📧 kotichintalasriharisakshith@gmail.com  
🔗 LinkedIn: [Srihari Sakshith Kotichintala](https://linkedin.com/in/srihari-sakshith-kotichintala-1a1a8a280)
