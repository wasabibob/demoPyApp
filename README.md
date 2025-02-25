<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>

<br />
<div align="center">
<h3 align="center">Demo Python App</h3>

  <p align="center">
    This is a example demo project to build and test a docker image.
    <br />
  </p>
</div>

### Built With

* [Python](https://www.python.org)
* [Flask](https://flask.palletsprojects.com/en/stable/)
* [pytestt](https://docs.pytest.org/en/stable/)
* [docker](https://docs.docker.com/get-started/)
* [GitHub Actions](https://github.com/features/actions)

<!-- GETTING STARTED -->
## Getting Started

It's pretty simple, you fork the [repository](https://github.com/wasabibob/demo-py-app). then build, test and publish

### Prerequisites

Install Python3 [installation package](https://www.python.org/downloads/) 

Install [docker](https://docs.docker.com/get-started/)


## Build

1.  Clone the repo
   ```sh
   git clone git@github.com:wasabibob/demo-py-app
   ```
2. Run docker build
   ```sh
   cd demo-py-app
   docker build .
   ```
3. Make note of the image **sha or image** id from the output of your build\
    eg. sha256:6dcb511f99a9e755e8c27b833739f38180ab79e329860fa0432c25ba0ca9be25
   
## Run

Run the built image in docker on in your local environment from the terminal window or from docker desktop application\
Once running, you can see the app by opening a browser and browsing to **localhost:5500**

### In a terminal

From the application source home directory (demo-py-app)
```sh
   docker run -it -p 5500:5000 <Image ID>
   ```
### From docker desktop

1. Navigate to images tab and locate your most recent build (typicaly at the bottom of the list)
2. Click on the play/run button under the Actions column
3. In the **Run a new container** diaglog box, under **Optional setting**, replace **Host port** with the value **5500**
4. Click **Run**


## Test
1. Tests are functions defined in the tests.py file
2. These will automatically run as part of the **GitHub Actions Workflow** which is found in the .github/workflows folder
3. To run the workflow, simply commit a change to your GitHub repsoitory, this will start the GitHub Actions Workflow
4. In your browser, navigate to your GitHub repository and slect the **Actions** tab
5. Click on the most recent workflow (named after your recent commit)
6. In the **docker-image.yaml** workflow select the **docker** run to see the test results as part of the workflow output


<p align="right">(<a href="#readme-top">back to top</a>)</p>

