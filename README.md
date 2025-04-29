# cs3245---homework-4-legal-case-retrieval-mini-project-solved
**TO GET THIS SOLUTION VISIT:** [CS3245 – Homework #4 Â» Legal Case Retrieval Mini Project Solved](https://www.ankitcodinghub.com/product/cs3245-homework-4-a-legal-case-retrieval-mini-project-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;114628&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS3245 - Homework #4 Â» Legal Case Retrieval Mini Project Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Commonalities with Homeworks #2 and #3

The indexing and query commands will use an (almost) identical input format to Homeworks #2 and #3, so that you need not modify any of your code to deal with command line processing. To recap:

Indexing: $ python index.py -i dataset-file -d dictionary-file -p postings-file Searching: $ python search.py -d dictionary-file -p postings-file -q query-file -o output-file-ofresults

The differences from Homeworks #2 and #3 are that 1) dataset-file is a csv file containing all the documents to be indexed, and 2) query-file specifies a single query instead of a list of queries.

However, significantly different from the previous homework, we will be using a legal corpus, provided by Intelllex, a company with origins partially from NUS.

Problem Statement: Given 1) a legal corpus (to be posted in LumiNUS Files) as the candidate document collection to retrieve from, and 2) a set of queries (each query in its own file), return the list of the IDs of the relevant documents for each query, in sorted order of relevance. Your search engine should return the entire set of relevant documents (don’t threshold to the top K relevant documents).

Your system should return the results for the query query-file on a single line. Separate the IDs of different documents by a single space ‘ ‘. Return an empty line if no cases are relevant.

Intelllex, the company we are working with for this contest, is particularly interested in good IR systems for this problem and thus is cooperating with us for this homework assignments. They have provided the corpus (the documents are in the public domain, as is most government information, but the additional structuring the Intelllex team has done is their own work) and relevance judgments for a small number of queries.

More detail on the inputs: Queries and Cases

The legal cases and the information needs have a particular structure in this task. Let’s start with the information needs.

Queries:

In Intelllex’s own system, searchers (lawyers or paralegals) use the familiar search bar to issue free text or Boolean queries, such as in the training query q1.txt: quiet phone call. and q2.txt: “fertility treatment” AND damages. The keywords enclosed in double quotes are meant to be searched as a phrase. The phrases in the queries are 2 or 3 words long, max; so you if you are able to deal with phrasal queries, you can support them using n-word indices or with positional indices. There are no ORs, NOTs or parentheses in the queries issued by us so you can simplify your query parsing code if you choose.

Query Relevance Assessments:

quiet phone call

6807771

3992148

4001247

The above indicates that there are 3 documents, with document_ids 6807771, 4001247 and 3992148, that are relevant to the query.

Cases:

The legal cases are given in a csv file. Each case consists of 5 fields in the following format: “document_id”,”title”,”content”,”date_posted”,”court”.

Below are snippets of a document, ID 6807771, a case relevant to the above example query:

“6807771”,”Burstow R v. Ireland, R v. [1997] UKHL 34″,”JISCBAILII_CASES_CRIME

JISCBAILII_CASES_ENGLISH_LEGAL_SYSTEM

ï¿½ï¿½Lord Goff of Chieveley ï¿½ï¿½Lord Slynn of Hadley ï¿½ï¿½Lord Steyn

ï¿½ï¿½Lord Hope of Craighead ï¿½ï¿½Lord Hutton

…

I would therefore answer the certified question in the affirmative and dismiss this appeal also.”,”1997-07-24 00:00:00″,”UK House of Lords”

Zones and Fields

As introduced in Week 8, Zones are free text areas usually within a document that holds some special significance. Fields are more akin to database columns (in a database, we would actually make them columns), in that they take on a specific value from some (possibly infinite) enumerated set of values.

Along with the standard notion of a document as a ordered set of words, handling either / both zones and fields is important for certain aspects of case retrieval.

Query Refinement

It is compulsory to implement at least one query refinement technique, such as (pseudo) Relevant Feedback and Query Expansion in your system. You might choose to switch it off in

