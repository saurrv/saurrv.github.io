---
title: Don't just write lines, craft your code
layout: post
subtitle: Lessons from the book - The Pragmatic Programmer by Andrew Hunt and David Thomas.
date: '2017-10-25 23:30:00 +0530'
author: Saurabh Verma
image: img/post-bg-2017-10-25-pragmatic-programmer.jpg
---
<p>After writing hundreds of thousands of lines of code in C++ for years, I used to assume proficiency in programming. I could not have been further from truth when it comes to producing quality code. By reading "The Pragmatic Programmer" by Andrew Hunt and David Thomas, I have tried to strengthen my art. In this process, I have documented the lessons learned here so that they can be reused by a wider audience for a quick read.</p>

<b>Chapter 1: Philosophy</b>
<ul type="square">
    <li>
        <p>Don't give excuses or blames, give options instead. Things will fail, but you should know how to tackle them.</p>
    </li>
    <li>
        <p>One broken window, left unrepaired for a substantial length of time, instills in the inhabitants of the building a sense of abandonment and a don't care attitude. It sets the building for rotting. Don't live with any broken windows.</p>
    </li>
    <li>
        <p>The story of soldiers and villagers cooking stone soup. The villagers find it easier to join when they see initial success. Be a catalyst for change, show some success and then add people as a part to your success story.</p>
    </li>
    <li>
        <p>The famous frog in boiling water story. The frog is able to realize a sudden increase in temperature when kept in boiling water but not gradual heating. Remember the big picture and review what is happening around. Question whether the given change is good or bad?</p>
    </li>
    <li>
        <p>The scope and quality of the system should be specified with system requirements. You should stop iterating at some point, which is good enough.</p>
    </li>
    <li>
        <p>Your knowledge and experience are your most important professional assets. They are expiring assets. Your knowledge portfolio is similar to financial portfolio: Invest regularly, Diversify, Manage risks, buy low sell high and constantly review.</p>
    </li>
    <li>
        <p>Sample goals: Learn at least one new language a year, read a technical book a quarter, read non-tech books, take classes, engage with people, stay updated and curious.</p>
    </li>
    <li>
        <p>Search for answers and think critically about what you read to understand complex answers.</p>
    </li>
    <li>
        <p>A good idea is an orphan without effective communication. Know what to say, know your audience, choose the moment, style and presentation. Involve them, listen to them and always respond.</p>
    </li>
</ul>

<b>Chapter 2: Approach</b>
<ul type="square">
    <li>
        <p>Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.</p>
    </li>
    <li>
        <p>Duplication can be of multiple types: Imposed, Inadvertent, Impatient and Inter-developer. Do not repeat yourself. Ever.</p>
    </li>
    <li>
        <p>Make it easy to reuse.</p>
    </li>
    <li>
        <p>Orthogonality: Independence and decoupling of components. Eliminate effects between unrelated things. It increases productivity and reduces risks.</p>
    </li>
    <li>
        <p>There are no final decisions. Plan for reversibility. If you follow other guidelines, it will generally be easy to reverse.</p>
    </li>
    <li>
        <p>Tracer bullets are those bullets which trace their path in dark. Use tracer bullets to find the target. Develop an initial build of the end-to-end system and add more to reach the target. This is done when there are too many unknowns. It has many advantages: continuous progress, laid out structure, continuous iteration and more. It is different from prototyping - Prototype code is generally thrown away, and these also tell how the overall application would work with an initial structure. Tracer code is lean but complete.</p>
    </li>
    <li>
        <p>Prototyping tries out risky and uncertain elements at a reduced cost. They are not always code based, such as drawings, post-it notes etc. Prototype to learn about the particular target leaving behind the unimportant details. Let everyone know it is a disposable, incomplete prototype code.</p>
    </li>
    <li>
        <p>Program closer to the problem domain using mini-language tailored for the application. You may use tools like yacc or extend programming language to implement the above mini-language. </p>
    </li>
    <li>
        <p>Estimate to avoid surprises. Choose the unit to reflect accuracy. For estimating, ask someone in similar situation, include assumptions, calculate the answers from estimates for smaller modules. Continuously improve on your estimates. You may iterate the schedule with code.</p>
    </li>
</ul>

<b>Chapter 3: Tools</b>
<ul type="square">
    <li>
        <p>Every craftsman has a set of tools, which he has learned and adapted to over time. Build yourself a toolkit. </p>
    </li>
    <li>
        <p>Keep knowledge in plain text. It may take more memory and parsing time, but it gives increased human understandability, more tools, consistent understanding, long term benefits. At least keep metadata in plain text always.</p>
    </li>
    <li>
        <p>GUI is limited, we need to use the power of shell to do more. Learn sed, sort, find, grep, perl, awk, xargs, vi and more commands to soar your productivity.</p>
    </li>
    <li>
        <p>Use a single editor well, know it thoroughly, use it for more than you already do.</p>
    </li>
    <li>
        <p>Always use source code control - for single developer, for documentation, for system configuration, for prototypes, for scripts, for procedures and what not.</p>
    </li>
    <li>
        <p>Fix the problem, not the blame. Debugging is just a problem and attack it as such. </p>
    </li>
    <li>
        <p>Don't panic. Check for warnings, what exactly happened, visualize the data, trace down the cause using print statements, eliminate causes, maybe using binary search and prove that that module works. You may need to explain your code as if explaining to a fellow.</p>
    </li>
    <li>
        <p>Learn text manipulation to quickly do short tasks, experiments and more. The author lists a big set of examples he did with Perl.</p>
    </li>
    <li>
        <p>Write code that generates code, maybe passive - ran once to save manual work and time or active - constantly parsed and rewritten, for example, thrift. Keep the input format simple.</p>
    </li>
