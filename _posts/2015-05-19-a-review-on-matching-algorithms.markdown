---
layout:     post
title:      "A Review on Matching Algorithms"
subtitle:   "Mechanism Design and Market Institutions"
date:       2015-05-19
author:     "Yuhao Zhu"
header-img: "img/post_head_pic_js.jpg"
tags:
    - Economics
---

<a href="{{site.url}}/doc/posts/review_on_matching_algorithms.pdf" target="_blank">Click here for the complete PDF document</a>, where the formulae and functions are better displayed.

Abstract
============

Matching is one of the basic functions of the market. It decides the
allocation of the resources among people. Among all matching problems,
one class is rather interesting, namely school matching. The way of
matching decides who can be admitted to school, and which school a
student will finally enter. Because school matching has profound and
long-lasting influence on students, parents and the society, studying
the properties of different matching mechanism and choosing the most
suitable one are objectives of economists.

In this essay, I first describe the school matching problem, state the
purpose of researches on this topic, and discuss some criteria on
matching mechanism. Then I present several matching mechanisms and their
theoretical properties. After that, I give some discussion on
application and experimental results of these school matching mechanism.
Finally, concluding remarks will be given.

Introduction
============

School matching problem
-----------------------

The school matching problem concerns two set of agents, schools
(colleges) and students (applicants). It was initially introduced by
[@gale1962college] as the following situation: A school (college) has
$n$ applicants and can only accepts at most $q$. The school, after
evaluating the applicants, need to send out offers to some of the
applicants. The problem is that not all applicants who receive offer
would reply to it. Therefore, the school needs to send more than $q$
offers to students in order to receive approximately $q$ acceptance.

This procedure generate too much guesswork because the school do not
know whether the students apply other schools, what are the preferences
of the students, and what are the preferences of other schools.
Therefore, the actual admission number can only be around desired $q$.

Difficulty are not only for colleges, but for students as well. They
need to decide whether to respond to the current offer, or to wait for a
preferred one. Since there are possibility of being declined by the
preferred school, an applicant may make a sup-optimal decision.

The purpose of studying schooling matching problem is to overcome
difficulties for both schools and students. A matching mechanism is
aimed to provide an match between students and schools, i.e., who can go
to school and which school she goes based on, ideally, true preferences
of both parties. It should eliminate or minimize guesswork of both side,
such that both side will achieve satisfactory result. It should also
take into consideration the social efficiency and fairness.

Model description
-----------------

Here I first give a formal model of school matching problem. There are
two groups of individuals, $m$ colleges (school) and $n$ students
(applicants), denoted by $C=\{c_1,c_2\ldots c_m\}$ and
$S=\{s_1,s_2\ldots,s_n\}$ respectively. School $i$ has a quota $q_i$,
i.e., at most $q_i$ students can be accepted. It is a two-sided
matching, and, therefore, the agents of two groups do not overlap.
Assume that the number of students is abundant enough for colleges to
meet their quotas, i.e., $\sum^m_{i=1} q_i \leq n$.

The individuals in each side has a complete and transitive preferences
over the individuals of the other sides. That is to say that, each
college rank the students, while each student also rank the colleges.
For example, the preference of college $c_1$ can be denoted as
$P(c_1)=s_1,s_2,\ldots, s_k, c_1$. Here $c_1$ means that the college 1
would rather waste its quota than accept students ranked after itself.
These unqualified students are omitted from the preference list of
college $c_1$. Initially, we assume that the preferences are private
information.[^1]

For simplicity, I also assume that the preference are strict. If there
is indifference in preference, the ties can be broken arbitrarily. For
example, if a college is indifferent between two students, he can
randomly rank these two students.

Moreover, if we set the quota $q$ equal to 1 for each college, the
students and the colleges are actually symmetric. It is a special case
of schooling matching called “marriage model”, and it is also the
starting point of the analysis of [@gale1962college].

Two examples
------------

Here I provide two simple examples of schooling matching problem. They
will help us in later chapters understand theoretical properties of
different matching mechanisms.

\[example1\]

There are two colleges $C=\{c_1,c_2\}$ and three students
$S=\{s_1,s_2,s_3\}$. Each school only admits 1 student, $q=1$.

The Preferences of colleges are 
$$\begin{aligned}
&P(c_1)=s_1,s_2,s_3\\
&P(c_2)=s_3,s_1,c_2\end{aligned}$$

