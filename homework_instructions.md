---
layout: home
title: HW Instructions
nav_order: 4
---

# Homework Instructions

---

## One-Time Setup

### ASAP: Complete Course Registration Form

If you have not done so already, [complete the course registration form](https://docs.google.com/forms/d/e/1FAIpQLScFXiWyp5Rf2jW-e-CuX51656R7vvsjSRX6O5Tp805Pq-viIw/viewform?usp=sharing). You will need to complete this form and wait up to 24 hours to get access to homework code.

### Enroll in Gradescope

Use the access code **WJJPZ8** to enroll in [the Gradescope course](https://www.gradescope.com/courses/1025616). See [here](https://guides.gradescope.com/hc/en-us/articles/21853290544909-Joining-a-Course) for detailed instructions.

### Fork the Course Code

After you get access to [the course code](https://github.com/rpmml/rpmml-code), you should [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) it. You will write and submit homework code through your fork.

![GitHub fork illustration](/assets/images/github-fork-illustration.png)

### Clone Your Fork

Follow the [instructions on GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) to clone your forked repository. Make sure that you clone your fork and not the original ("upstream") repository.

### Set Upstream

While in your cloned repository:

```bash
git remote add upstream git@github.com:rpmml/rpmml-code.git
git fetch upstream
```

This will allow you to pull in future updates to the course code.

### Install the Code

We require that you use a virtual environment when working with course code to avoid unintended interactions with other code on your machine. Specifically, we require you to use <a href="https://github.com/astral-sh/uv">uv</a>. Follow the instructions to install uv if you do not already have it. Then, while in your cloned repository:

**Note: Make sure that you fully deactivate any conda environments before running these steps.**

```bash
uv venv --python=3.10
source .venv/bin/activate
uv pip install -e ".[develop]"
```

To test the installation:

```bash
./run_ci_checks.sh
```

## Working on Problem Sets

### Download the PDF
Problem set PDFs are posted on the <a href="/calendar">course calendar</a>.

### Complete Written Exercises
LaTeX is preferred, but immaculately hand-written answers are also allowed.

### Complete Coding Exercises
1. Activate your virtual environment if not already done: `source .venv/bin/activate`
2. Pull upstream changes: `git pull upstream main`
3. Complete the missing code in `assignments/homework<X>`
4. Test your answers using pytest: `pytest assignments/homework<X>`
5. Save and commit your code (throughout working on the assignment):
```
git add -u
git commit -m "<some message>"
git push origin HEAD
```

## Submitting Problem Sets

You will submit both written and coding exercises through Gradescope. There will be two separate submissions for written answers and for code. The code will be autograded and in most cases will not be manually reviewed by instructors. (Note that there are automated plagarism checks.) You can resubmit as many times as you want.

### Submitting Written Answers

Submit your written answers in one PDF on GradeScope.

### Submitting Code

Submit your code on Gradescope using the Github plugin, as shown below.

![GitHub Gradescope illustration](/assets/images/github-gradescope.png)

The autograder should simply run the tests that you have locally. There are no additional hidden tests. If there is a discrepancy between the local tests and Gradescope, that either means that your code is nondeterministic, or our code has an issue. Consider the first possibility and then reach out if you continue to see a discrepancy.


## Troubleshooting

If you run into any technical trouble, please don't hesitate to contact course staff.