</ul>

<b>Chapter 4: Paranoia</b>
<ul type="square">
    <li>
        <p>You can't write perfect software. Defend against yourself.</p>
    </li>
    <li>
        <p>Design by contracts: Document the rights and responsibilities of software modules to ensure program correctness. If all the preconditions are met by the caller, the routine shall guarantee all postconditions and invariants on completion. Liskov Substitution principle: Subclasses must be usable through the base class interface without the need for user to know the difference. This pushes us to think about contract (boundaries, functionalities etc.) at the design phase.</p>
    </li>
    <li>
        <p>Crash early. A dead program does less damage compared to a wrong one. On unexpected, we crash.</p>
    </li>
    <li>
        <p>If it can't happen, use assertions to ensure that it won't. Don't do error handling with this. Leave them turned on in production.</p>
    </li>
    <li>
        <p>Use exceptions to handle exceptions - unexpected events, not errors. This is so because exceptions cause an immediate transfer of control.</p>
    </li>
    <li>
        <p>Finish what you start. Whoever allocates a resource is responsible for deallocating it. Deallocate resources in opposite order of allocating them. In separate processes, allocate resources in same order to avoid deadlock. Remember to deallocate in case of exceptions. C++ provides auto_ptr to automatically provide a wrapper over a pointer object, Java provides finally. Use a semantic invariant for memory allocation and deallocation. Use code and tools to ensure no memory leaks happen.</p>
    </li>
</ul>

<b>Chapter 5: Adaptable Programs</b>
<ul type="square">
    <li>
        <p>Divide your code into cells (modules) such that current cell does not care about other cells. Law of Demeter suggest to call methods of itself, parameters, objects held and created. It may create too many wrappers in case of critical applications.</p>
    </li>
    <li>
        <p>Metaprogramming: Get the details out of code. Configure, do not integrate algorithms, databases, middle-ware, UI etc. Put abstractions in code, details in metadata. The author emphasizes this using Java beans.</p>
    </li>
    <li>
        <p>Minimize temporal dependencies and maximize concurrency. Use services for designing independent components. Always design for concurrency -  It will give you clean, scalable, robust code.</p>
    </li>
    <li>
        <p>When we modularize, message passing becomes crucial and Publish-Subscribe pattern becomes important. The author then uses MVC pattern to describe decoupling between independent pieces and later carries it for general system design.</p>
    </li>
    <li>
        <p>Use a consistent visual interface synonymous to blackboard for large and complex problems. Some online blackboards are - JavaSpaces, T Spaces etc. It is a good idea where different people are gathering data.</p>
    </li>
</ul>

<b>Chapter 6: Coding</b>
<ul type="square">
    <li>
        <p>Don't program by coincidence. Know what are you doing, rely on reliable things, document as much as you can, write good tests, spend time on hard parts and don't be constrained by existing code.</p>
    </li>
    <li>
        <p>Estimate time and space of your algorithm, theoretically and practically, and test it. Use code profilers if needed. The best is not always the best.</p>
    </li>
    <li>
        <p>Refactor early, refactor often. Take short steps and test continuously.</p>
    </li>
    <li>
        <p>Software should be treated like IC, thus, include testing behavior in itself. Test against contract. Emphasize on importance of writing tests. Test your software, or your users will.</p>
    </li>
    <li>
        <p>Use code wizards, but not the wizard code you don't understand.</p>
    </li>
</ul>

<b>Chapter 7: Requirements Analysis</b>
<ul type="square">
    <li>
        <p>A requirement is a statement that needs to be accomplished. Dig for them. Don't specify changing policies into requirements. Document your requirements in a contract in a suggested format like UML. Specify, but do not overspecify, since abstractions will live longer than details. Track changes in requirements. Use a glossary for consistency in understanding.</p>
    </li>
    <li>
        <p>To solve the hardest problems, find the bounding box, the set of constraints exactly and work only on them. Don't dismiss foolish-sounding solutions because of misleading constraints.</p>
    </li>
    <li>
        <p>Start when you are ready, respect your intuition, but do not procrastinate.</p>
    </li>
    <li>
        <p>Don't be slave to formal methods, use them when needed. They have limitations and adopting costs. Continuously improve your methods.</p>
    </li>
</ul>

<b>Chapter 8: Beyond Individual</b>
<ul type="square">
    <li>
        <p>Apply these lessons individually and in the team. Divide teams into functionalities, not duties. It will create orthogonal teams. </p>
    </li>
    <li>
        <p>Any recurring task has to be automated. This includes build, test, compilation, code generation, bootstrap, maintenance, alerts, permissions, review etc. Let the computer do the boring job.</p>
    </li>
    <li>
        <p>Test early. Test often. Test automatically. Coding ends when tests run. We need unit tests, integration tests, validation tests, resource exhaustion tests, performance tests, usability tests and more. Use regression, test data, tests for tests (saboteurs), state coverage. Find bugs once, then test against them.</p>
    </li>
    <li>
        <p>Ink is better than memory. Write comments for why, not how. Use good names, and do not mislead. Keep documentation on the web. Documentation is also a first-class citizen. Documentation is another view, develop it automatically using technology.</p>
    </li>
    <li>
        <p>The success of a project is measured by how well it meets the users' expectations. Manage their expectations with proper communication and gently exceed by that little bit extra in delivery.</p>
    </li>
    <li>
        <p>Sign your work and be proud of it. Do not defend it furiously. Own it.</p>
    </li>
</ul>

<p>I am anxious to know what you think of this piece, the content, the expressions and more. For giving it back, you should reach me <a href="{{ site.baseurl }}/contact/">here</a>. Programming is an art, and I want to help you hone it. Cheers!</p>
