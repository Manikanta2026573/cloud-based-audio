Cloud Audio Translator: Seamless Multilingual Communication with AWS

**Home Page Screenshot**

This is the main interface of the Cloud Audio Translator web application.
Users can upload an audio file in .mp3 format through this page.

The frontend is developed using HTML, CSS, and JavaScript, and it connects with AWS backend services through API Gateway.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/13bf5a3f-7007-43a2-871f-02175b673c9e" />

  **Upload Audio Screenshot**
🎧 Audio Upload Process

This screenshot shows the audio upload functionality.
When a user selects an audio file and clicks upload:

A pre-signed URL is generated using AWS Lambda

The audio file is securely uploaded to Amazon S3 input bucket

The file is processed automatically for transcription

<img width="1238" height="696" alt="image" src="https://github.com/user-attachments/assets/65b37e0c-6b6d-4bd9-b60c-00aa605c0097" />

  **AWS S3 Input Bucket Screenshot**
☁️ Amazon S3 Input Bucket

The uploaded audio files are stored in the S3 input bucket.
Each file is stored with a dynamically generated filename for security and uniqueness.

S3 ensures high durability and availability for audio storage.
<img width="1258" height="708" alt="image" src="https://github.com/user-attachments/assets/4fb3fb7b-6f56-4b8a-afff-d97cc293c1d8" />

  **Lambda Function Screenshot**
⚙️ AWS Lambda Processing

AWS Lambda is used to:

Generate pre-signed upload URLs

Trigger transcription process

Process audio files

Store output text file in S3 output bucket

This enables a fully serverless backend architecture.
<img width="1292" height="627" alt="image" src="https://github.com/user-attachments/assets/9b0631ee-bfaf-42be-ad62-ba992ff52765" />

  **Translated Output Screenshot**
🌍 Translated Text Output

After processing, the translated text is generated and saved in the S3 output bucket.
The frontend fetches the output text file using a GET API and displays it instantly to the user.
<img width="1238" height="696" alt="image" src="https://github.com/user-attachments/assets/60f868c4-a8b7-4265-9f39-e53b258e123d" />
