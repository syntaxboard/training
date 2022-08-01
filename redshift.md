python / API
JBDC to Redshift
1. From "S3/folder" Read all file.metadata_cols,file.business_Data_cols from s3Bucket into spectrum.stg_s3_table
2. python build collection from [file.metadata_cols from spectrum.stg_s3_table]
3. insert into redshift app.table select file.business_Data_cols from spectrum.stg_s3_table;
4. validate and report status to cloudwatch, and archive this* set of processed files processed folder.