The preferences of students are 
$$\begin{aligned}
&P(s_1)=c_2,c_1\\
&P(s_2)=c_1,s_2\\
&P(s_3)=c_1,c_2\end{aligned}$$

\[[@gale1962college]\]\[example2\]

There are three colleges $C=\{c_1,c_2,c_3\}$ and three students
$S=\{s_1,s_2,s_3\}$. Each school only admits 1 student, $q=1$.

The Preferences of colleges are 
$$\begin{aligned}
&P(c_1)=s_1,s_2,s_3\\
&P(c_2)=s_2,s_3,s_1\\
&P(c_3)=s_3,s_1,s_2\end{aligned}$$

The preferences of students are 
$$\begin{aligned}
&P(s_1)=c_2,c_3,c_1\\
&P(s_2)=c_3,c_1,c_2\\
&P(s_3)=c_1,c_2,c_3\end{aligned}$$

Criteria
--------

There are many mechanisms for matching schools and students. Each of
them have certain properties and can fulfill certain purposes. Some of
properties might be desirable. Therefore, we need to establish several
criteria for matching procedures. [@roth1982economics] pointed out that
any matching procedure depending on preference can be seen as two parts.
One part is a mechanism to reveal the preferences of all agents, and the
other part is to determine the outcome depending on the preferences
revealed. If preferences are not truly revealed, resulting outcomes from
stated preferences cannot process certain desirable properties with
respect to true preferences. Therefore, the first criteria concerns
incentive compatibility.

\[Strategy-proofness, incentive compatibility\] An assignment is
strategy-proof if all agents prefer to reveal their true preferences. If
only one side of the agents prefer to tell the truth, it is one-sided
strategy-proof.

Another criterion is the stability of matching. It eliminate the
possibility that a pair of agents form a coalition and deviate the
matching outcome.

\[Stability [@gale1962college]\] An assignment is unstable if there are
two students $s_1$ and $s_2$ who are assigned to colleges $c_1$ and
$c_2$. However, $s_1$ prefers $c_2$ to $c_1$ and $c_2$ prefers $s_1$ to
$s_2$. Then, a transfer will improve the total benefits.

Stability can also be regarded as fairness, namely no justified envy
[@kojima2010axioms]. It means that there is no case in which student
$s_1$ is matched to $c_1$ but prefer $c_2$, but $c_2$ accepts $s_2$ who
ranks $c_2$ lower than $s_1$ does. When matching outcome is not
compelled among all agents, stability is also a desirable criterion to
prevent possible coalition.

The next criterion comes from social perspective. That is, whether the
matching outcome is Pareto efficient.

\[Pareto efficiency [@roth1985college]\] Some agents can improve their
benefits while keeping others at least as good as current status.

Mechanisms and theoretical properties
=====================================

Deferred acceptance mechanism
-----------------------------

Although college matching is a very important and common function of
educational market, the economic theories of schooling matching was not
systematically established by economists until 1962 when Shapley and
Gale published their leading paper “College Admissions and the Stability
of Marriage”. In this paper, [@gale1962college] proposed the deferred
acceptance mechanism for marriage matching and school matching. It
requires all agents to state their preferences.

The analysis starts from the special case when $q=1$. The algorithm has
following steps.

Step 1: Individuals of one side, say students, make proposals to his
favorite college. Each college who receives more than one proposals
rejects all but its favorite students among all those who proposes to
it. The school hold its favorite student on a string without immediately
accept her.

Step 2: The students who were rejected in the step 1 can now propose to
their second favorite school. After receiving the new proposals, the
school chooses the favorite student from those who proposes in step 2
and the student on the string from step 1. This student will be put in
the list, while other students are rejected.

In general at

Step $k$: The students who were rejected in step k-1 proposed to the
last college in the preference lists. There are acceptance and
rejection. Since a student cannot propose to the same college twice, the
algorithm stops. The schools provides offer to the students on the
string.

To see how this algorithm works, let us refer to **Example 1**. I use
school proposing deferred acceptance algorithm here to find a match. In
the first step, $s_1$ proposes to $c_2$, $s_2$ proposes to $c_1$, and
$s_3$ proposes to $c_1$. $c_1$ holds $s_2$ on the string and rejects
$s_3$, and $c_2$ holds $s_1$ on the string.

In the second step, $s_3$ proposes to $c_2$. $c_2$ holds $s_3$ on the
string and rejects $s_1$.

In the third step, $s_1$ proposes to $c_1$, and $c_1$ hold $s_1$ on the
string while it rejects $s_2$.

