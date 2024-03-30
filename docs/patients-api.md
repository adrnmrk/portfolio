# Patients API Documentation

### Base URL
- **Base URL**: `http://127.0.0.1:3000`

### Endpoints

#### GET /patients
- **Description**: Get all patients in the system.
- **Response**: Returns a list of all patients.

#### GET /patients/:id
- **Description**: Get a single patient by their patient ID.
- **Parameters**:
  - `id`: The unique ID of the patient.
- **Response**: Returns the patient data if found, otherwise returns a 404 error.

#### POST /patients
- **Description**: Create a new patient in the system.
- **Request Body**: JSON object containing patient information.
- **Response**: Returns the created patient data with a status code of 201.

#### PUT /patients/:id
- **Description**: Update user details with the given ID.
- **Parameters**:
  - `id`: The unique ID of the patient.
- **Request Body**: JSON object containing the updated patient information.
- **Response**: Returns the updated patient data if successful, otherwise returns a 404 error.

#### DELETE /patients/:id
- **Description**: Delete a patient with the given ID along with their associated clinical data.
- **Parameters**:
  - `id`: The unique ID of the patient.
- **Response**: Returns the deleted patient data if successful, otherwise returns a 404 error.

#### POST /patients/:id/clinicaldata
- **Description**: Add clinical data for a specific patient and update the critical condition status.
- **Parameters**:
  - `id`: The unique ID of the patient.
- **Request Body**: JSON object containing clinical data.
- **Response**: Returns the created clinical data with a status code of 201.

#### GET /patients/:id/clinicaldata
- **Description**: Retrieve all clinical data for a specific patient.
- **Parameters**:
  - `id`: The unique ID of the patient.
- **Response**: Returns a list of clinical data associated with the patient.

#### DELETE /patients/:id/clinicaldata/:clinicalDataId
- **Description**: Delete specific clinical data for a patient by ID.
- **Parameters**:
  - `id`: The unique ID of the patient.
  - `clinicalDataId`: The unique ID of the clinical data to delete.
- **Response**: Returns a success message if the clinical data is deleted successfully, otherwise returns a 404 error.

#### GET /patients/critical
- **Description**: Retrieve patients in critical condition based on their latest clinical data.
- **Response**: Returns a list of patients in critical condition.