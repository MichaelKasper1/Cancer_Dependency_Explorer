# Django Web Server for Gene Dependency Prediction

This is a web implementation of DeepDEP algorithms. The goal of this project is to foster access to onocology researchers so they can predict the gene dependencies of a tumor or cancer cell line in one sample or a cohort of samples.

### Deployment

This app is containerized in a docker image. The easiest deploy the app, you will need to have docker installed within your environment. You can download docker [here](https://www.docker.com/products/docker-desktop). You can also easily deploy the app on the CRC. To build and run the docker image, you can use the following commands within a bash terminal:

```bash
docker build -t myapp .
docker run -p 8000:8000 myapp
```

This will start the app and make it accessible at http://localhost:8000.

### Development

I recommend using Visual Studio code for development. You can download it [here](https://code.visualstudio.com/). You will also need to have python installed.

Below are links to useful tutorials:
- [Django Tutorial from VSCode Documentation](https://code.visualstudio.com/docs/python/tutorial-django) Django is the backend of the application. It performs the data processing and interacts with the SQL database. This tutorial gives you Django basics and you can learn about the directory structure and important files.
- [Vue] (https://vuejs.org/) Vue is the javascript framework for the web server. It is the front end of the application that allows users to interact with the application. Follow various tutorials here. They have different ones for different learning styles.
- [Using Docker and Python in VScode](https://learn.microsoft.com/en-us/visualstudio/docker/tutorials/docker-tutorial) This tutorial helps you understand how and why to use Docker for containerization.
- [Understanding Debugging Using Breakpoints](https://code.visualstudio.com/docs/python/debugging) This tutorial helps you understand breakpoints and using VS code debugger to understand issues with the app and data flow.
- [Make] (https://makefiletutorial.com/) Tutorial for understanding Make and how makefile helps to build app. There are also official tutorials on their website but I liked this one.

Below are extensions I used for development:
- [Copilot](https://code.visualstudio.com/docs/copilot/overview) Copilot is an AI pair programmer that helps you write code faster and understand others code more easily. It's a LLM that watches you code and recommends code.
- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) This extension provides Python language support and debugging capabilities.
- [Django](https://marketplace.visualstudio.com/items?itemName=batisteo.vscode-django) This extension provides rich language support for the Django framework.
- [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) This extension makes it easy to build, manage, and deploy containerized applications from Visual Studio Code.
- [Remote Explorer](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) Let's you connect to Pitt CRC
- [Vue](https://marketplace.visualstudio.com/items?itemName=Vue.volar) This extension provides support for view framework

Once you have at least a basic understanding of these, time to start developing! I recommend creating an environment within the main "Gene_Dependency_Web_Server" directory named .venv. You can do so like this

    ```bash
    brew install python@3.8
    python3.8 -m venv .venv
    source .venv/bin/activate
    ```

Install make to easily install all app dependencies and start your development servers:

    ```bash
    brew install make
    ```

Use a make command to run various commands necessary to build and to run the app:

    ```bash
    make install
    ```

Use a make command to concurrently 

    ```bash
    make start
    ```

Follow the directions in your terminal to open in your browser once the server is started:
http://127.0.0.1:8000/