The algorithm terminates, and the schools accept the students on the
string. The final match is
$\mu=\{(c_1,s_1),(c_2,s_3),(\emptyset,s_2)\}$.

Now let us move on to see whether DA algorithms features certain
criteria.

\[[@gale1962college]\] There always exists a stable set of matching.
Resulting outcome produced by adopting deferred acceptance algorithm is
stable.

The proof of the theorem is simple. If $c_1$ and $s_1$ are not matched,
but $s_1$ prefer $c_1$ to her own school. Then, $s_1$ must have proposed
to $c_1$ at some steps before and was rejected by $c_1$ because $c_1$
prefers another student. In this way, we say the $c_1$ must prefer its
matched student more than $s_1$. Thus, the deferred acceptance mechanism
can eliminate instability.

Notably, [@gale1962college] also showed that the stable matching
generated by deferred acceptance algorithm is one-sided optimal.

\[Optimal [@gale1962college]\] An assignment is optimal if every
applicant is at least as well off under any other stable assignment.

\[[@gale1962college], [@roth2008deferred]\] The matching produced by the
deferred acceptance algorithm with one side proposing is the optimal
stable matching for this side, i.e., every individual from proposing
side likes this matching at least as well as other stable matching.

This theorem indicates that the deferred acceptance algorithm favors the
group of people who make a proposal. Let us see **Example 2**. There are
three stable match:

The first matching outcome results from students proposing:
$\mu_1=\{(c_1,s_3),(c_2,s_1),(c_3,s_2)\}$.

The second matching outcome results from colleges proposing:
$\mu_2=\{(c_1,s_1),(c_2,s_2),(c_3,s_3)\}$.

The third matching outcome is also stable:
$\mu_3\{(c_1,s_2),(c_2,s_3),(c_3,s_1)\}$.

We can see that the proposers are at least as well off under any other
stable assignment using deferred acceptance algorithm. $\mu_1$ is
student-optimal stable matching, and $\mu_2$ is school-optimal stable
matching.

Gale and Shapley then extend 1-to-1 matching problem to many-to-1
matching problem, which is straightforward. Assume now the quotas of
colleges, $q$, can be more than 1. We consider student proposing. The
steps are as follows:

Step 1: Each students proposes to his favorite college. College $i$
keeps the first $q_i$ applicants on the waiting (if there are less than
$q_i$ students proposing to it, keep them all), and then rejects the
others.

Step 2: The students who were rejected in the step 1 can now propose to
their second favorite school. After receiving the new proposals, the
college $c_i$ chooses the favorite $q_i$ student from those who proposes
in step 2 and the student on the waiting list from step 1. These student
will be on the waiting list, while other students are rejected.

In general at

Step $k$: The students who were rejected in step $k-1$ proposed to the
last college in the preference lists. There are acceptance and
rejection. Since a student cannot propose to the same college twice, the
algorithm stops. The schools provides offer to the students on the
waiting list.

Later literature continued to investigate other properties of deferred
acceptance mechanism. First of all, they want to see whether the DA
algorithm is incentive compatible.

\[[@roth1982economics]\] No stable matching procedure for the general
matching problem exists for which truthful revelation of preference is a
dominant strategy for all agents.

This theorem indicates that no matching procedure can generate both
stable outcome and incentive compatible outcome. It directly means that
deferred acceptance algorithm is not strategy-proof. See **Example 2**
and consider students proposing. If, say, college 1 truncates its
preference by reporting $P'(c_1)=s_1$. After 7 steps of iteration, the
student-optimal stable matching under reported preferences is
$\mu'_S=\{(c_1,s_1),(c_2,s_2),(c_3,s_3)\}$. The colleges are strictly
better off by reporting fake preferences.

However, literature showed that truth-telling can still be dominant
strategies for one side of the agents.

\[[@dubins1981machiavelli], [@roth1982economics], [@roth1985college]\]
It is a dominant strategy for each student to state his true preference
when deferred acceptance algorithm is used and when students make
proposers. In another words, the student-optimal stable matching is
strategy-proof.

This theorem sheds some light in application when preferences of schools
are predetermined by announced rules. In this case, preferences of
schools are actually publicly known. They will not behave strategically.
The student-optimal stable matching is thus strategy-proof for all
agents.

Literature also examined the another criterion, namely Pareto
efficiency.

