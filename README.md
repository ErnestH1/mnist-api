
<!-- Environment: Python 3
Build Command: pip install -r requirements.txt
Start Command: uvicorn main:app --host 0.0.0.0 --port 8000
Port: 8000 (default) -->


# MNIST API

This API uses a Convolutional Neural Network (CNN) model to predict handwritten digits from the MNIST dataset. It is built using FastAPI and TensorFlow.

## Description

The MNIST API allows users to upload images of handwritten digits and get predictions from a pre-trained CNN model. The model was trained on the MNIST dataset, which consists of 28x28 grayscale images of handwritten digits (0-9).

## Usage

### Endpoints

- **GET `/`**
  - Returns a brief description of the API and its purpose.

- **POST `/predict`**
  - Accepts an image file (PNG or JPG) of a handwritten digit.
  - Returns a JSON response with the predicted digit as an integer.

### Example

To use the API:

1. Send a POST request to `/predict` with an image file containing a handwritten digit.
2. Receive a JSON response with the predicted digit.

### Example Usage

```bash
curl -X 'POST' \
  'https://your-mnist-api-url.com/predict' \
  -H 'accept: application/json' \
  -H 'Content-Type: multipart/form-data' \
  -F 'file=@/path/to/your/image.png'
```

## Setup

### Requirements

- Python 3.x
- Dependencies listed in `requirements.txt`
- Pre-trained `mnist_cnn_model.keras` model file

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/ErnestH1/mnist-api.git
   cd mnist-api
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the API locally:

   ```bash
   uvicorn main:app --reload
   ```

4. Open your browser or use tools like `curl` to interact with the API.

## Deployment

The API can be deployed on various platforms such as Render, Vercel, or Heroku. Ensure to set up environment variables and configurations specific to your deployment platform.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

