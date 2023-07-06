<div align="center">

# ◐ &nbsp; GPT Migrate &nbsp; ◑

**This project is only used as a challenge and is not maintained**
It was copied from [here](https://github.com/0xpayne/gpt-migrate)

<br />

</div>


## ⚡️ Usage

1. Install Docker and ensure that it's running. It's also recommended that you use at least GPT-4, preferably GPT-4-32k.

2. Set your [OpenAI API key](https://platform.openai.com/account/api-keys) and install the python requirements:

`export OPENAI_API_KEY=<your key>`

`pip install -r requirements.txt`

3. Run the main script with the target language you want to migrate to:

`python main.py --targetlang nodejs`

4. (Optional) If you'd like GPT-Migrate to validate the unit tests it creates against your app before it tests the migrated app with them, please have your existing app exposed and use the `--sourceport` flag. For executing this against the benchmark, open a separate terminal, navigate to the `benchmarks/language-pair/source` directory, and run `python app.py` after installing the requirements. It will expose on port 5000. Use this with the `--sourceport` flag.

By default, this script will execute the flask-nodejs benchmark. You can specify the language, source directory, and many other things using the options guide below.

## 📈 Performance

GPT-Migrate is currently in development alpha and is not yet ready for production use. For instance, on the relatively simple benchmarks, it gets through "easy" languages like python or javascript without a hitch ~50% of the time, and cannot get through more complex languages like C++ or Rust without some human assistance.

## ✅ Benchmarks

We're actively looking to build up a robust benchmark repository. If you have a codebase that you'd like to contribute, please open a PR! The current benchmarks were built from scratch: REST API apps which have a few endpoints and dependency files.

## 🧗 Roadmap

Below are improvements on the to-do list. If you'd like to knock any of these or others out, please submit a PR :)

#### High urgency
- Add logic for model input size limiting based on the window size. See issue [#2](https://github.com/0xpayne/gpt-migrate/issues/2).

#### Med urgency
- Add unit tests to the entire project for better reliability and CI/CD
- Add more benchmark examples, especially larger repos
- Add functionality to let the LLM request access to dependency functions in other files as it debugs
- Add support for other LLMs

#### Low urgency
- Enable internet search requests as the model debugs
- Identify and compile language-specific issues + solve for them

## 📣 Call to Action

We're looking for talented contributors. Whether you have a particular passion about a specific language or framework, want to help in creating a more robust test suite, or generally have interesting ideas on how to make this better, we'd love to have you!