\[Weakly Pareto efficiency[@roth2008deferred]\] A matching $\mu$ is
weakly pareto efficient for all students if there is no matching,
including unstable ones, that all students strictly prefer it to $\mu$.

\[[@roth1982economics]\] The student-optimal matching is weakly Pareto
optimal for all students. However, it is not strongly Pareto optimal for
all students.

Return to **Example 1**. The stable matching
$\mu=\{(c_1,s_1),(c_2,s_3),(\emptyset,s_2)\}$ is dominated by an
unstable matching $\mu'=\{(c_1,s_3),(c_2,s_1),(\emptyset,s_2)\}$ from
the perspective of student side even though $\mu'$ is not stable, since
$s_1$ and $s_3$ achieved their first choices while $s_2$ was not worse
off.

Boston mechanism
----------------

Forty years after the deferred acceptance mechanism is proposed by Gale
and Shapley, [@abdulkadiroglu2003school] in their AER paper discusses
another mechanism, Boston mechanism. In this mechanism, students are
required to submit their private preference to educational center. The
priorities of schools are determined by announced hierarchies, and thus
their quotas and preferences can be regarded as public information. The
mechanism goes as follows[^2].

Step 1: Each student proposes to the school she lists as her first
choice. Each school accepts its applicants according to its preference
until the quota is completely used. The remaining students are rejected.

Step 2: Those who are rejected in the step 1 proposes to the school they
list as their second choice. Each school accepts its applicants
according to its preference until the remaining quota is fully used.

In general at Step $k$: Those who are rejected in the step $k-1$
proposes to the school they list as their (k-1)th choice. Each school
accepts its applicants according to its preference until the remaining
quota is fully used.

The mechanism terminates either when there is no quota any more, or no
students are rejected in this step.

The difference between the deferred acceptance mechanism and Boston
mechanism lies in that the latter one does not never put any students on
waiting lists, i.e., proposers in this step will not be compared to
students in the waiting lists of last step.

See **Example 1**. There is only one step before matching is done if
Boston mechanism is adopted. In this step, $s_1$ proposes to $c_2$,
$s_2$ and $s_3$ proposes to $c_1$. Only $s_3$ is rejected. The resulting
matching is $\mu=\{(c_1,s_2),(c_2,s_1),(\emptyset,s_3)\}$

This mechanism has following properties.

\[[@abdulkadiroglu2003school]\] Boston mechanism is not strategy-proof.

It is easy to see from **Example 1** that even if student $s_3$ ranked
first in school $c_2$, she might still lose priority if he does not list
school $c_2$ as her first choice. Thus, students and their parents might
fake their true preferences, and improve the ranking of schools that
give them high priority.

Moreover, Boston mechanism, theoretically, is neither stable nor Pareto
efficient.

\[[@abdulkadiroglu2003school]\] Boston mechanism is not stable.

\[[@abdulkadiroglu2003school]\] Boston mechanism is Pareto efficient if
students present their true preferences. It is not Pareto efficient if
students misrepresent their preferences.

Top trading cycles mechanism
----------------------------

In 1974, [@shapley1974cores] introduced “top trading cycle” to find the
competitive prices in the market. This concept was extended to school
matching context by [@abdulkadiroglu2003school]. In this paper, the
authors mentioned another matching procedure, namely top trading cycles
mechanism. Given preferences of both sides, students are matched to
schools with the following algorithm.

Step 1: Each student points to its announced favorite school, and each
school points to its announced favorite student. This will generate at
least a cycle. For example, $(s_1,c_1,s_2,c_3,\ldots,c_k)$, in which
student $s_1$ points to college $c_1$, $c_1$ points to student $s_2$,
and so on, until $c_k$ points to $s_1$. Every student in the cycle is
assigned to the school she points to.

In general at Step k: The rest students and colleges with quota continue
to form cycles. Every student in the cycle is assigned to the school she
points to.

The algorithm stops when no cycle can be formed.

Considering **Example 1**, in step 1, $s_1$ points to $c_2$, $c_2$
points to $s_3$, $s_3$ points to $c_1$, and $c_1$ points to $s_1$. There
is a cycle and then $s_1$ is assigned to $c_2$ and $s_3$ is assigned to
$c_1$. The resulting matching is
$\mu=\{(c_1,s_3),(c_2,s_1),(\emptyset,s_2)\}$.

The top trading cycles mechanism has some different properties from
deferred acceptance mechanism. These properties can also be seen from
the resulting matching for **Example 1**.

First of all, other than DA algorithm, top trading cycles mechanism is
Pareto efficient.