–

For example, we can perform a preliminary round of retrieval on the query terms. We can then assume that the top few documents are relevant and expand the query by 1) using the Rocchio formula, or 2) extracting important terms from these documents and adding them to the query. This is basically pseudo relevance feedback.

As another example, we can use manually created ontology (e.g., WordNet) or automatically generated thesauri (e.g., Co-occurrence Thesaurus) to identify related query terms.

Constraint on Index / Submission Size

Although you are free to explore different techniques in your system, you should keep your index at a reasonable size (e.g., by choosing space-efficient techniques and / or applying indexing compression techniques). Otherwise, your approach is not really scalable.

Since the corpus size is around 700MB, your submission (i.e., code + documentation + index + other miscellaneous files) should be no more than 800MB before zipping. Submissions that fail to comply with this constraint will be

rejected.

What to turn in?

You are required to submit README.txt, index.py, search.py, dictionary.txt, and postings.txt. Please do not include the legal case corpus.

Submission Formatting

You are allowed to do this assignment individually or as a team of up to 4 students. There will be no difference in grading criteria if you do the assignment as a large team or individually. For the submission information below, simply replace any mention of a student number with the student numbers concatenated with a separating dash (e.g., A000000X-A000001Y-A000002Z). Please ensure you use the same identifier (student numbers in the same order) in all places that require a student number.

For us to grade this assignment in a timely manner, we need you to adhere strictly to the following submission guidelines. They will help us grade the assignment in an appropriate manner. You will be penalized if you do not follow these instructions. Your student number in all of the following statements should not have any spaces and any letters should be in CAPITALS. You are to turn in the following files:

A plain text documentation file README.txt: this is a text only file that describes any information you want me to know about your submission. You should not include any identifiable information about your assignment (your name, phone number, etc.) except your student number and email (we need the email to contact you about your grade, please use your e***@u.nus.edu address, not your email alias). This is to help you get an objective grade in your assignment, as we won’t associate student numbers with student names. You should use the README.txt template given to you in Homework #1 as a start. In particular, you need to assert whether you followed class policy for the assignment or not.

All source code. We will be reading your code, so please do us a favor and format it nicely. Again, if you’re using external libraries, make sure to include some nicely so they play well with our default ir_env environment (and acknowledge your external libraries as a source of help in your submission).

Grading Guidelines

The grading criteria for the assignment is below.

35% Documentation. This component is graded with a higher weightage in this assignment than in previous ones. This component breaks down into the following two subcomponents:

5% For following the submission instructions and formatting your documentation accordingly. 5% For code level documentation.

65% Performance of your code. This component breaks down into several subcomponents:

25% We will compare it against a baseline TFÃ—IDF ranked retrieval implementation, in which the entire document is treated without zones (i.e., all zone/field information is removed). If your system works at least as good as the standard baseline, you will receive all 25% for this component.

35% We will use a competition framework to assign credit to teams and to show the leaderboard. Submissions will begin to be auto-run with a 3-hour delay (to prevent phishing for relevant documents). You can make submissions from 17 Apr. The framework will attempt to auto-run your code, with the training queries and a few other development queries (hidden from you, but run by the framework, please do not try to log these developmental queries. If in a team, please do not permute your student numbers to allow yourselves additional runs; this is unfair to smaller teams. NLTK is installed on the system.

5% We will measure the time efficiency of your system to answer queries. Your system should be able to answer a query within one minute. This requirement is mostly so that we can grade assignments in a timely manner.

Hints

Working in a group can be helpful but can be counter-productive too. We have observed that group work tends to make homework submissions grades slightly higher than single submissions but also more average (it’s harder to have an outstanding grade with a group). If you think you work better in a larger group, please do. Make sure to clearly partition the work and demarcate the API between your modules.

Bulletproof your input and output. Note that now the input is only a singe file instead of a directory. Check that your output is in the correct format (docIDs separated by single spaces, no quotations, no tabs).
