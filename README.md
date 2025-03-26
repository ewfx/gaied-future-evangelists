# 🚀 Gen AI-Based Email Classification and OCR

## 📌 Table of Contents
- [Introduction](#introduction)
- [Demo](#demo)
- [Inspiration](#inspiration)
- [What It Does](#what-it-does)
- [How We Built It](#how-we-built-it)
- [Challenges We Faced](#challenges-we-faced)
- [How to Run](#how-to-run)
- [Tech Stack](#tech-stack)
- [Team](#team)

---

## 🎯 Introduction
The purpose of the project is to automate the Gatekeeper tasks of browsing throught the email (with and without attachment) and trying to identify the request type and subtype from the email or its attachment content. With the help of this classification and extraction of key terms from the email, the team would be able to riase Service requests easily and would try to process them in the work flow.
## 🎥 Demo
🔗 [Live Demo](#) (if applicable)  
📹 [Video Demo](#) (if applicable)  
🖼️ Screenshots:
![image](https://github.com/user-attachments/assets/9752a257-1508-4c0a-8f4f-6e6a205a55bb)

![image](https://github.com/user-attachments/assets/c8c4fc85-d375-4232-b3d4-5434aca92110)

![image](https://github.com/user-attachments/assets/6273864e-9645-42ec-b3dc-510c16bf5ae6)


## 💡 Inspiration
What inspired you to create this project? Describe the problem you're solving.
I have lots of scripting expereince and cloud experience working on google cloud. I have participated in Hackathon few years back, i like participating in code challenges. 
In this problem, we are expecting an input that is email, it can be in the form of eml file or a document or a pdf file or a simple text. 
We need to identify the type of file input we got and process it accordingly. Also if we get a eml file, and it has attachments we should be able to read that content as well and provide an option to user to combine the content recieved from mail and attachment and then on the top of it do analysis. After doing the analysis then we need to claissfy the mail, identify the following keys
Request Type, Request Sub Type, Reasoning, Amount feilds, Sender, Reciever, etc.

## ⚙️ What It Does
Explain the key features and functionalities of your project.
This project is using model from google cloud Gemini model(gemini-1.5-pro-002). So it authenticates us using google cloud api key.  I have used module to read pdf files and emails and docs. Once the reading is complete, i have created prompts that will provide inputs on what request types and subtypes are expected and what output to provide as mentioned below:

Classify the following email into one of the request types:
[Adjustment, AU Transfer, Closing Notice, Commitment Change, Fee Payment, Money Movement-Inbound, Money Movement - Outbound, Urgent, Acknowledgement].
and Request subtypes:
[Reallocation Fees,Amendement Fees,Reallocation Principal,Cashless Roll,Decrease,Increase,Ongoing Fee,Letter of Credit Fee, Principal,Interest, 
Principal + interest, Principal+interest+fee,Timebound, foreign currency]"""
        tailer_content = """"         
Return the following:
- Request Type:
- Request Subtype:
- Sender:
- Receiver(To):
- Date:
- Amount:
- Currency:
- Reasoning:

## 🛠️ How We Built It
Technologies used are python, google generative ai module, and few python modules like docx, pyPDF2, extract_msg and email.
## 🚧 Challenges We Faced
Describe the major technical or non-technical challenges your team encountered.
We have faced challenge in enabling the model and usign the model. Then we have faced issues in reading pdf files and docx files directly. It was throwing error like binary data provided. Then we have used pyPDF2 and docx modules.

## 🏃 How to Run
1. Clone the repository  
   ```sh
   git clone https://github.com/ewfx/gaied-future-evangelists.git
   ```
2. Install dependencies  
   ```sh
   pip install gcloud
   pip install pyPDF2
   pip install docx
   pip install python-docx PyPDF2 extract-msg
   pip install google-generativeai torch
   
   ```
3. Run the project  
   ```sh
   python GenAI_Email_Classify_and_OCR.py
   ```

## 🏗️ Tech Stack
- 🔹 python
- 🔹 Other: OpenAI API / Twilio / Stripe

## 👥 Team
- **Your Name** - raj2610-andriod  | https://www.linkedin.com/in/venkata-evani-6b8988156/
- **Teammate 2** - choppas
- **Teamate 3** - devaralaak
