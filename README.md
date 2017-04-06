# comp2068-presentation-final

        Introduction

         # 1. What is file upload
          - File upload is the transmission of a file from local computer to server computer.
          - File upload takes place using FTP, HTTP, HTTPS, SOAP, and etc protocols.
          - In http protocol, we need to use multipart uploading, we will use "multer" npm module.

        # 2. How to upload file
          - First, save binary file into database directly.
          - Second, save file into server computer and save the link in database
          - Third, save binary file into commercial other server site and save the link in database.

          - We will use second way to upload file.

       # 3. fileupload

        File upload method is basically used to uplaod files which returns 4 functions:

        1.   middleware - route middleware
        2.   get - to retrieve uploaded files
        3.   put - to add files to the upload directory
        4.   delete - to remove uploaded files

         # 4. commands used to install file upload npm package

         npm install fileupload


        # 5. How to use file upload get ,put and delete methods

        #  a. get() method to retrieve the data/file from the upload directory


       var fileupload = require('fileupload').createFileUpload('/uploadDir')

        fileupload.get('path-to-uploaded-file.gif', function(error, data) {
        // file has content that is data
        })

        # b. put() it puts the file into the upload directory


      var fileupload = require('fileupload').createFileUpload('/uploadDir')

      fileupload.put('path-to-file.gif', function(error, file) {
        // file is the object folder which consists information about the uploaded file
      })
