# Adjusting Your Path on Windows<a name="serverless-sam-cli-install-windows-path"></a>

This section describes how you can adjust your path\. You have to do this as part of installing the AWS SAM CLI by using pip, as described in [Installing Using Pip](serverless-sam-cli-install-additional.md#serverless-sam-cli-install-using-pip)\.

On Windows systems, the command `py -m site --user-site` typically prints `%APPDATA%\Roaming\Python<VERSION>\site-packages`, so you need to remove the last `\site-packages` folder, and replace it with the `\Scripts` folder\.

```
$ python -m site --user-base
```

Using File Explorer, go to the folder that's indicated in the output, and look for the `Scripts` folder\. Visually confirm that the `sam` application is inside this folder\.

Copy the file path\.

**Note**  
As explained in the [ Python Developer's Guide](https://www.python.org/dev/peps/pep-0370/#specification), the user's home directory \(where the scripts are installed\) is `%APPDATA%\Python\Scripts` for Windows\.

Search Windows for `Edit the system environment variables`\.

Choose **Environment Variables**\.

Under **System Variables**, choose **Path**\.

Choose **New**, and enter the file path to the Python Scripts folder\.