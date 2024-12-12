# Vector-Embeddings-for-Video
Using Python Notebook, OpenAI CLIP, and Singlestore

The notebooks stores and scans a video. It clips it into images and allows a query phrase that it searches for in the clipped images. It then selects the top 5 images, indexes them so they're easier to search later, and stores them in the database.

## Repository
For the demo I used the files from this repository
https://github.com/VeryFatBoy/clip-demo

### I set up my Singlestore demo account on AWS and created my Workspace

![image](https://github.com/user-attachments/assets/498e94ee-558e-4681-be7e-c1a5a3691336)

### I uploaded the jupyter notebook from the repository.

![image](https://github.com/user-attachments/assets/4e4fa823-6a14-4c6d-970f-bd41f80ae6d6)

### I downloaded the appropriate python libraries in the notebook.

![image](https://github.com/user-attachments/assets/efa9ed89-1938-4adf-90c8-34d99da4d3c0)
![image](https://github.com/user-attachments/assets/eab390fa-ba86-4a6c-9b52-bf2f3054c7b4)

### Next save the video.

![image](https://github.com/user-attachments/assets/96c23346-bb85-46db-b037-be3fef6ca80c)

### I played the video to make sure it was pulled properly from the URL.

![image](https://github.com/user-attachments/assets/c312d93b-31f9-4b92-895f-829cde46e9f1)

### Load the CLIP model to clip the video.

![image](https://github.com/user-attachments/assets/42226de0-e695-4d3c-813c-a0c88ede7ff1)

### I extracted frames in 1 second intervals.

![image](https://github.com/user-attachments/assets/471f959b-ae3a-4e0e-b455-6784cf06854b)

### Next generate embeddings for each frame and stored the embeddings and image data in a Pandas Dataframe.

![image](https://github.com/user-attachments/assets/b19635b7-0b61-47a4-80f9-9a229f03abac)
![image](https://github.com/user-attachments/assets/6f9cf9a1-ea5a-47da-9219-36f14d222279)
![image](https://github.com/user-attachments/assets/cf333c6c-86ec-445d-a745-15ebf262f134)
![image](https://github.com/user-attachments/assets/d0e2d60a-27ab-492e-b7c5-a70f9ef4e12a)

### Calculate the lengths of embeddings and frames and then calculate the similarity for each embedding in the DataFrame.

![image](https://github.com/user-attachments/assets/fbe4bff6-0f5a-44c2-9c22-ac671e881054)
![image](https://github.com/user-attachments/assets/b6284c5a-51cf-4b44-8071-c150c5e5dff8)
![image](https://github.com/user-attachments/assets/8fa93d5f-09d6-4f52-aa9e-ea84c52ece4b)

### Turn text query into a simpler numerical form == Encode query string into a vector representation.

![image](https://github.com/user-attachments/assets/93ae7e93-0b3a-4fbd-b7b6-ffa7438e862d)

### I decided on my query which was "singlestore."

![image](https://github.com/user-attachments/assets/3737d850-6283-4408-afa8-e10f09fc2854)

### Find the top 5 matches and show the frames.
![image](https://github.com/user-attachments/assets/69b50a4b-bda5-4e9a-8609-5986357e3b8a)
![image](https://github.com/user-attachments/assets/b5771b97-8d0a-40dd-8538-0484ef4fcfe6)
![image](https://github.com/user-attachments/assets/2e6e8e12-655d-40a7-aa2d-c5f5d2809653)

### Present an example image.
![image](https://github.com/user-attachments/assets/eb9e8a3c-d58d-4bfe-8443-8ee507ffe51b)
![image](https://github.com/user-attachments/assets/d0be138c-8468-472a-9367-ca41bf9996f8)
![image](https://github.com/user-attachments/assets/c83eb7e1-1abc-4518-abd7-b4048cd8de3c)

### Find the Top 5 Best Matches.
![image](https://github.com/user-attachments/assets/065c802c-bf86-48da-b090-d3ad3e9e8c60)

### Show the frames and use CLIP with text and image in the query == balance them by element-wise averaging.
![image](https://github.com/user-attachments/assets/3361515f-f40f-44c5-adaf-61286217d732)
![image](https://github.com/user-attachments/assets/9c52edbe-b890-479e-bce8-09aa2e65d49f)

### Again find the Top 5 Best Matches and show the frames.
![image](https://github.com/user-attachments/assets/e55a148f-3393-41ef-af03-fc5fc700515e)
![image](https://github.com/user-attachments/assets/6349b885-c704-46b1-9640-5fbe2e325ba3)

Check the notebook in the repository for singlestore database operation.