\[[@abdulkadiroglu2003school]\] Top trading cycles mechanism is Pareto
efficient with preferences of schools predetermined.

Second, like DA algorithm, top trading cycles mechanism is
strategy-proof.

\[[@abdulkadiroglu2003school]\] Top trading cycles mechanism is
strategy-proof with preferences of schools predetermined.

However, top trading cycles mechanism produces unstable result.

\[[@abdulkadiroglu2003school]\] Top trading cycles mechanism is
unstable.

Application and Experimental results
====================================

Application
-----------

### Deferred acceptance mechanism for clearinghouses

Although deferred acceptance mechanism is introduced in 1962, similar
ideas were adopted well before it. [@roth2008have] discussed the first
application of the thought of deferred acceptance (DA) algorithm in
doctor market[^3].

The first jobs of newly-graduated doctors have great influence on their
future careers. The jobs are also a great part of labor forces of
hospital. In order to compete for graduates, hospitals tried to hire
doctor students as early as possible. This resulted in the phenomenon
that students were hired almost two years before they would graduate
from medical school.

In order to cure this market failure, in 1945, American medical school
agreed to not release students’ information until certain date. This
caused another problem that hospitals requested their candidates to
reply the offers immediately, before the students receive about other
offers. The shortened response time also caused chaos in the market.

In 1951, a centralized clearinghouse was adopted to coordinate the
market, which is called National Resident Matching Program (NRMP) now.
It requires both hospitals and graduates to submit their preferences,
and uses an algorithm to produce a matching. [@roth1984evolution] showed
that this matching mechanism can result a hospital-optimal stable
matching in the sense introduced by [@gale1962college].

Although the DA algorithm solved market failure in hospital-doctor
matching, but, however, there are new challenges to this mechanism. One
of them is that a growing number of married couples wish to be assigned
to the same hospital. [@roth1984evolution] showed that stable matching
cannot be made in this situation. This caused high-qualified couples
reluctant to participate the clearinghouse. Another issue is that the
NRMP results in hospital-optimal stable matching, which pays little
attention to the interest of the graduates.

Therefore, Roth was invited in 1995 to redesign the matching mechanism,
and in 1999, [@roth1999] provided a new algorithm to always produce
stable matching when there are couples. The new algorithm was
consequently used by other labor market clearinghouses.

### Boston public school matching

The Boston mechanism was initially used by educational administration to
allocate students to public schools. The problem of this system, as
stated above, is that it is not safe for students and parents to state
their true preferences. They might misrepresent their preferences and
improve the ranking of schools which also give them higher priority. As
recommended in the 2004-2005 BPS School Guide, “for a better choice of
your ’first choice’ school, consider choosing less popular schools.”

In 2005, [@abdulkadirouglu2005boston] proposed two alternative
mechanisms. One is deferred acceptance algorithm, and another one is top
trading cycles mechanism. Because the schools’ priority over students
are not decided by schools but by the educational administration, there
is no strategic issues for schools. Meanwhile, DA algorithm with
student-proposing also ensure truth-telling. Therefore, both mechanism
are strategy-proof. The choice between DA algorithm and TTC mechanism is
just a trade-off between stability (fairness) and Pareto-efficiency on
the student side.

Under the recommendation of Roth and his colleagues, the Boston school
committee finally adopted the deferred acceptance algorithm with student
proposing [@roth2008have].

### New York school matching

The old system for school matching in New York is decentralized. Each
student submits a preference list of 5 schools. The lists are sent to
schools. The schools decide independently who they will accept and send
out offer letters. Students reply to the offers after receiving mails.
Then, school with empty seats send out offers for the second round. This
procedure lasts for three round. Those who are not accepted by any
school will be assigned to their zoned schools [@roth2008have].

This system generated a problem which is quite similar to what I
described in introduction. There is too much guesswork and uncertainty
for both schools and students. About 1,700 students received multiple
offers and about 3,000 students received nothing.

Schooling matching problem in New York is different from that in Boston.
It is because in New York, preferences of schools are not determined by
authorities. Preferences over students are private information for
schools, and schools can behave strategically. The analysis is more
complicated than the Boston case.

Naturally, student proposing DA algorithm becomes a desirable mechanism
for several reasons. First, student proposing DA algorithm provides
student-optimal stable matching. It is envy-free and it cares more about
the interest of students. Second, student proposing DA algorithm is
strategy-proof for students. Third, [@roth1999redesign] and
[@kojima2009incentives] showed that when the market is large, the
proportion of colleges that misrepresent their preferences in student
proposing DA algorithm converges to zero. It means the algorithm is
almost strategy-proof for schools.

