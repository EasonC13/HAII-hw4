**Assignment 2: Prompting via Crowdsourcing Strategies**

In this assignment, you will apply decades of research findings in Crowdsourcing instructions to LLM prompting. Hopefully the assignment will help you:

* Get familiar with the concept of prompting.
* Get familiar with the Gemini interface.
* Get familiar with crowdsourcing techniques & limitations.
* Explore the feasibility of using LLMs as crowdworkers -- If the results are interesting, we might use them to compile a research paper with everyone in the class listed as a coauthor!

**Assignment overview**

**Background:** If you think of each large language model call as a crowdworker completing a small task, then naturally we can ask: can multiple LLM modules collectively solve a larger task, if each of them completes a microtask? This is the basic idea behind multiple research papers like AI Chains (CHI 2022), least-to-most prompting (2022), etc. I highly recommend reading the AI Chains paper, especially the Introduction, Sec 2.3 (gives you an overview of Crowdsouring workflow vs. LLM workflow), and Sec 3.1 (why LLMs can be used in workflows).

This framing opens up additional possible explorations of LLM usage. Researchers have explored microtasking/building workflow and pipelines for crowdsourcing tasks for decades, and so we can investigate if their design pipelines can also be applied to LLMs.

**In this assignment, you will:**

* Read a crowdsourcing paper in detail.
* Replicate its pipeline by writing multiple prompts that would instruct different LLM modules to complete different subtasks.
* Test the pipeline on some tasks and inputs you selected.
* Write a reflection on why the pipeline worked or did not work.

**Steps for completing the assignment:**

1. **Pick a Crowdsourcing paper to focus on.**
   Pick from one of the six crowdsourcing papers to read in detail. You will replicate its baseline when you do prompting in the notebook (see next section).

   Please use this Google Sheet signup for the paper you are replicating. Each paper can be signed up by up to four people, first come first serve.

   If none of these six look interesting to you, you can also pick your own paper. In that case, please email Sherry the paper link so I can approve it.

2. **Set up the environment and code.**

   **Environment setup:** Similar to Assignment 1, set up a virtual Python environment to ensure consistent package versions. Here's an example using Conda:

   ```bash
   # create an environment named eval_env, under the version of python 3.7
   conda create --name prompt_env python=3.7
   # start the environment.
   conda activate prompt_env
   ```

   **Install necessary packages:**

   ```bash 
   conda activate prompt_env 
   pip install gemini-python notebook 
   ```

   **Start the programming environment**

   ```bash
   conda activate prompt_env
   git clone $GIT_REPO_URL 
   cd $PATH_TO_YOUR_LOCAL_REPO 
   jupyter notebook 
   ```

   **Obtain your Gemini API Key:**  
   * Follow instructions on the Gemini documentation to obtain your API key.
   * Create a json file `credential.json` in the repo folder, and put the following information there:

   ```json
   {
     "gemini": "[INPUT YOUR APIKEY HERE]"
   }
   ```

   **Familiarize yourself with Gemini:** Read the tutorial doc and explore the examples to understand how to use the Gemini API.  

   **Important:** Use the appropriate Gemini model for your task (read the model descriptions carefully).

3. **Start to complete the task in the notebook.** 
   Visit http://localhost:8888/notebooks/A2-Notebook.ipynb to access your notebook. We provide a toy example solution to help you better understand the steps involved.

**Delivery**

* Complete all steps in the notebook.
* Download the notebook as HTML (File => Download As => HTML in Jupyter Notebook).
* Rename the downloaded HTML A2-Notebook.html to A2-Notebook-[AndrewID].html (e.g. A2-Notebook-janedoe.html)
* Submit A2-Notebook-[AndrewID].html on Canvas.

**Grading**

If you find the assignment difficult, there are some ways to earn partial credits, as shown below.

The base grade will be up to 80, based on how you attempted the task:

- **0 point** if no submission.
- **30 points if you only describe your task and strategies without actual prompting**. You will only need to fill in the writeup sessions in the notebook. For the result part, you should write how you _envision_ the model to perform.
- **60 points if you modified the pipeline in the Sample notebook** -- i.e., if you created a different task (that's not metaphor creation, and has different inputs and outptus), and showed that a pipeline similar to the Sample pipeline also works for your new task.
- **70 points if you wrote a pipeline that's applicable to 1 input** (i.e., you made it work for a particular input).
- **80 points if you wrote a pipeline that's applicable to 3 inputs** (i.e., you showed some generalizability).

**The remaining 20 point will be based on peer review results:**:

- Three students will read your notebook and rate your prompting effort on a 1-5 scale. This rating will be about whether you've put in enough effort replicating and improving the selected crowdsourcing pipeline for LLM prompting (and, relatedly, how thoughtful was your writeup), not on the final prompt efficiency.
- Your score depends on the relative ranking of averaged your test score usefulness. you wil get {20, 15, 10, 5} scores if your averaged score is ranked top {25%, 50%, 75%, 100%} percent respectively.

**Questions?**

Please post your questions on Slack channel.
