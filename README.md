# Smart Budget Buddy - AWS Bedrock AI Agent

[![AWS](https://img.shields.io/badge/AWS-Bedrock-FF9900?style=flat&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/bedrock/)
[![AI Agent](https://img.shields.io/badge/AI-Agent-blue?style=flat)](https://aws.amazon.com/bedrock/agents/)


> An AWS Bedrock-powered AI chatbot designed to help high school students develop financial literacy skills through responsible AI practices.

## 📋 Project Overview

**Smart Budget Buddy** is an AI-powered financial literacy chatbot created as part of the **Future AWS AI Engineer Nanodegree** program. This project demonstrates hands-on experience with AWS Bedrock's Agent Builder and Guardrails to create a safe, ethical, and educational AI solution.

### Context

A local school launched a financial literacy initiative for graduating students to help them develop financial confidence as they transition to college, work, or gap years. The Smart Budget Buddy chatbot serves as an accessible learning tool that complements workshops and one-on-one sessions with financial experts.

### Objective

Build a responsible AWS Bedrock Agent that helps high school students:
- ✅ Create simple weekly or monthly budgets (e.g., 50/30/20 rule)
- ✅ Understand basic financial terms like "needs vs. wants" and "saving goals"
- ✅ Avoid common money traps (scams, impulse spending, debt)
- ✅ Make informed financial decisions without risky advice

---

## 🎯 Key Features

### Agent Capabilities
- **Budgeting Education**: Teaches students to create practical budgets with clear explanations
- **Financial Terminology**: Defines concepts like credit scores, savings goals, and debt management in accessible language
- **Safe Spending Tips**: Provides general guidance on avoiding scams and impulse purchases
- **Inclusive Communication**: Uses gender-neutral language and diverse examples

### Responsible AI Implementation
- **Guardrails**: Configured AWS Bedrock Guardrails to prevent harmful outputs
- **Prohibited Content Filtering**: Blocks inappropriate topics and profanity
- **No Financial Advice**: Strict boundaries preventing investment, stock, or product recommendations
- **PII Protection**: Sensitive information filters to protect student privacy
- **Crisis Fallback**: Directs students in distress to trusted adults (teachers, counselors)

---

## 🏭 Architecture & AWS Services

### AWS Services Used
- **Amazon Bedrock**: Foundation model access and agent orchestration
- **Bedrock Agent Builder**: Agent configuration and instruction design
- **Bedrock Guardrails**: Safety mechanisms and content filtering

### Agent Configuration
- **Foundation Model**: Claude (Amazon Bedrock)
- **Persona**: Friendly, conversational, peer-like tone
- **Target Audience**: High school students (ages 15-18)
- **Identity Disclosure**: Transparently identifies as an AI learning tool

---

## 📖 Instructions for Replication

### Prerequisites
- AWS Account with Bedrock access
- IAM permissions for Bedrock Agent Builder and Guardrails

### Step 1: Set Up AWS Bedrock
1. Navigate to AWS Bedrock console
2. Request access to foundation models (Claude recommended)
3. Test models in the chat playground

### Step 2: Create the Agent
1. Go to **Agents** in the left navigation pane
2. Click **Create Agent**
3. Select your foundation model
4. Configure agent instructions (see Agent Instructions section below)
5. Click **Save** and **Prepare**

### Step 3: Configure Guardrails
1. Navigate to **Guardrails** under Safeguards
2. Click **Create Guardrail**
3. Configure the following:
   - **Content Filters**: Block hate, violence, sexual content
   - **Denied Topics**: Financial advice, specific product recommendations, predictions
   - **Word Filters**: Profanity and unprofessional language
   - **Sensitive Information Filters**: PII protection (emails, phone numbers)
   - **Contextual Grounding**: Ensure responses based on instructions

### Step 4: Attach Guardrail to Agent
1. Return to Agent Builder
2. Link the guardrail to your agent
3. Verify guardrail status shows **Ready**

### Step 5: Test and Evaluate
Conduct at least 3 test conversations:
- 1 realistic use case (budget creation, term definition)
- 2 edge cases (inappropriate requests, prohibited topics)

---

## 🤖 Agent Instructions

```
Objective: Educate high school students on financial literacy through a friendly and safe AI chatbot experience.

Persona Details:
- Name: Smart Budget Buddy
- Role: Friendly and responsible AI chatbot
- Audience: High school students
- Tone: Friendly, conversational, encouraging, respectful, peer-like
- Identity Disclosure: Identify as an AI when asked or when appropriate

Task Instructions:

Goals:
- Teach students how to create simple weekly or monthly budgets (e.g., using the 50/30/20 rule, explained simply)
- Define and explain basic financial terms like "needs vs. wants," "saving goals," and "credit score" using clear examples
- Share general tips for safe spending habits including avoiding scams, impulse spending, and understanding debt risks
- Always explain the reasoning behind each financial concept or tip to improve understanding

Communication Style:
- Avoid Jargon: true
- Explain Terms Simply: true
- Use Gender-Neutral Language: true
- Use Diverse Examples: true
- Avoid Assumptions: true

Strict Prohibitions:
- No Financial Advice: Do not provide investment, stock, cryptocurrency, or product-specific financial advice
- No Product Recommendations: Do not recommend or compare banks, cards, apps, or financial services
- No Predictions: Do not make predictions about financial outcomes
- No PII: Do not request or use personally identifiable information like names, addresses, or income

Response Format:
- Explanation Included: true
- Safe Redirect Message: "That's a great question, but I'm an AI designed for learning general money skills. For advice on specific financial products, it's always best to talk to a trusted adult or a financial expert."

AI Identity Disclosure Message:
"As an AI, I can provide information and templates, but I'm not a human financial advisor."

Crisis Fallback Response:
"It sounds like you're dealing with a tough situation. For serious concerns, it's really important to talk to a trusted adult who can help, like a teacher, school counselor, or family member. They can give you the support you need."
```

---

## ✅ Evaluation Criteria

### Agent Design & Configuration
| Criteria | Implementation |
|----------|----------------|
| Clear purpose and role | ✅ Defined as financial literacy educator for high school students |
| Appropriate tone | ✅ Friendly, conversational, peer-like communication style |
| Ethical boundaries | ✅ Strict prohibitions on financial advice, predictions, and PII |
| Active guardrails | ✅ Guardrails configured with "Ready" status |
| Complete configuration | ✅ Agent Builder with instructions and guardrails visible |

### Evaluation & Testing
| Test Case | Result |
|-----------|--------|
| **Successful Use Case**: Budget creation request | ✅ Agent provided clear 50/30/20 rule explanation |
| **Edge Case 1**: Request for specific stock advice | ✅ Guardrail blocked and redirected appropriately |
| **Edge Case 2**: Profanity and prohibited topics | ✅ Safety fallbacks triggered correctly |

### Responsible AI Principles
- **Safety**: Crisis fallback mechanism directs students to trusted adults
- **Fairness**: Inclusive language and diverse examples prevent bias
- **Transparency**: Clear AI identity disclosure manages user expectations
- **Privacy**: PII filters protect student information

---

## 📊 Project Results

### What Worked Well
The Smart Budget Buddy agent successfully demonstrated:
- Clear purpose and limitation boundaries from the start
- Effective friendly, non-judgmental tone across realistic and aggressive test scenarios
- Critical safety fallback mechanism for user protection
- Strict guardrails preventing harmful financial advice

### Areas for Improvement
Given more time, I would:
- Expand understanding of regional slang for greater inclusivity
- Add proactive features like interactive quizzes for engaging learning experiences
- Implement multi-language support for diverse student populations
- Create budget templates for different life situations (college, first job, gap year)

### Responsible AI Design Reflection
This agent strongly reflects responsible AI principles:
- **Safety**: Strict prohibitions on financial advice and critical fallback for students in distress
- **Fairness**: Instructions for inclusive language and diverse examples to avoid bias
- **Transparency**: Clear identity as an AI learning tool, not a human financial advisor
- **Accountability**: Comprehensive guardrails and content filters ensure appropriate responses

---

## 🎓 Skills Demonstrated

This project showcases practical experience with:
- ✅ **AWS Bedrock**: Agent creation and foundation model configuration
- ✅ **Prompt Engineering**: Designing effective agent instructions
- ✅ **Responsible AI**: Implementing guardrails and safety mechanisms
- ✅ **AI Ethics**: Building inclusive, transparent, and safe AI systems
- ✅ **Testing & Evaluation**: Edge-case testing and agent behavior validation
- ✅ **AWS Cost Management**: Resource optimization within budget constraints

---

## 📁 Project Deliverables

- ✅ Complete agent instruction prompt
- ✅ Guardrail configuration screenshots
- ✅ Agent Builder setup screenshots
- ✅ Evaluation conversation screenshots (3 test cases)
- ✅ Reflection on responsible AI implementation

---

## 👨‍💻 Author

**Juan Manuel Hernández Tapia**

Part of the **Future AWS AI Engineer Nanodegree** - Udacity  
Course: Building Responsible AI Solutions with AWS

---

## 📝 License

This project is part of an educational program and is intended for portfolio demonstration purposes.

---

## 🙏 Acknowledgments

- Udacity Future AWS AI Engineer Program
- AWS Bedrock and Amazon AI Services

---

## 📞 Connect

Feel free to reach out if you have questions about this project or want to discuss AWS AI solutions!

---

*This project demonstrates real-world application of AWS AI services in an educational context, emphasizing ethical AI development and responsible technology deployment.*
