
---

# Instagram Reel Downloader API

This is a FastAPI-based backend application that allows you to download Instagram reel videos by providing the reel URL. The API extracts the video URL from the Instagram reel and returns it in JSON format.

## Features

- **Extract Video URL**: Given an Instagram reel URL, the API extracts the direct video URL.
- **CORS Enabled**: The API is configured to allow requests from any origin, making it easy to integrate with frontend applications.
- **Deployable on Vercel**: The project is configured for easy deployment on Vercel.

---

## Prerequisites

Before using or deploying this project, ensure you have the following:

1. **Python 3.7 or higher**: The project is built using Python and FastAPI.
2. **Vercel Account**: For deploying the application.
3. **GitHub Account**: To host the repository and connect it to Vercel.

---

## Setup Instructions

### 1. Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/instagram-reel-downloader.git
cd instagram-reel-downloader
```

### 2. Install Dependencies

Install the required Python packages using `pip`:

```bash
pip install -r requirements.txt
```

### 3. Run the Application Locally

Start the FastAPI server locally:

```bash
uvicorn api.instagram:app --reload
```

The API will be available at `http://localhost:8000`.

---

## Usage

### API Endpoint

- **Endpoint**: `/download`
- **Method**: `GET`
- **Query Parameter**:
  - `url`: The Instagram reel URL (e.g., `https://www.instagram.com/reel/Cxample123/`).

### Example Request

```bash
GET /download?url=https://www.instagram.com/reel/Cxample123/
```

### Example Response

If the URL is valid and the post is a video:

```json
{
    "video_url": "https://example.com/video.mp4"
}
```

If the URL is invalid or the post is not a video:

```json
{
    "error": "This is not a video post."
}
```

---

## Deploying to Vercel

1. **Push the Code to GitHub**:
   - Create a GitHub repository and push your code to it.

2. **Log in to Vercel**:
   - Go to [Vercel](https://vercel.com) and log in with your GitHub account.

3. **Import the Project**:
   - Click on "New Project" and select the GitHub repository where your code is hosted.

4. **Deploy**:
   - Vercel will automatically detect the `vercel.json` file and deploy the application.

5. **Access the API**:
   - Once deployed, Vercel will provide a URL (e.g., `https://your-app.vercel.app`). Use this URL to access the API.

---

## Project Structure

```
.
├── api
│   └── instagram.py       # FastAPI application
├── requirements.txt       # Python dependencies
├── vercel.json            # Vercel configuration
└── README.md              # Project documentation
```

---

## Technologies Used

- **FastAPI**: A modern, fast (high-performance) web framework for building APIs with Python.
- **Instaloader**: A Python library to download Instagram content.
- **Vercel**: A platform for deploying and hosting web applications.

---

## Contributing

Contributions are welcome! If you find any issues or want to improve the project, feel free to open a pull request.

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Support

If you encounter any issues or have questions, feel free to open an issue on GitHub or contact the maintainer.

---

Enjoy using the Instagram Reel Downloader API! 🚀

---
