<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>index.md</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__left">
    <div class="stackedit__toc">
      
<ul>
<li><a href="#combining-keystroke-and-mouse-dynamics-for-a-stronger-and-more-usable-authentication-mechanism.">Combining Keystroke and Mouse Dynamics for a Stronger and More Usable Authentication Mechanism.</a></li>
<li><a href="#index">Index</a>
<ul>
<li><a href="#project-timeline">Project Timeline:</a></li>
</ul>
</li>
<li><a href="#introduction">1. Introduction</a></li>
<li><a href="#related-works">2. Related Works</a>
<ul>
<li><a href="#the-landscape">2.1 The Landscape</a></li>
<li><a href="#algorithmic-works">2.2 Algorithmic Works</a></li>
<li><a href="#systems-and-integration">2.3 Systems and Integration</a></li>
</ul>
</li>
<li><a href="#our-contribution">3. Our Contribution</a></li>
<li><a href="#approach-and-model">4. Approach and Model</a>
<ul>
<li>
<ul>
<li></li>
</ul>
</li>
</ul>
</li>
<li><a href="#extending-the-model-and-its-integration">5. Extending the Model and its Integration</a></li>
<li><a href="#results-and-conclusion">6. Results and Conclusion</a></li>
<li><a href="#references">References</a></li>
<li><a href="#further-readings-and-notes">Further Readings and Notes</a></li>
</ul>

    </div>
  </div>
  <div class="stackedit__right">
    <div class="stackedit__html">
      <h1 id="combining-keystroke-and-mouse-dynamics-for-a-stronger-and-more-usable-authentication-mechanism.">Combining Keystroke and Mouse Dynamics for a Stronger and More Usable Authentication Mechanism.</h1>
