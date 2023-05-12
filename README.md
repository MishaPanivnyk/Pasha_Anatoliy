# image_storage_service
This code sets up an image storage service using Node.js, Express, and MongoDB. It uses Multer to handle file uploads and uuid to generate unique filenames for the uploaded images. The uploaded images are stored in a directory called "image_uploads/images/", which is created if it does not exist. The service listens on port 3000, or on the environment variable PORT if it is defined.

The code sets up two endpoints: "/upload" for uploading images and "/image/:id" for deleting images. When a file is uploaded, its name is changed to a unique UUID and saved in the "image_uploads/images/" directory. The URL of the uploaded image is then saved in the MongoDB database. When an image is deleted, its file is removed from the directory and its entry is deleted from the database.

To run the code, the user must install the required dependencies: Express, Mongoose, Multer, and uuid. Additionally, the user must set up a MongoDB database and provide the connection string in the code. Once this is done, the user can run the program with the command "node app.js".
