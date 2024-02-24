# Project: Automated Data Ingestion from AWS S3 to Snowflake using Snowpipe

## Overview:

This project aims to automate the process of ingesting data from an AWS S3 bucket into Snowflake using Snowpipe. By leveraging Snowpipe, data ingestion becomes a seamless, near real-time process, enabling timely insights for analytical purposes.

## Prerequisites:

1. **AWS IAM user account** with appropriate permissions to access the desired S3 bucket.
   - Create an IAM role and configure permissions. Refer to [[AWS documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)]
   - Create an S3 bucket to store the data.

2. **Snowflake account** with sufficient privileges to configure storage integrations, stages, and pipes.
   - Ensure access to create warehouses, databases, schemas, tables, and pipes.

## Steps:

1. **Set up AWS IAM Roles and Permissions:**
   - Create an IAM role with the necessary permissions to access the S3 bucket.
   - Configure policies to grant access to required S3 resources.

2. **Configure Snowflake Storage Integration:**
   - Create a storage integration in Snowflake to connect with the AWS IAM role.
   - Specify the IAM role ARN and the allowed S3 bucket locations.

3. **Create File Formats and Tables:**
   - Define file formats according to the types of files in the S3 bucket (e.g., CSV, JSON).
   - Create tables in Snowflake where data will be loaded.

4. **Set Up External Stage:**
   - Create an external stage in Snowflake to point to the specific folder in the S3 bucket.
   - Specify the path of the folder where data files will be uploaded.

5. **Develop Snowpipe for Automated Ingestion:**
   - Create a Snowpipe to automate the ingestion process.
   - Set `AUTO_INGEST` to true for automatic data loading.
   - Define the Snowpipe's behavior and specify the target table.

6. **Configure SQS Notifications:**
   - Set up SQS notifications in AWS to trigger Snowpipe upon new file uploads.
   - Specify the event type, folder prefix, and file suffix for the notifications.

7. **Testing and Verification:**
   - Upload sample data files to the S3 bucket to trigger Snowpipe.
   - Monitor the Snowpipe execution and verify data loading into Snowflake tables.

## Additional Resources:
- Snowflake Documentation: [https://docs.snowflake.com/en/user-guide/data-load-snowpipe-auto-s3]
- AWS IAM Documentation: [https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html]
- AWS S3 Documentation: [https://docs.aws.amazon.com/s3]

## Conclusion:

By following these steps, you can automate the data ingestion process from AWS S3 to Snowflake, enabling near real-time access to data for analytical purposes. This project empowers data-driven decision-making by ensuring a continuous flow of fresh data into Snowflake.

For any inquiries or assistance, feel free to reach out!

**Author:** Sai Varun Namburi


