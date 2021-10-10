# SAP NetWeaver AS ABAP Missing Configuration Security Demo Tool

## Description
Profile parameters are a set of specific parameters that are responsible for the configuration of the system. <br>
There are more than a thousand parameter profiles in the SAP system. Some of them are critical and are responsible for configuring system security (password policy, SAP Gateway configuration, logging configuration). <br>
This application was created to analyze the settings of the SAP system profile parameters and detect incorrect configurations.

## System and User requirement

### System
This demo tool was created to check the incorrect configuration of the sap abap systems. <br>
The application works through the SAP Gateway port (33NN) using SAP JCO RFC requests.<br>
To run the aplication you must install Java 17 on your system. <br>
**The demo tool working without internet and doesn't transfer any data to the public.**
```
java -jar profileparameters-cli --help
Usage: <main class> [--client=<client>] [--host=<host>] [--lang=<lang>]
                    [--out=<outputFile>] [--password=<password>] [--sys=<sys>]
                    [--user=<user>]
      --client=<client>
      --host=<host>
      --lang=<lang>
      --out, --output, --outputFile=<outputFile>

      --password=<password>

      --sys=<sys>
      --user=<user>
```

### User
For running the demo tool, you need to pass an authorization by existing credentials in your system. <br>
Of course, there is no need to use SAP* privilege user for the test. However, the user (e.g., RRUSER) should have **S_RZL_ADM** and **S_RFC** authorization objects for better results.
<br>
![image](https://user-images.githubusercontent.com/7976421/136682452-65bd215c-698b-4618-b464-21c4e4e33fca.png)

## Report
After the demo tool successful  execution 
```
java -jar profileparameters-cli --out="Report.xlsx" --host="IP" --user="RRUSER" --password="PASSWORD#" --client 001
```
![image](https://user-images.githubusercontent.com/7976421/136682383-5068a682-896e-4839-8d26-6b16b6e291bc.png)
<br>You can find the report as an EXCEL file
![image](https://user-images.githubusercontent.com/7976421/136681105-be52c482-4033-4283-8dee-6ebeb09bee94.png)


## Download
To download the SAP Profile Parameters CLI Demo Tool please contact us by the following form https://redrays.io/request-profile-parameters-cli-demo/ 
