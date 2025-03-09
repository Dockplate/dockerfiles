## Contributing

### Adding Dockerfile for a new langauge

#### Naming and directory schema

![directory-schema](https://i.imgur.com/bykj2FC.png)

Files should be arranged in the above fashion. Every language must contain:

- Source code
- Dockerfile
- Readme file

The naming of the folders shouldn't be abbreviated from like (javascript to js). 
Always use lowercase for file names. Hypens should be used in between files and folder names instead of space.

#### Source Code

The source code of the specific programming language should be kept as simple as possible like a basic Hello World program so as to just show the program works inside Docker.Never ask input from user and don't print unesserary lines or extra statements.

#### Dockerfile

The docker file must be prepared in such a fashion that it doesn't use any unofficial docker images. Try to stick with alpine or ubuntu as the base image as often as possible.

#### Readme

The Readme file should contain brief information on how to build and run the Dockerfile.