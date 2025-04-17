# During the Workshop

Before starting make sure you have addressed the prerequisites in the [README.md](README.md)

## Part 1 OAuth

This part of the workshop is in covered in [Part 1](./part_1.md).

## Part 2 Threat Modelling

In the second part of today's workshop you will be conducting a security review of an organisation's IT systems. [The details of this system can be found here](./Scenarios/Alpha_Organisation/description.md). Threat modelling can be an open ended process, so your trainers will probably time box each section of the exercise.

### Identify Threats

The first thing we need to do is to try to identify the possible threats the system could face. This is not an easy task: there are lots of possible attack vectors and many different sorts of threats.

Use the **STRIDE** topics as guidance and work your way through the systems methodically, perhaps system by system. At the end of this process you should have a list of potential threats grouped by topic and system. (You will probably find it helpful to record these in a spreadsheet of some sort. Feel free to structure it your own way, or use something like:

| System        | Risk Description | Risk Category (STRIDE) | Risk Likelihood | Impact Rating | Mitigation? |
| ------------- | ---------------- | ---------------------- | --------------- | ------------- | ----------- |
| Apollo        | ...              | ...                    | Low             | Low           | ...         |

#### STRIDE

A reminder from the reading material.

- **Spoofing** - impersonating another user or application
- **Tampering** - modifying input to execute an attack (e.g. the injection attacks from previous chapters)
- **Repudiation** - performing an action that cannot definitively be traced to the attacker
- **Information disclosure** - leak of sensitive data, a data breach
- **Denial of service** - rendering the application unavailable
- **Elevation of privilege** - gaining access to resources that would otherwise be protected

### Assessing Likelihood and Severity

Once you have assembled your list of potential threats it is time to assess how risky they are. For each threat you should estimate its **likelihood**, the chance of it happening; and its **severity**, how bad it would be. There are many ways to do this, perhaps the simplest is to assign one of three categories for each axis, e.g. low, medium, or high. Once done you will be able to combine likelihood and severity to determine which threats you should prioritise.

Suggested prioritisation matrix:

|                   | Low Impact | Medium Impact | High Impact |
| ----------------- | ---------- | ------------- | ----------- |
| Low Likelihood    | LOW        | LOW           | MEDIUM      |
| Medium Likelihood | LOW        | MEDIUM        | HIGH        |
| High Likelihood   | MEDIUM     | HIGH          | HIGH        |

### Mitigating Risks

Finally, work through the prioritised list of threats and suggest ways to mitigate those risks. These don't have to be technical solutions; it can be cheaper **and** more effective to put a non-technical control in place instead.

## Part 3 Vulnerable Docker Box

The [Damn Vulnerable Web Application](https://github.com/digininja/DVWA) will let you see some concrete examples of exploits. It is a deliberately vulnerable web application to let you safely and _legally_ explore breaking into a system.

### Quick Start Instructions

You can start the application by either: 
* Running `docker compose up` from the `dvwa` folder 
or 
* Cloning [the GitHub repository](https://github.com/digininja/DVWA) and following the instructions for running the application with Docker [here](https://github.com/digininja/DVWA#getting-started)

Once running:
1. Visit `localhost:4280` in a browser (if you see an error message you may need to wait 30 seconds and then refresh the page)
1. Enter the username and password (`Username: admin` and `Password: password`)
1. Click to `Create / Reset database` at the bottom of the homepage
1. Reauthenticate with the same username and password
1. Select the DVWA Security tab and change the security level from `impossible` to `low` and you're good to go!

On each vulnerability page there are buttons on the bottom right hand side that provide hints and display the code running on the server.

## Part 4 XSS Training (Optional)

XSS bugs are extremely common. Google have developed a game that helps demonstrate how some of these work.

You can find the game [here](https://xss-game.appspot.com/) and work through it.
