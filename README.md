# CSharp prototype repository

This repository contains the code underlying the WEBEXPO C# prototype, allowing to use it as a starting point to build their own applications.

A functioning prototype can be downloaded from this [dropbox link](https://www.dropbox.com/s/3hhsxnvn8jtphav/WebexpoPrototypeCsharp.zip?dl=0). Simply dowload and extract the zip archive into a folder of your choice and double click the WebExpo.InterfaceGraphique.Csharp.exe file. The prototype includes a bilingual French/English infrastructure. The French version can be launched double clikcing the WebExpo.InterfaceGraphique.Csharp.fr.bat file.

The scientific report describing the principles and details of the calculations allowed by the WEBEXPO algorithms is not public yet, but some details can be found [here](http://www.expostats.ca/site/en/webexpoen.html). The abstract of the scientific report can be found below.

-----------------------------------------------------------------------------------------------------

A significant part of industrial hygiene activities is the measurement of workers’ occupational exposure levels. Considerable spatial and temporal variability is usually observed in most exposure assessment surveys, frequently with upto 10-fold variations in exposure intensity despite apparently similar conditions. This has historically represented an important challenge to the interpretation of measured levels with regard to comparison with occupational exposure limits (OELs). There now exists a consensus framework, progressively developed during the last two decades, for the analysis of exposure levels related to exposure limits. Within this framework, exposure levels are assumed to follow, at least approximately, a lognormal distribution. Several parameters from the underlying distribution deemed associated with health risk are estimated from a number of measurements and interepreted relative to the OEL. 

These developments, although permitting a better assessment of risk compared to historical approaches, have not been widely adopted by industrial hygiene practitioners, and involve notions of statistics not usually taught in traditional education programs. Moreover they require calculations not usually feasible in common tools such as calculators or spreadsheet programs. While some specific tools have been developed over the years, usually through volunteer initiatives, most are lacking in several areas, be they accessibility, functionality, user-friendliness or complexity. In addition, uncertainty in parameter estimates has mostly been taken into account through formal hypothesis tests or the calculation of confidence intervals, the results of which are not easily conveyed to decision makers, hampering the ability of practitioners to efficiently communicate risk. Finally, available tools are standalone, and are not easily amenable to integration within an existing data management structure.

The WEBEXPO projects aimed at improving current practices in the interpretation of occupational exposure levels through the creation of a library of algorithmic solutions to frequently asked risk assessment questions in industrial hygiene. Most of these questions require the estimation of parameters from one or several distributions. WEBEXPO has utilized Bayesian statistics to perform these tasks.  Bayesian was chosen due to two main advantages: first, Bayesian methods provide inferences in direct probabilistic terms (e.g. what are the odds that….), facilitating risk communication. Second, they tackle methodological issues traditionally rarely taken into account, such as the data reported as not detected (a frequent concern). The three specific objectives of WEBEXPO included 1) To assess current needs in calculation, documentation and risk communication associated with the interpretation of occupational exposure measurement data. 2) To create a library of computer programming code based on Bayesian statistics that answers a set of data interpretation questions elaborated in specific objective 1. 3) To create prototype tools using the code from specific objective 2 that computes industrial hygiene statistics and answers to needs established in specific objective 1.

Specific objective 1 was achieved through a review of international guidelines and recent relevant literature complemented by meetings with stakeholder and experts committees. Specific objective 2 was achieved through creating bayesian solutions to the list of calculations finalised in step 1, implementing these algorithms in statistical code, and translating the code into programming language. Finally the programming algorithms were used to create functioning data analysis prototypes able to showcase the calculation and useable as starting point for the creation of practical data analysis tools.

The list of relevant calculations resulting from specific objective one and later implemented mathematically and in the form of algorithms and prototypes included two main avenues. The first involved estimating parameters from one distribution, i.e., the traditional “similar exposure group” approach. The measurements are assumed to come from a distribution of exposures shared by a group of workers performing similar tasks. As an illustration, this model permits to answer the question: “What is the probability that unmeasured exposures for this group exceed the OEL more than 5% of the time?”. The second model extends the first model by permitting to estimate to what extent a group of workers does or does not share similar exposures. The global exposure variability is split into within and between worker variability. It is possible to assess the group risk but also whether some individual workers might experience higher risk than the group. As an illustration, this model permits to answer the question: “Although group exposure seems acceptable, what is the probability that a randomly selected worker might experience exposure exceeding the OEL more that 5% of the time?”. All models include the seemless treatment of non-detects and take into account measurement error associated with the observations. 

The resulting algorithms are available in R, aimed at academics, C#, for standalone offline or server-based applications, or JavaScript, for web-based applications. They include data entry, core Bayesian estimation, numerical data interpretation modules, as well as a limited user interface for the C# and JavaScript prototypes. The code is publicly available to allow users to build their own applications.

The WEBEXPO project should result in the availability for the industrial hygiene community of a comprehensive toolbox for the interpretation of occupational exposure levels, with the added flexibility for users to build or adapt their own software instead of using a new one.


