# AMI Packer
Packer is a tool for building identical machine images for multiple platforms from a single source configuration.

# Installing Packer

##Prerequisites: 
   Install Packer on you machine. Follow this link to learn more about packer:
   https://learn.hashicorp.com/tutorials/packer/getting-started-install

## Instructions to Run:

1. Clone the repository

    ```sh
    $ git clone git@github.com:sutharp-fall2020-csye6225/ami.git
    ```

2. Validate the packer file using 'validate' command
    ```shell script
    $ packer validate ami.json
    ```

3. `ami.json` file tells Packer what platforms to build images for and how you want to build them. In our
    case, we'll create a simple AMI using `Ubuntu 18 LTS (AMI ID ami-0817d428a6fb68645)` as your source image that has Node pre-installed.

4. Export your AWS credentials as the `AWS_ACCESS_KEY`,`AWS_SECRET_KEY`, `AWS_REGION` and `SUBNET_ID` as environment variables.

5. Build the Image using Packer command 

    ```sh
    $ packer build ami.json
    ```

    Packer will build an AMI according to the `ami.json` template. The AMI will be available in your AWS account
