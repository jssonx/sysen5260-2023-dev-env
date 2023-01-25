# Troubleshooting in SYSEN 5260
SYSEN 5260: Software Systems Engineering

## dev-env

### Problem: Incorrect Line Endings

When running the command ```docker-compose run hello-dev-env```, the terminal returns an error ```: not found.sh: line 2:```. This is likely due to the difference in line endings between Windows and Unix/Linux systems. Windows uses "CRLF" (Carriage Return + Line Feed) as its line ending, while Unix/Linux uses "LF" (Line Feed) as its line ending.

#### Solution 1:

Try running the command ```dos2unix hello-world.sh```. This will convert the line endings from Windows format to Unix format, stripping the "CR" (Carriage Return) from the line endings and changing them from "CRLF" to "LF".

#### Solution 2:

In VSCode, go to the bottom right corner and change the line ending format from "CRLF" to "LF".

Note: Make sure to save the changes before running the command again.

### Problem: The docker daemon is not running

When running the command ```docker-compose run hello-dev-env```, the terminal returns an error ```error during connect: this error may indicate that the docker daemon is not running```.

#### Solution:

Ensure that the Docker Desktop program is running before executing the "docker-compose" command. This error occurs because the Docker daemon, which is responsible for managing and running containers, is not running when the command "docker-compose" is executed. In order for "docker-compose" to function properly, the Docker daemon must be running in the background.