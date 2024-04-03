# Homework 4: Prompting via Crowdsourcing Strategies**

In this assignment, you will apply decades of research findings in Crowdsourcing instructions to LLM prompting. Hopefully the assignment will help you:

* Get familiar with the concept of prompting.
* Get familiar with the Gemini interface.
* Get familiar with crowdsourcing techniques & limitations.
* Explore the feasibility of using LLMs as crowdworkers -- If the results are interesting, we might use them to compile a research paper with everyone in the class listed as a coauthor!

## Homework overview

**Background**: If you think of each large language model call as a crowdworker completing a small task, then naturally we can ask: can multiple LLM modules collectively solve a larger task, if each of them completes a microtask?
This is the basic idea behind multiple research papers like [AI Chains](https://arxiv.org/pdf/2110.01691.pdf) (CHI 2022), [least-to-most prompting](https://arxiv.org/pdf/2205.10625.pdf) (2022), etc.
**I highly recommend reading the [AI Chains](https://arxiv.org/pdf/2110.01691.pdf) paper, especially the Introduction, Sec 2.3 (gives you an overview of Crowdsouring workflow vs. LLM workflow), and Sec 3.1 (why LLMs can be used in workflows).**

This framing opens up additional possible explorations of LLM usage. Researchers have explored microtasking/building workflow and pipelines for crowdsourcing tasks for decades, and so we can see if their design pipelines can also be applied to LLMs.

In this homework, you will:

1. read a crowdsourcing paper in detail,
2. replicate its pipeline by writing multiple prompts that would instruct different LLM modules to complete different subtasks,
3. test the pipeline on some tasks and inputs you selected, and
4. write a reflection on why the pipeline worked or did not work.


## Steps for completing the homework.

### 1. Pick a Crowdsoucring paper to focus on.

Pick from one of the six crowdsourcing papers to read in detail. You will replicate its baseline when you do prompting in the notebook (see next section).

- **Please [use this Google Sheet](https://docs.google.com/spreadsheets/d/1qM66oZ5YcSjqifegoyNgl3LFMaCfFHgoPe8isgckbXA/edit?usp=sharing) signup for the paper you are replicating**. Each paper can be signed up by up to four people, first come first serve.
- If none of these six look interesting to you, you can also pick your own paper. In that case, please email Sherry the paper link so I can approve it.


### 2. Set up the environment and code.

   **Environment setup:** Similar to previous homeworks, set up a virtual Python environment to ensure consistent package versions. Here's an example using Conda:

   ```bash
   # create an environment named eval_env, under the version of python 3.7
   conda create --name prompt_env python=3.7
   # start the environment.
   conda activate prompt_env
   ```

   **Install necessary packages:**

   ```bash 
   conda activate prompt_env 
   pip install -U google-generativeai
   ```

   **Start the programming environment**

   ```bash
   conda activate prompt_env
   git clone $GIT_REPO_URL 
   cd $PATH_TO_YOUR_LOCAL_REPO 
   jupyter notebook 
   ```


   **Familiarize yourself with Gemini:** Read the tutorial doc and explore the examples to understand how to use the Gemini API.  

3. **Start to complete the task in the notebook.** 
   Visit http://localhost:8888/notebooks/HAII-HW4-Notebook.ipynb to access your notebook. We provide a sample solution (in HAII-HW4-Notebook-Sample.ipynb) to help you better understand the steps involved.

**Delivery**

* Complete all steps in the notebook.
* Download the notebook as HTML (File => Download As => HTML in Jupyter Notebook).
* Rename the downloaded HTML  HAII-HW4-Notebook.html to  HAII-HW4-Notebook-[AndrewID].html (e.g.  HAII-HW4-Notebook-janedoe.html)
* Submit HAII-HW4-Notebook-[AndrewID].html on Canvas.

**Grading**

If you find the assignment difficult, there are some ways to earn partial credits, as shown below.

- **0 point** if no submission.
- **40 points if you only describe your task and strategies without actual prompting**. You will only need to fill in the writeup sessions in the notebook. For the result part, you should write how you _envision_ the model to perform.
- **70 points if you modified the pipeline in the Sample notebook** -- i.e., if you created a different task (that's not metaphor creation, and has different inputs and outptus), and showed that a pipeline similar to the Sample pipeline also works for your new task.
- **80 points if you wrote a pipeline that's applicable to 1 input** (i.e., you made it work for a particular input).
- **100 points if you wrote a pipeline that's applicable to 2 inputs** (i.e., you showed some generalizability).


**Questions?**

Please post your questions on Slack channel.