<hr>
<h1 id="index">Index</h1>
<ul>
<li><a href="#project-timeline">Project Timeline</a></li>
</ul>
<ol>
<li><a href="#introduction">Introduction</a></li>
<li><a href="#related-works">A Survey of Related Works</a><br>
2.1 <a href="#the-landscape">The Landscape</a><br>
2.2 <a href="#algorithmic-works">Algorithmic works</a><br>
2.3 <a href="#systems-and-integration">Systems and Integration</a></li>
<li><a href="#our-contribution">Our Contribution</a></li>
<li><a href="#approach-and-model">Approach and Model</a><br>
4.1 <a href="#data-acquisition">Data Acquisition</a><br>
4.2 <a href="#design">Design</a><br>
4.3 <a href="#performance-measurement">Performance Measurement</a></li>
<li><a href="#results">Results</a></li>
</ol>
<ul>
<li><a href="#references">References</a></li>
<li><a href="#further-readings-and-notes">Further Readings and Notes</a></li>
</ul>
<h2 id="project-timeline">Project Timeline:</h2>
<p><strong>Title</strong>- Combining Keystroke and Mouse Dynamics for a Stronger and More Usable Authentication Mechanism.<br>
<strong>Proposal</strong>- April, 2018.<br>
<strong>Break</strong>- June-August, 2018.<br>
<strong>Literature Review/ Proposal Corrections</strong>- Sep-November 15, 2018.<br>
<strong>Development/ Testing/ Results</strong>- November 15- December 15, 2018.<br>
<strong>Publication Drafts Deadline</strong>- January 15, 2019.<br>
<strong>Beta-Deployment Deadline</strong>- January 30, 2019.<br>
<strong>Hard-Deadline for Final Submission</strong>- May, 2019.</p>
<hr>
<h1 id="introduction">1. Introduction</h1>
<p>Since as early as the late 70s,  researchers and organizations alike have been concerned about user authentication and verification to prevent unauthorized access to computer systems <a href="#meissner">[Meissner]</a> <a href="#fips">[FIPS 1977]</a>. Followed by the unprecedented and almost a sudden proliferation of computers and world-wide web services, authentication has become a daily chore for all of us. Even though authentication techniques come in different forms and flavors, the majority of them are still using a text-based authentication system.</p>
<p>Owing to its simplicity, text-based authentication techniques have their own distinctive appeal. Like any other information science component, however, it too is not perfect and there are a range of well-known exploits. Likewise, researchers have tried to make the text-based authentication systems more resilient by enhancing it with different additional techniques. Thorough and critical works ranging from better security policy designs <a href="#shay">[Shay]</a> to very difficult to exploit Multi-Factor Authentication (MFA) mechanisms<a href="#weber">[Weber]</a> to federal publications for security frameworks <a href="#nist">[NIST]</a>.</p>
<p>Aware of the observations that showed that each telegraph operator had a distinct pattern of keying <a href="#bryan">[Bryan &amp; Harter]</a> and that typing is motor-programmed skill which is organized in advance of its actual execution <a href="#shaffer">[Shaffer]</a> , <a href="#leggett">[Leggett et al.]</a> proposed one of the earliest identity verification scheme based on keystroke characteristics. Since keystroke dyanamics are personal characteristics of authenticators, they can easily serve as a biometric. Traditionally, biometric methods such as fingerprints and physical tokens have been associated with additional security but they also come with an additional price. With access to keystroke dynamics, existing computing systems can be extended with this new biometric for almost no additional cost. <a href="#monrose">[Monrose]</a> proposed such a password hardening scheme using keystroke dynamics.</p>
<p>As mouse based Graphical User Interfaces started becoming common place, similar observations were made for mouse dynamics as well <a href="#ahmed">[Ahmed]</a>. Additionally, there are proposals for systems which combine both keystroke and mouse dynamics <a href="#mondal">[Mondal &amp; Bours]</a> <a href="#traore">[Traore et al.]</a>. In the <em>Related Works</em> section, we discuss various works in the field using a comprehensive framework.</p>
<p><strong>Keystroke and Mouse Dynamics for Usable Security</strong></p>
<p><s>The existing literature body in behavioral biometrics for authentication and identification emphasizes on ‘strengthening’ existing system by adding the layer(s) of behavioral biometrics in addition to existing authentication, say only text-based username-password authentication. A simplistic logic being used is that such a system would be far more secure, but the extra load on the part of the user is being ignored. For instance, in case of <strong>static</strong> authentication, out of the fear of going through a longer authentication process, a user may choose not to logout of authentication sessions. <strong>Continuous</strong> authentication systems, on the other hand, may not be practical for all applications.</s></p>
<p>** Usable Security diagram goes here. **</p>
<p>Although it is left to be explored in future works, we are yet to see the practical implications of the extra burden of the behavioral biometric that let us achieve the extra theoretical security. <a href="#herley">[Herley]</a> argues that the user’s rejection of the security advice they receive is entirely rational from an economic perspective. Arguing about stronger password policies, <a href="#inglesant">[Inglesant]</a> shows that there is a negative impact on the productivity of users and their organizations.  However, inferring from conclusions in <a href="#shay">[Shay et. al]</a>, we may conclude that users in systems with behavioral biometric authentication systems will feel more secure.</p>
<p>This paper presents also presents a scheme where the benefits of added security due to multi-factor static authentication  could be enjoyed with much more usability; hence, guaranteeing a better practical performance than previous schemes. In essence, the behavioral biometrics become a decision layer between text-based authentication and extra layers of authentication. Behavioral biometrics is not an end in itself, it is rather a means to an end; the end is more practical security. <a href="#pin">[Pin et al.]</a> comes closest to such an outlook but it only accomodates for keystroke dynamics and there is an initial enrollment phase.</p>
<h1 id="related-works">2. Related Works</h1>
<h2 id="the-landscape">2.1 The Landscape</h2>
<p>Current research literature for using keyboard and/ or mouse biometric dynamics for security improvements is very diverse. There are some which pertain to alogorithmic optimizations, while others are new integration proposal. For a comprehensive review, we suggest the following approach. Current publications  fall under the following categor(y/ies) of:</p>
<h2 id="algorithmic-works">2.2 Algorithmic Works</h2>
<p>Majority of the algorithmic works are concerned with improving the results of existing publications.  <a href="#leggett">[Leggett et al.]</a> was one of earliest to propose a dynamic authentication system using statistical methods for digraph latency analysis between the keystroke. <a href="#killourhy">[Killourhy et al.]</a> put forth a survey of various algorithms on a a data set of typing behaviour of 51 typists; the dataset was made public (henceforth, referred to as CMU keystroke dataset) and many works have reported performance improvements using different algorithmic techniques <a href="#deng">[Deng &amp; Zhong, 2013]</a> <a href="#deng">[Zhong et al., 2013]</a><a href="#Ali">[Ali et al., 2017]</a>. There are other works which have reported performances on different datasets in their experiments. <a href="#rezaei">[Rezaei &amp; Mirzakochaki, 2012]</a>, for instance, reports a FAR and FRR of 0.0% using a combination of various classifiers.</p>
<pre><code>There is a similar contribution on mouse dynamics as well [\[Salman &amp; Hameed, 2018\]](#salman) [\[Shen et al., 2013\]](#shen) [\[Ahmed &amp; Traore, 2007\]](#ahmed). Some notable contributions use both keystroke and mouse dynamics, hence, effectively using a multi-modal model for the two different biometrics [\[Traore et al., 2012\]](#traore)[\[Mondal &amp; Bours, 2016\]](#mondal). In terms of data sources, some works rely on  **single modality** i.e. either of the two behavioral biometrisc or a **multi-modal** model which takes both keystroke and mouse dynamics as input. A more thorough tabular survey can be found in [table 1](#table1).
</code></pre>
<h2 id="systems-and-integration">2.3 Systems and Integration</h2>
<p>Systems and Integration is concerned with the “big-picture” of putting the final work within an existing system with some well-defined purpose. Some works define there application and integration in detail <a href="#shen">[Shen et al., 2013]</a> <a href="#mondal">[Mondal &amp; Bours, 2016]</a> while some focus more on the algorithmic side and do not feel the necessity to do so. In general, all the published works in behavioral biometric methods for identification and authentication fall in either of the two categories:<br>
1. <strong>Static Authentication</strong> relies on behavioral biometrics only once, ideally during the authentication phase. Once a an authentication session is active, the biometric authentication methods are not triggered.<br>
2. <strong>Continuous Authentication</strong> methods have also been suggested in the literature. In this case, the behavioral biometrics is continuously monitored and an active session is maintained as long as the system is convinced about the authenticity of its user.</p>

<table>
<thead>
<tr>
<th align="center">Publication</th>
<th align="center">Purpose</th>
<th align="center">Approach</th>
<th align="center">Data Sources</th>
<th align="center">Performance</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><a href="#mondal">Mondal &amp; Bours, 2016</a></td>
<td align="center">Contiuous Authentication and Indentification</td>
<td align="center">Pairwise Coupling</td>
<td align="center">Mouse and Keyboard (25)</td>
<td align="center">Identification Accuracy Rate = 62.2%</td>
</tr>
<tr>
<td align="center"><a href="#leggett">Leggett et al., 1991</a></td>
<td align="center">Continuous and Static Authentication</td>
<td align="center">Digraph Analysis &amp; Sequential Statistics Theory</td>
<td align="center">Keyboard (36)</td>
<td align="center"><strong>Static</strong> (FAR=11.7%, IPR=5.8%) <strong>Dynamic</strong> (FAR=11.1%, IPR=12.8%)</td>
</tr>
<tr>
<td align="center"><a href="#deng">Deng &amp; Zhong, 2013</a></td>
<td align="center">Static Authentication</td>
<td align="center">Gausian Mixture Model &amp; Deep Belief Nets</td>
<td align="center">CMU Dataset</td>
<td align="center"><strong>GMB</strong> (EER = 5.5%) <strong>DBN</strong> (EER = 3.5)</td>
</tr>
<tr>
<td align="center"><a href="#deng">Zhong et al., 2013</a></td>
<td align="center">Static Authentication</td>
<td align="center">Combined Mahalanobis &amp; Manhattan Distance</td>
<td align="center">CMU Dataset</td>
<td align="center">EER = 8.4%</td>
</tr>
<tr>
<td align="center"><a href="#killourhy">Killourhy et al., 2009</a></td>
<td align="center">Static Authentication</td>
<td align="center">Manhattan (scaled), Euclidean, Nearest Neighbor (Mahalanobis), SVM (one-class), Fuzzy Logic, k-Means, etc.)</td>
<td align="center">CMU Dataset</td>
<td align="center"><strong>Manhattan</strong>(EER = 9.6%, FAR = 60.1%) <strong>Euclidean</strong> (EER = 17.1%, FAR = 87.5%) <strong>Nearest Neighbor (Mahalanobis)</strong> (EER = 10.0%, FAR = 46.8%) <strong>SVM (one-class)</strong> (EER = 10.2%, FAR = 50.4%) <strong>Fuzzy Logic</strong> (EER = 22.1%, FAR = 93.5%) <strong>k Means</strong> (EER = 37.2%, FAR = 98.9%)</td>
</tr>
<tr>
<td align="center"><a href="#salman">Salman &amp; Hameed, 2018</a></td>
<td align="center">Continuous Mouse Authentication</td>
<td align="center">Neural Network, Gaussian Naive Bayes</td>
<td align="center">Mouse Dynamics of 48 users over 998 sessions.</td>
<td align="center">FAR = 2.6%, FRR = 2.5%</td>
</tr>
<tr>
<td align="center"><a href="#shen">Shen et al., 2013</a></td>
<td align="center">Static Mouse Authentication</td>
<td align="center">One Class SVM, Neural Network Backpropagation(NN-BP), 3 Nearest Neighor</td>
<td align="center">5550 samples of 37 subjects</td>
<td align="center"><strong>SVM</strong> (FAR = 8.74%, FRR = 7.96%) <strong>NN-BP</strong> (FAR = 12.78%, FRR = 12.22%) <strong>3 Nearest Neighor</strong> (FAR = 15.67%, FRR = 14.53%)</td>
</tr>
<tr>
<td align="center"><a href="#lin">Lin, 1997</a></td>
<td align="center">Static Authentication</td>
<td align="center">Three layered back-propagation neural network</td>
<td align="center">90 valid users and 61 invalid keystroke dynamics</td>
<td align="center">FAR = 1.1% IPR = 0.0%</td>
</tr>
<tr>
<td align="center"><a href="#ahmed">Ahmed &amp; Traore, 2007</a></td>
<td align="center">Mouse based biometric detection</td>
<td align="center">Neural Network</td>
<td align="center">45 average sessions (each 30 minutes long) for 21 users</td>
<td align="center">FAR = 2.5% FRR = 2.5%</td>
</tr>
<tr>
<td align="center"><a href="#rezaei">Rezaei &amp; Mirzakochaki, 2012</a></td>
<td align="center">Static Authentication</td>
<td align="center">Fusion of LDC, QDC and K-NN classifiers</td>
<td align="center">100 keystroke patterns for 24 users</td>
<td align="center">FRR = 0.0% FAR = 0.0% EER = 1.15%</td>
</tr>
<tr>
<td align="center"><a href="#Ali">Ali et al., 2017</a></td>
<td align="center">Static Keystroke verification</td>
<td align="center">Partially observable HMM</td>
<td align="center">CMU dataset</td>
<td align="center">EER = 4.5%</td>
</tr>
<tr>
<td align="center"><a href="#traore">Traore et al., 2012</a></td>
<td align="center">Static Mouse and Keystroke Authenticaition</td>
<td align="center">Bayesian Fusion</td>
<td align="center">Keystroke and Mouse behavior of 24 users</td>
<td align="center">EER = 8.21%</td>
</tr>
</tbody>
</table><p><a id="table1"></a> Table 1: Previous works using different techniques for using behavioral biometrics for different purposes.</p>
<h1 id="our-contribution">3. Our Contribution</h1>
<p>The focus of this paper is to use behavioral authentication as a decision layer in authentication systems. If the behavriol authentication are above a certain confidence threshold, the user is successfully authenticated, otherwise additional authentication challenges could be posed to the user to verify his/ her identity. Our contribution is unique in that:</p>
<ol>
<li>We focus on using behavioral biometrics for additional security but at <strong>no extra cost</strong> on the part of the user in terms of usability. In other words, we user behavioral biometric as a part of an enhanced security protocol that dynamically adapts for more usability and yet offering the same level of security.</li>
<li>We are able to achieve a usable level of performance in an environment where the <strong>data is scarce</strong> due to the short interaction time between the user and the computer (typically 5-15 seconds) per session.</li>
<li>There are <strong>no additional requirements in terms of hardware, software or add-ons</strong>. A web-browser with JavaScript enabled is all that is required on the authenticator side. Additionally, on the user side, there is no additional requirement whatsoever.</li>
<li>We propose a hierarchical scheme where the <strong>algorithm is adaptive and allows for different behaviors pertaining to a user</strong>.</li>
</ol>
<h1 id="approach-and-model">4. Approach and Model</h1>
<p>Instead of using an enrollment phase, we collect keystroke and mouse dynamics from the user from every authentication session (described  further in <em>Data Acquisition</em> section below). After multiple successful login attempts, the algorithm generates a biometric profile. The total number of authentications required before a successful biometric profile is generated will depend on the variability in modelling the particular user’s behavior. After a profile is generated, in the future login attempts, the user’s keystroke and mouse dynamics will be checked against to get the full advantage of using keystroke and mouse dynamics for authentication. The next section describes how the model is extended to handle multiple profiles based on user’s interaction on different systems and how the profiles are <em>ranked</em>.</p>
<h4 id="data-acquisition">4.1 Data Acquisition</h4>
<h5 id="keystroke-dynamics">4.1.1 Keystroke Dynamics</h5>
<p>The keystroke dynamics is collected from the time the authentication session starts. The kestroke dynamics vector is essnetially a time-series of three attributes:</p>
<ol>
<li><strong>K<sub>P</sub></strong>, the key identifier for the key P that was pressed.</li>
<li><strong>K<sub>PD</sub></strong>, the time when the key was pressed.</li>
<li><strong>K<sub>PU</sub></strong>, the time when the key was released.</li>
</ol>
<p>From the above attributes, a new feature vector is generated which has additional information like digraph timing and in-flight time i.e. the time between when a key was released and the following key was pressed. Additionally, the time when the first key was pressed is set to zero to normalize the data.</p>
<h5 id="mouse-dynamics">4.1.2  Mouse Dynamics</h5>
<p>The raw data that is collected is a time-series of two attributes:</p>
<ol>
<li><strong>M<sub>B</sub></strong>: is the identifier of any mouse button that is pressed.</li>
<li><strong>M<sub>M</sub></strong>: This event is fired everytime the mouse moves. Essentially, in modern browsers, it is the position of the mouse pointer with different time resolutions. We collect the information of pointer co-ordinates against time.</li>
</ol>
<p>Unlike keyboard dynamics, we do not normalize the time as <strong>M<sub>M</sub></strong> is fired only when the mouse moves and that is actually a signal that the session is active. Like the keystroke dynamics, the mouse movement is also mapped a direction attribute which could take twelve different values, plus the pointer acceleration values. But these values are derived and calculated only after the above mentioned data points have been collected.</p>
<h4 id="design">2.2 Design</h4>
<h5 id="feature-extraction-and-noise-reduction">2.2.1 Feature Extraction and Noise Reduction</h5>
<pre><code>Informativeness of features [(Frank et al., 2012)](#frank)
Kalman Filters (have never been applied before in the field).
</code></pre>
<h5 id="fusion-of-the-two-modalities">2.2.2 Fusion of the two modalities:</h5>
<pre><code>The question is how do we treat the two biometrics together for generating the profiles and authentication?
The two major works [Traore] and [Modal] propose fusion methods: 
1. [Mondal] uses Pairwise coupling but the performance is really poor for our implementation- needs 333 actions and Identification rate is 58.9%.
2. [Traore] uses Bayesian fusion and the performance , at least in terms of EER is 8.21% which is still promising and it took 8 weeks for the algorithm to learn the behavior.
</code></pre>
<p>I am proposing a very simple <em>fusion</em> algorithm. Because the performance based on single modality i.e. either keystroke or mouse dynamics, taken independently, is much better in separate works. The proposed algorithm gives weights to classification result <strong>C<sub>K</sub></strong>, for Keystroke classfication and <strong>C<sub>M</sub></strong>, for mouse dynamics based classificaiton. Assuming C<sub>K</sub> and C<sub>M</sub> to be real numbers and are good estimates of confidence, we can assign weights <em>w<sub>K</sub></em> and <em>w<sub>M</sub></em> proportional to inverse of the standard deviation of the profile. If this simple heuristic doesn’t work, we can also Back Propagation Neural Network to assign the weights to every user independently.</p>
<h4 id="performance-measurement">2.2.3 Performance Measurement</h4>
<pre><code>Given the requirement that FAR has to 0.0%, find the best FRR.
</code></pre>
<h1 id="extending-the-model-and-its-integration">5. Extending the Model and its Integration</h1>
<pre><code>I think this section goes before the previous one because we use definitions from this section in the above one. Here I extend the model to handle multiple behaviors for a single user (for instance, to handle multiple devices) and the bigger picture of the profiling and authentication alogorithm and system.
</code></pre>
<h1 id="results-and-conclusion">6. Results and Conclusion</h1>
<h1 id="references">References</h1>
<p><a id="ahmed"></a> A. A. E. Ahmed and I. Traore, “A New Biometric Technology Based on Mouse Dynamics,” in <em>IEEE Transactions on Dependable and Secure Computing</em>, vol. 4, no. 3, pp. 165-179, July-Sept. 2007.<br>
doi: 10.1109/TDSC.2007.70207</p>
<p><a id="shen"></a> C. Shen, Z. Cai, X. Guan, Y. Du and R. A. Maxion, “User Authentication Through Mouse Dynamics,” in <em>IEEE Transactions on Information Forensics and Security</em>, vol. 8, no. 1, pp. 16-30, Jan. 2013.<br>
doi: 10.1109/TIFS.2012.2223677</p>
<p><a id="deng"></a> Deng, Yunbin, and Yu Zhong. 2013. “Keystroke Dynamics User Authentication Based on Gaussian Mixture Model and Deep Belief Nets.”  _ISRN Signal Processing_2013: 1–7. doi:10.1155/2013/565183.</p>
<p><a id="fips"></a> Federal Information Processing Standards Publication: Guidelines on evaluation of techniques for automated personal identification. (1977). doi:10.6028/nbs.fips.48</p>
<p><a id="frank"></a> Frank, M., Biedert, R., Ma, E., Martinovic, I., &amp; Song, D. (2013). Touchalytics: On the Applicability of Touchscreen Input as a Behavioral Biometric for Continuous Authentication. _IEEE Transactions on Information Forensics and Security,_<em>8</em>(1), 136-148. doi:10.1109/tifs.2012.2225048</p>
<p><a id="herley">Herley, Cormac. 2009. “So Long, and No Thanks for the Externalities.”  <em>Proceedings of the 2009 Workshop on New Security Paradigms Workshop - NSPW 09</em>. doi:10.1145/1719030.1719050.</a></p>
<p><a id="inglesant"></a> Inglesant, Philip G., and M. Angela Sasse. 2010. “The True Cost of Unusable Password Policies.”  <em>Proceedings of the 28th International Conference on Human Factors in Computing Systems - CHI 10</em>. doi:10.1145/1753326.1753384.</p>
<p><a id="killourhy"></a>Killourhy, K. S., &amp; Maxion, R. A. (2009). Comparing anomaly-detection algorithms for keystroke dynamics. <em>2009 IEEE/IFIP International Conference on Dependable Systems &amp; Networks</em>. doi:10.1109/dsn.2009.5270346</p>
<p><a id="leggett"></a> Leggett, John, Glen Williams, Mark Usnick, and Mike Longnecker. 1991. “Dynamic Identity Verification via Keystroke Characteristics.”  _International Journal of Man-Machine Studies_35 (6): 859–870. doi:10.1016/s0020-7373(05)80165-8.</p>
<p><a id="lin"></a> Lin, Daw-Tung. “Computer-Access Authentication with Neural Network Based Keystroke Identity Verification.”  <em>Proceedings of International Conference on Neural Networks (ICNN97)</em>. doi:10.1109/icnn.1997.611659.</p>
<p>Mahadi, Nurul Afnan, Mohamad Afendee Mohamed, Amirul Ihsan Mohamad, Mokhairi Makhtar, Mohd Fadzil Abdul Kadir, and Mustafa Mamat. 2018. “A Survey of Machine Learning Techniques for Behavioral-Based Biometric User Authentication.”  <em>Recent Advances in Cryptography and Network Security</em>. doi:10.5772/intechopen.76685.</p>
<p><a id="ali"></a>M. L. Ali, J. V. Monaco and C. C. Tappert, “Biometric studies with hidden Markov model and its extension on short fixed-text input,” <em>2017 IEEE 8th Annual Ubiquitous Computing, Electronics and Mobile Communication Conference (UEMCON)</em>, New York, NY, 2017, pp. 258-264.</p>
<p><a id="meissner"></a> <em>Meissner</em>, P., <em>Evaluation of techniques for verifying personal identity</em>, Proc. ACM- NBS Fifteenth Annual Technical Symp., Gaithersburg, MD, June 17, 1976, pp.</p>
<p><a id="mondal"></a>Mondal, Soumik, and Patrick Bours. 2016. “Combining Keystroke and Mouse Dynamics for Continuous User Authentication and Identification.”  <em>2016 IEEE International Conference on Identity, Security and Behavior Analysis (ISBA)</em>. doi:10.1109/isba.2016.7477228.</p>
<p><a id="monrose"></a> Monrose, Fabian, Michael K. Reiter, and Susanne Wetzel. 2002. “Password Hardening Based on Keystroke Dynamics.”  _International Journal of Information Security_1 (2): 69–83. doi:10.1007/s102070100006.</p>
<p>Obaidat, M. S., and B. Sadoun. “Keystroke Dynamics Based Authentication.”  <em>Biometrics</em>, 213–229. doi:10.1007/0-306-47044-6_10.</p>
<p><a id="rezaei"></a>Rezaei, A., &amp; Mirzakochaki, S. (2012). A Novel Approach for Keyboard Dynamics Authentication based on Fusion of Stochastic Classifiers.</p>
<p><a id="salman"></a> Salman O.A., Hameed S.M. (2019) Using Mouse Dynamics for Continuous User Authentication. In: Arai K., Bhatia R., Kapoor S. (eds) Proceedings of the Future Technologies Conference (FTC) 2018. FTC 2018. Advances in Intelligent Systems and Computing, vol 880. Springer, Cham</p>
<p><a id="shay"></a> Shay, Richard, Saranga Komanduri, Patrick Gage Kelley, Pedro Giovanni Leon, Michelle L. Mazurek, Lujo Bauer, Nicolas Christin, and Lorrie Faith Cranor. 2010. “Encountering Stronger Password Requirements.”  <em>Proceedings of the Sixth Symposium on Usable Privacy and Security - SOUPS 10</em>. doi:10.1145/1837110.1837113.</p>
<p><a id="shay1"></a> Shay, R., Cranor, L. F., Komanduri, S., Durity, A. L., Huh, P. (., Mazurek, M. L., . . . Christin, N. (2016). Designing Password Policies for Strength and Usability. _ACM Transactions on Information and System Security,_<em>18</em>(4), 1-34. doi:10.1145/2891411</p>
<p><a id="teh"></a>Teh, Pin Shen, Andrew Beng Jin Teoh, Connie Tee, and Thian Song Ong. 2010. “Keystroke Dynamics in Password Authentication Enhancement.”  _Expert Systems with Applications_37 (12): 8618–8627. doi:10.1016/j.eswa.2010.06.097.</p>
<p><a id="traore"></a> Traore, Issa, Isaac Woungang, Mohammad S. Obaidat, Youssef Nakkabi, and Iris Lai. 2012. “Combining Mouse and Keystroke Dynamics Biometrics for Risk-Based Authentication in Web Environments.”  <em>2012 Fourth International Conference on Digital Home</em>. doi:10.1109/icdh.2012.59.</p>
<p><a id="nist"></a>U.S. Department of Commerce. “Digital Identity Guidelines- Authentication and Lifecycle Management” <em>NIST Special Publication 800-63B</em> 2017.<br>
<a id="weber"></a> Weber, F. (2018). <em>Multi-factor authentication</em>. US7770002B2.</p>
<p>Y. Nakkabi, I. Traore and A. A. E. Ahmed, “Improving Mouse Dynamics Biometric Performance Using Variance Reduction via Extractors With Separate Features,” in <em>IEEE Transactions on Systems, Man, and Cybernetics - Part A: Systems and Humans</em>, vol. 40, no. 6, pp. 1345-1353, Nov. 2010.<br>
doi: 10.1109/TSMCA.2010.2052602</p>
<p>Zaidan, Dema, Asma Salem, Andraws Swidan, and Ramzi Saifan. 2017. “Factors Affecting Keystroke Dynamics for Verification Data Collecting and Analysis.”  <em>2017 8th International Conference on Information Technology (ICIT)</em>. doi:10.1109/icitech.2017.8080032.</p>
<p><a id="zhong"></a> Y. Zhong, Y. Deng and A. K. Jain, “Keystroke dynamics for user authentication,” <em>2012 IEEE Computer Society Conference on Computer Vision and Pattern Recognition Workshops</em>, Providence, RI, 2012, pp. 117-123.</p>
<h1 id="further-readings-and-notes">Further Readings and Notes</h1>
<p><a href="https://60cd0793-a-d5557daf-s-sites.googlegroups.com/a/vmonaco.com/vmonaco/publications/Behavioral%20Biometric%20Authentication%20in%20Human-Computer%20Interaction.pdf?attachauth=ANoY7cqV8mOgQgBpfpn1zMR_TjehFX0p87KMszyghD3Q-ZPy0PSHn1nS9c6jh-TM-b00uXVsn5H_U_y9l4WCBI3ZINXKlGrzYRY8XQuTbuI0xxzjV88tmVHO3wkIlHoez6fJ9LzvTEjRNAEW6fCMcjoZkKO-IZgnV6QDLt7itx5B2ctr1tSkl_98DrNFIwVnxzVVtc_jjUtPffhZD-JxESDZ4UV5w21ST2LtxrmU0lZRnNV7glrWhzNEbY5GXySY_WZ_6drTDVvtRB7ajm656053gMj7JUwkIueLlXq4oDHnUBDEbqOMbOk%3D&amp;attredirects=1">Behavioral Biometric Authentication in Human-Computer Interaction</a>, John Vincent Monaco, January 2014. Thesis.<br>
<a href="https://60cd0793-a-d5557daf-s-sites.googlegroups.com/a/vmonaco.com/vmonaco/publications/Time%20Intervals%20as%20a%20Behavioral%20Biometric.pdf?attachauth=ANoY7co-7gh7ob9-RvoWHrwnQbgTu4XGpVX-hn0QMlndQUiclYz_6KnwvcD28KLHslaTSSJeXYUYgy4u4I2eNNQ9xuSHP59NVRnSHWiAE7-vmUNc5G8XMtNDND0matshYp-hi2h5mlcwVo5jN40CQTJp1asv_x4nA8rdZJmh9zcWJdKaJu9K6BPUf65QmrUSP_JCJWDAph8QZe3Jg7Ep6fqXt-7cDxJ5gJtMlC6PhSKIxBHij41ZI9zVGRS9hoWN6DLK39icxZWF&amp;attredirects=1">TIME INTERVALS AS A BEHAVIORAL BIOMETRIC</a>, John Vincent Monaco, November 2015. Dissertation.<br>
<a href="https://60cd0793-a-d5557daf-s-sites.googlegroups.com/a/vmonaco.com/vmonaco/publications/Keystroke%20Biometric%20Systems%20for%20User%20Authentication.pdf?attachauth=ANoY7cqGjUtcMrRpGGmmtccQR7kmPWk2xUvuPAoy0tNoyGq79MG3crdrhbJ5_dCDDk7D9oLH8osRFEwkm5ofimhpEY2HX7cAGmXGbW_smwOaPIYi6PaUYEzScunU-TvONR8LPy-B6lBJ4HZHjjd1_Nxx7_yWOWRGpPORoXv8Cci1pN-_fJFMx_E-Obn9vpC6hKBQNCN1S4tX9YjGpsLmLoRil5TrZ4MuuYlXSXI27v2vq7gDJi9R-0a5syXLvphhzJ2-ksi2qAfOYa21WRVkfXvAfn8ATQIL5w%3D%3D&amp;attredirects=1">Keystroke Biometric Systems for User Authentication</a> Md Liakat Ali1 · John V. Monaco1 · Charles . Tappert · Meikang Qiu, Feb 2016.<br>
<a href="https://arxiv.org/pdf/1607.03854.pdf">The Partially Observable Hidden Markov Model and its Application to Keystroke Dynamics</a> John V. Monacoa, Charles C. Tappert, November 2017.<br>
<a href="https://60cd0793-a-d5557daf-s-sites.googlegroups.com/a/vmonaco.com/vmonaco/publications/An%20investigation%20of%20keystroke%20and%20stylometry%20traits%20for%20authenticating%20online%20test%20takers.pdf?attachauth=ANoY7crCz7YOdwWtIEGdXVzXDPURNlBHMoT4Z5ynM07Lj-W61JbxhbgZDa6Xf0nrd9KvxwPVco">An Investigation of Keystroke and Stylometry Traits for Authenticating Online Test Takers</a></p>

    </div>
  </div>
</body>

</html>