[@roth2008have] mentioned that after the New York City adopted this new
school matching mechanism, the problem was solved. Only about 3,000
students did not receive offers. The submitted preferences also became
more truthful.

Experimental results
====================

In this chapter I will present two laboratory experiments that test the
theoretical predictions of matching mechanisms.

The experiment carried out by [@chen2006school] compares DA algorithm,
TTC mechanism and Boston mechanism with criteria mentioned in
introduction.

First, concerning strategy proof, Boston mechanism results in the least
truth-telling, compared to other two mechanism. Top trading cycles
mechanism results in weakly less truth-telling than DA algorithm. The
authors showed that 70.8% of the participants got their reported first
choice but only 28.5% of them got their true top choices. This indicates
that applicants tends to improving the ranking of schools that give them
high priority under Boston mechanism.

Second, concerning efficiency, DA algorithm always performs better than
top trading cycles mechanism. Boston mechanism performs worse than TTC
mechanism in the designed environment, but performs as well as DA
algorithm in the random environment[^4].

The main results of the experiment suggest that DA algorithm is better
than the others.

[@pais2008school] also carried out experiments to compare these three
mechanisms when participants have different level of information.
Different from what was found by [@chen2006school], they showed that TTC
mechanism outperform DA algorithm in both truth-telling and efficiency,
while DA algorithm does not show too much superiority over TTC mechanism
in stability.

Their main results indicate, on the contrary, that TTC mechanism is
superior over the other two.

These two experiments confirmed the theoretical predictions that Boston
mechanism is the worst mechanism among the three in term of
truth-telling, efficiency and stability. However, the experiments do not
reach a agreement whether DA algorithm or TTC mechanism is better.
Moreover, although theories predict that TTC mechanism outperforms DA
algorithm in efficiency, the experimental results of [@chen2006school]
do not show this superiority.

Concluding remarks
==================

School matching is an important issue. The matching may have profound
influence on the future of the students, their family and society.
Therefore, the study of different matching mechanism, as well as
improving them towards desirable criteria, is what economists should do.

Current literature mainly focus on three criteria of matching mechanism.
First, it should give students incentive to state their true preference.
Second, it should be efficient on the student side. Third, it should
eliminate or minimize unfairness. Given these criteria, two mechanisms
are superior over others, namely student proposing deferred acceptance
algorithm and top trading cycles mechanism.

Although theoretically DA algorithm results in more stable matching than
TTC mechanism and the latter results in more efficient matching, current
empirical results does not reach an agreement which one is better.
Therefore, both DA algorithm and TTC mechanism be regarded as two best
alternatives in school matching.

One more lesson we should also learn from the empirical application of
these mechanisms is that there is never a “best” school matching
mechanism. As time passes by, new problem rises and new criteria need to
be taken into consideration. For example, DA algorithm successfully
solved the market chaos for hospital-doctor matching in 1950th, but,
however, it was challenged by growing number of married doctors.
Therefore, new matching mechanisms need to be continuously explored to
fulfill new social goals.

Future researchers can contribute to existing literature on school
matching in following ways.

First, more matching mechanism currently in use can be studied. This
should not be restricted in the US. What are the advantages and
disadvantages of these mechanisms? What are the potential improvements?
It is also important to take in to account the social and cultural
background when doing analysis.

Consequently, second, other criteria for school matching mechanisms can
be explored. These criteria may reflect the different social goals from
era to era, and from culture to culture.

Third, the axiomatization of school matching problem can be considered.
Do certain criteria uniquely determine the matching mechanism? It will
be easy for educational authorities to select most the suitable matching
mechanism if this axiomatization is done.

[^1]: However, it is worthy pointing out that the preferences (priority)
    of public schools might be determined by announced rules, and thus
    preferences of schools can be regarded as public knowledge. This
    setting can affect the properties of mechanisms.

[^2]: I rephrased the mechanism to make it more comparable to deferred
    acceptance mechanism.

[^3]: I include this example here because hospital matching problem is
    quite similar to a school matching problem to some extents.

[^4]: In the designed environment, schools are assigned different
    characteristics to make them more realistic, and students’
    preferences over schools are adjusted with these characteristics. On
    the contrary, in the random environment, the payoff of attending
    each schools are only random integers
