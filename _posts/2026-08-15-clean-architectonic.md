---
title: "Clean Architectonic: A Conversation"
description: "A dialogue between philosophy and software architecture."
---

> *“...so daß die Antinomie der reinen Vernunft, die in ihrer Dialektik offenbar wird, in der Tat die wohltätigste Verirrung ist, in die die menschliche Vernunft je hat geraten können, indem sie uns zuletzt antreibt, den Schlüssel zu suchen, aus diesem Labyrinthe herauszukommen.”*
>
> — Immanuel Kant, *Kritik der praktischen Vernunft* (1788, AA 5:107)

## Architectonic

> “By the term architectonic I mean the art of systems [translation, C.D.].”[^pdf-note-01]

It might be tempting to start the discussion by positively conjecturing what Kant wanted to say by this statement. But maybe it’s a good idea to firstly frame conjectures of this kind by pointing out what he clearly does *not* say here.

Kant does *not* ...

1. ...use the name “architecture” for what he defines, but “architectonic”.
2. ...talk about a specific system, but about systems *as such*.
3. ...talk about given, already created systems, which can be reviewed, but about the *art of constructing* them.

### On 1

What Kant aims for seems to be some kind of definition, a definition of “architectonic” in this case. The name could have been “architecture”, which might sound more familiar, but Kant went for another one. Independent of how intentionally this decision was made, it forbids us to equate Kant’s definition of “architectonic” with the one of “architecture”, unless we have some evidence that he considered both names as synonyms. If we haven’t such, this designation seems to convey that “the art of systems” is not what “architecture” means, it’s the meaning of “architectonic” instead. This doesn’t exclude any relations between those two terms. Maybe the meaning of “architecture” includes the one of “architectonic” or vice versa. It’s just that Kant opens up for those possibilities but ensures, by the same token, that if you want to comply with his system *for sure*, you better call the art of systems not “architecture” but “architectonic”.

We shall come back to this point later in order to discuss if the title of the “Clean Architecture” book should, according to the Kantian nomenclature, rather be “Clean Architectonic”.

### On 2

That the definition refers to “systems”, not *a* system, indicates that the subject of the respective art is not a specific kind of system, like a biologic or physical system, it’s a about what makes a system a system.

> “By a system I mean the unity of various cognitions under one idea. This idea is the conception—given by reason—of the form of a whole, in so far as the conception determines a priori not only the limits of its content, but the place which each of its parts is to occupy.”[^pdf-note-02]

Thus a system for Kant is what unifies a variety by an idea. This idea does not only define what belongs to the system but also where its respective parts belong to. It both comprises and locates the system parts rigorously, “so that the absence of any part can be immediately detected from our knowledge of the rest”[^pdf-note-03]. What constitutes this general idea? It “contains, [...] the end and the form of the whole which is congruent with that end [translation, C.D.]”[^pdf-note-04]. Hence, according to Kant, the idea of every system is purposive in nature[^pdf-note-05]. The purpose is to make the system a whole.

Thus, in the architonic perspective, the emphasis lies on the wholeness of a system and not on how to make it work in this or that particular empirical respect. Problems of the latter kind Kant distinguishes from archtitectonical as merely technical ones.

> “We require, for the execution of the idea of a system, a *schema*, that is, a content and an arrangement of parts determined a priori by the principle which the aim of the system prescribes. A schema which is not projected in accordance with an idea, that is, from the standpoint of the highest aim of reason, but merely empirically, in accordance with accidental aims and purposes (the number of which cannot be predetermined), can give us nothing more than *technical* unity. But the schema which is originated from an idea (in which case reason presents us with aims a priori, and does not look for them to experience), forms the basis of *architectonical* unity. A science, in the proper acceptation of that term, cannot be formed technically, that is, from observation of the similarity existing between different objects, and the purely contingent use we make of our knowledge in concreto with reference to all kinds of arbitrary external aims; its constitution must be framed on architectonical principles, that is, its parts must be shown to possess an essential affinity, and be capable of being deduced from one supreme and internal aim or end.”[^pdf-note-06]

Let’s use an example inorder to make sense out of this passage. Say, you want to build a house and you try to construct the system of it. Any thought you have to spend on the bricks and stones would be considered as merely technical in Kantian terms because it relies on the “observation of the similarity existing between different objects”[^pdf-note-07], e.g. bricks and stones have a certain mass, therefore you have to construct the system in a way that respects their gravity. You cannot arrange them in the “house-system” as levitating around without restraint. So this consideration targets at the arrangement of the whole without targeting at the *whole as such*.

In constrast, any consideration which does not derive from observable properties like this, but “from one supreme and internal aim or end”, which makes the system a whole, maybe the purpose of dwelling in this case (if it’s not already too much “in concreto”), Kant would probably accept as architectonic. For him constitutive principles guide the architectonical viewpoint in order to show the “essential affinity” of the system parts. Affinity belongs to the principles of reason which, according to Kant, guide our understanding[^pdf-note-08]. That is, roughly spoken, those principles which frame our experience of things.

> “Reason thus prepares the sphere of the understanding for the operations of this faculty: 1. By the principle of the *homogeneity* of the diverse in higher genera; 2. By the principle of the *variety* of the homogeneous in lower species; and, to complete the systematic unity, it adds, 3. A law of the *affinity* of all conceptions which prescribes a continuous transition from one species to every other by the gradual increase of diversity.”[^pdf-note-09]

When you read this passage before the one on architectonic the principles may appear rather abstract. But applied to the architectonical context they seem to be quite clearly illustrated. Since Kant views systems as consisting of parts. You need to concecptualize parts. For that a part can be *a* part Kant assumes the requirement of a principle which makes it the same, the principle of *homogeneity*. Now, would it make sense that a system consists only of a single part? If we deny that we’re in need of a further principle which makes that a part is not another part. However with only those two principles at disposal one would be left with lots of different things where each one is a part. But the part of *what*? The answer to this remaining question is given by the principle of affinity in the end. It organizes the parts by organizing how they are same and different following a “gradual increase of diversity”.

The principle of affinity “unites both the former [the principles of homogeneity and variety, C.D.], by enouncing the fact of homogeneity as existing even in the most various diversity, by means of the gradual transition from one species to another. Thus it indicates a relationship between the different branches or species, in so far as they all spring from the same stem”[^pdf-note-10].

So the parts are related by respects of their sameness and difference ranging from the “same stem” to the most diversified species. Would you also provide us with some kind of illustration Mr. Kant?

> “We may illustrate the systematic unity produced by the three logical principles in the following manner. Every conception may be regarded as a point, which, as the standpoint of a spectator, has a certain horizon, which may be said to enclose a number of things that may be viewed, so to speak, from that centre. Within this horizon there must be an infinite number of other points, each of which has its own horizon, smaller and more circumscribed; in other words, every species contains sub-species, according to the principle of specification, and the logical horizon consists of smaller horizons (subspecies), but not of points (individuals), which possess no extent. But different horizons or genera, which include under them so many conceptions, may have one common horizon, from which, as from a mid-point, they may be surveyed; and we may proceed thus, till we arrive at the highest genus, or universal and true horizon, which is determined by the highest conception, and which contains under itself all differences and varieties, as genera, species, and subspecies.”[^pdf-note-11]

### On 3

Now we probably have a better understanding of what Kant thinks to make a system a system. Architectonic, though, doesn’t directly point to systems as systems but to the art of creating them. In this endeavour a fictitious “architect of reason” faces several problems which mainly accrue from her work item: reason. For the thing called *reason* only includes principles which hardly can be considered as things at all.

> “[T]he principles of pure reason cannot be constitutive even in regard to empirical conceptions, because no sensuous schema corresponding to them can be discovered, and they cannot therefore have an object in concreto. Now, if I grant that they cannot be employed in the sphere of experience, as constitutive principles, how shall I secure for them employment and objective validity as regulative principles, and in what way can they be so employed?”[^pdf-note-12]

Let me try to reconstruct the relevant argument of this passage in a intentionally pessimistic manner:

1. In order to deal with something artificially, like for example systems in architectonic, you have to somehow make sense of it, that is, to understand it.
2. In order to understand this something it has to be tangible by experience in some way.
3. Principles of reason are not tangible by experience in any way.
4. Therefore you cannot deal with them artificially and an art which deals with principles of reason is impossible, - right?

> “[A]lthough it is impossible to discover in intuition a schema for the complete systematic unity of all the conceptions of the understanding, there must be some analogon of this schema. This analogon is the idea of the maximum of the division and the connection of our cognition in one principle. For we may have a determinate notion of a maximum and an absolutely perfect, all the restrictive conditions which are connected with an indeterminate and various content having been abstracted. Thus the idea of reason is analogous with a sensuous schema, with this difference, that the application of the categories to the schema of reason does not present a cognition of any object (as is the case with the application of the categories to sensuous schemata), but merely provides us with a rule or principle for the systematic unity of the exercise of the understanding.”[^pdf-note-13]

Thus, the argumentative reconstruction above turns out to be harshly oversimplified. For even if principles of reason cannot be grasped by understanding immediately, like sensual data, they can be perceived as rules by concrete analogy. It’s like with design patterns in software development. Have you ever observed such a design pattern? Or have you rather observed concrete code examples which implement a pattern in one way or another and by observing those concrete analogies you got an idea of the underlying principle? At least for me I can say, that I only can affirm the latter. From my point of view, software design principles constitute a suitable example for both the *direct* intangibility and the *indirect* tangibility of principles of reason by analogy. We’ll discuss this suitability in the next section.

However for closing this section we need to discuss another major obstacle for an art of systems. When you hear Kant talking about the principles of *homogeneity*, *variety* and *affinity* you might get the impression of an artisan with the glue of homogeneity in the one hand and the knife of variety in the other left with the task to create a continuous whole guided by the principle of affinity. But in actual fact this principle alone appears to be a rather poor guide “because we cannot make any determinate empirical use of this law, inasmuch as it does not present us with any *criterion* of affinity which could aid us in determining how far we ought to pursue the graduation of differences: it merely contains a general indication that it is our duty to seek for and, if possible, to discover them”[^pdf-note-14].

What an artisan of systems needs is an end which tells her how to employ reasonable principles. At the first glance the most obvious solution which comes to mind could be some external purposes like a concrete requirement of a customer, or properties of the building material, for example.

But do you remember what we told about the bricks and stones above? The respects in which *external* purposes guide the construction of a system Kant deliberately excludes from the definition of architectonic. Therefore our fictitious artisan has to find the ends of the system in reason itself. How can we avoid to run into a circle here, though? Actually reason is not just reason for Kant: it’s divided into a theoretical (“speculative”) part and a practical one with seperate responsibilities.

> “Reason, as the faculty of principles, determines the interest of all the powers of the mind and is determined by its own. The interest of its speculative employment consists in the cognition of the object pushed to the highest a priori principles: that of its practical employment, in the determination of the will in respect of the final and complete end.”[^pdf-note-15]

Thus Kant tries to disentangle a possible circularity of pure reason by *departmentalization*. If practical reason is considered as the faculty of ends it’s apt to provide artisans of reason with the necessary goals without taking them from scopes outside of reason. For this interaction to work out, however, the mere departments must also be related to one another by a *primacy of practical reason*.

> “By primacy between two or more things connected by reason, I understand the prerogative, belonging to one, of being the first determining principle in the connection with all the rest. In a narrower practical sense it means the prerogative of the interest of one in so far as the interest of the other is subordinated to it, while it is not postponed to any other. To every faculty of the mind we can attribute an interest, that is, a principle, that contains the condition on which alone the former is called into exercise.”[^pdf-note-16]

According to Kant practical reason has a primacy over its theoretical counterpart because the latter depends on the former in the sense that theoretical reason requires practical one for it’s “execution” while the opposite is not true.

What practical reason now *does* for Kant is avoiding the possible entanglement of reason by prescribing a practical law which only has it’s justification in the problem it has to solve[^pdf-note-17]:

> “Supposing that a will is free, to find the law which alone is competent to determine it necessarily.”[^pdf-note-18]

So the mess which the above artisan of reason got stuck in, is the problem of freedom itself in the end. That’s where the necessity of a lawlike prescription comes in:

> “Since the matter of the practical law, i.e., an object of the maxim, can never be given otherwise than empirically, and the free will is independent on empirical conditions (that is, conditions belonging to the world of sense) and yet is determinable, consequently a free will must find its principle of determination in the law, and yet independently of the matter of the law. But, besides the matter of the law, nothing is contained in it except the legislative form. It is the legislative form, then, contained in the maxim, which can alone constitute a principle of determination of the [free] will.”[^pdf-note-19]

According to this, the “business” of practical reason seems to consist in enforcing a principle which, in my view, has some suspicious odor of *dependency inversion*. Keeping empirical “details” outside sounds actually like a prescription you can be conscious of and work with artificially.

> “We can become conscious of pure practical laws just as we are conscious of pure theoretical principles, by attending to the necessity with which reason prescribes them and to the excretion of all empirical conditions, which it directs us to [translation, C.D.].”[^pdf-note-20]

## Clean “Architecture”

> “I wrote my very first line of code in 1964, at the age of 12. The year is now 2016, so I have been writing code for more than half a century. In that time, I have learned a few things about how to structure software systems—things that I believe others would likely find valuable. I learned these things by building many systems, both large and small. I have built small embedded systems and large batch processing systems. I have built real-time systems and web systems. I have built console apps, GUI apps, process control apps, games, accounting systems, telecommunications systems, design tools, drawing apps, and many, many others. I have built single-threaded apps, multithreaded apps, apps with few heavyweight processes, apps with many light-weight processes, multiprocessor apps, database apps, mathematical apps, computational geometry apps, and many, many others.”[^pdf-note-21]

Uncle Bob comprehends the art of systems based on his experience with specific technical software systems, that is, systems mainly determined by external purposes which Kant, as we saw above, would not put in the domain of architectonic. So why not stop the discussion here with this conclusion?

> “I’ve built a lot of apps. I’ve built a lot of systems. And from them all, and by taking them all into consideration, I’ve learned something startling. *The architecture rules are the same!* This is startling because the systems that I have built have all been so radically different. Why should such different systems all share similar rules of architecture? My conclusion is that *the rules of software architecture are independent of every other variable*.”[^pdf-note-22]

Independency “of every other variable” sounds already a bit more like an art of constructing systems as such, though. So let’s compare Uncle Bob’s notion of software architecture with the Kantian one of architectonic and see if both can learn some lessons from each other.

Maybe it’s a good idea to structure the discussion corresponding to the three points of the last section. Let’s lable them respectively *“On naming”*, because we firstly discussed Kant’s naming decision above, *“On the term ‘system’”* and *“On craftsmanship”*, because that’s how Uncle Bob calls the latter.

### 1. On naming

As far as I can see Uncle Bob doesn’t use the name “architectonic” anywhere. Instead he talks about “architecture” and defines it at some point in the following way:

> “The architecture of a software system is the shape given to that system by those who build it. The form of that shape is in the division of that system into components, the arrangement of those components, and the ways in which those components communicate with each other.”[^pdf-note-23]

So this definition clearly differs from an “art of systems” in the Kantian sense of “architectonic” because it doesn’t refer to systems as such, not even to *software* systems as such, but always just to *a* software system as a concretely formed shape of components. *Arrangement*, *division* and *ways of communication* may already ring the bells of *homogeneity*, *variety* and *affinity*, but let’s postpone this topic to the next section since we are concerned with the name “architecture” here.

Is there any problem with it? I have the impression that there is one if you look at the use of this name in the title of the book “Clean Architecture. A Craftman’s Guide to Software Structure and Design”. Suppose you plug in the definition above, roughly something like “Clean shape of a given software system” might result. But in my view that cannot be what is meant here. The book is a “Craftman’s Guide” full of explanations and illustrations for software design patterns, perceivable analoga for unobservable principles of reason. That’s quite something else than a concrete software system, as the former definition suggests. How can the book be about shapes of software systems if it’s primary concern are principles of an art on how to build them?

Furthermore the naming might actually cause problems for term users. Since in ordinary language we’re probably inclined to think of the relation between “architecture” and “clean architecture” like in the way of, say, “car” and “clean car”, so that the latter behaves like some sort of the former, as in a relation of inheritance. But a concrete *software system* and a *collection of design principles* do clearly *not* behave the same way. Therefore we might, in actual fact, witness a break of the *Liskov Principle* in ordinary language here or, at least, some kind of, say, “polymorphic flaw”.

Kant avoids confusions like this for term users by wisely reserving the name “architectonic” for the “craftsmanship-meaning” which Uncle Bob seems to indifferently name “architecture” in the title of his book.

### 2. On the term “system”

As already mentioned above Uncle Bob describes software systems as distinct components which show some arrangement and communicate to each other. They form a continuous whole which reaches from a detailed low-level to the high-level core.

> “The low-level details and the high-level structure are all part of the same whole. They form a continuous fabric that defines the shape of the system. You can’t have one without the other; indeed, no clear dividing line separates them. There is simply a continuum of decisions from the highest to the lowest levels.”[^pdf-note-24]

The *homogeneous* components are divided by the *specification* of detailedness and brought to continuous *affinity*. Thus, it smells like the Kantian principles are at work here. But actually for the whole to be a whole there’s more to it than just affinity. From an architectural point of view the continuous affinity of the arranged components is stripped on hierarchical bonds of dependencies as shown in Figure 1.

{% include figure.html
  src="/assets/images/posts/clean-architecture/clean_architecture_refactored.png"
  alt="Clean Architecture diagram showing four nested layers and examples of runtime flow and inward-pointing source-code dependencies"
  width="1672"
  height="941"
  caption="Figure 1. AI-generated refactoring of Martin’s Clean Architecture diagram (Martin, 2012; see also Martin, 2018, Figure 22.1)."
%}

> “The overriding rule that makes this architecture work is the Dependency Rule:
>
> *Source code dependencies must point only inward, toward higher-level policies.*
>
> Nothing in an inner circle can know anything at all about something in an outer circle. In particular, the name of something declared in an outer circle must not be mentioned by the code in an inner circle. That includes functions, classes, variables, or any other named software entity. By the same token, data formats declared in an outer circle should not be used by an inner circle, especially if those formats are generated by a framework in an outer circle. We don’t want anything in an outer circle to impact the inner circles.”[^pdf-note-25]

Source code dependencies refer to something else than what Uncle Bob calls the “flow of control”. The latter means the calling hierarchy of the components at runtime[^pdf-note-26]. That’s nothing a software architect is interested in. “[S]oftware architects working in systems written in OO [Object Oriented, C.D.] languages have absolute control over the direction of all source code dependencies in the system”[^pdf-note-27].

Source code dependencies refer to component *names* which appear in the source code *definition* of other components. That’s how they are *“interested”* in each other like homogeneities of reason in the Kantian parlance mentioned above[^pdf-note-28]. The *interested* module has to know the name of the *interesting* module, whereas the opposite is not true. The interesting module doesn’t care and not even know about the interested one.

### 3. On craftsmanship

In other words, source code dependencies are all about the human control of the construction process of software. The machine follows the call hierarchy without caring for the architectural dependency management. But if you have to touch the source code as a developer, you really care for *where* to touch in order to apply some changes. You are a term user of the system and expect the names to be *cleanly* arranged so that functional progress can painlessly implemented.

But how to bring this about? At this point we have to talk about some specialities of the building material we’re facing here, that is software. This is also the place where we can finally answer the still open question why this whole section should be relevant at all. What has the craftsmanship of a *software* system architect to do with the art of systems as such?

In order to see the software-independency and the overarching generality of software architectonical problems, I think we have to take Uncle Bob’s observation above more seriously: “*[T]he rules of software architecture are independent of every other variable*”[^pdf-note-29].

If you think about this for moment, what does this imply? Doesn’t Uncle Bob say here that, according to his long-lived experience, the rules of software architecture depend only on themselves while every other things relevant to the softare architect depend on them? The less you can deny this the more Uncle Bob’s observations conform to what Kant says about the *Behavior* pure reason: “Reason, as the faculty of principles, determines the interest of all the powers of the mind and is determined by its own” (see above: p. 6). Of course I’m not suggesting that software is a mind, so that software architects are godlike creators of conscious beings. Only I’m pointing to the behavior of software as “medium”.

> “It’s not obvious that software structure obeys our intuition the way building structure does. Buildings have an obvious physical structure, whether rooted in stone or concrete, whether arching high or sprawling wide, whether large or small, whether magnificent or mundane. Their structures have little choice but to respect the physics of gravity and their materials. On the other hand—except in its sense of seriousness—software has little time for gravity. And what is software made of? Unlike buildings, which may be made of bricks, concrete, wood, steel, and glass, software is made of software. Large software constructs are made from smaller software components, which are in turn made of smaller software components still, and so on. It’s coding turtles all the way down. When we talk about software architecture, software is recursive and fractal in nature, etched and sketched in code. Everything is details. Interlocking levels of detail also contribute to a building’s architecture, but it doesn’t make sense to talk about physical scale in software.”[^pdf-note-30]

What Kevlin Henney, in his foreword to the “Clean Architecture” book, points out is that software is a very special kind of bulding material because it just consists of itself. We write code by using other code and structuring our own. That’s all about it. As developers or architects we do not integrate soft- with hardware or the like. Those are different layers. The best thing you can do is to translate between them. But that’s not the job description of a *software* developer or architect. We’re bound to a medium which only finds structure in itself. There’s not the luxury as for an architect of houses to form plans or expectations based on considerations of bricks and stones. We’re doomed to build houses out of houses based on house-considerations, if you allow me to overtax the metaphor this way.

The only regard we can cling to is the purpose of the whole as whole, mere wholeness, say. In this respect, I suspect, what Kant says about the architectonic of pure reason fully, that is *not just in some metaphorical sense*, applies to the problems of software architecture, as well.

Do you remember what we said about the fictitious artisan of reason trying helplessly to form some whole only equipped with the principle of homogeneity, specification and affinity? Isn’t the software architect quite in a similar position? In my view, she is indeed. But there’s a solution and, like for Kant, it can only be a practical one.

> “The first value of software is its behavior. Programmers are hired to make machines behave in a way that makes or saves money for the stakeholders. We do this by helping the stakeholders develop a functional specification, or requirements document. Then we write the code that causes the stakeholder’s machines to satisfy those requirements.”[^pdf-note-31]

Thus, for Uncle Bob the orienting purpose can only originate in the stakeholders’ needs. A software system, in the end, is nothing but a functional whole whose function is to satisfy stakeholders. But how does architectonic come in?

> “Software was invented to be ‘soft.’ It was intended to be a way to easily change the behavior of machines. If we’d wanted the behavior of machines to be hard to change, we would have called it hardware. To fulfill its purpose, software must be soft—that is, it must be easy to change. When the stakeholders change their minds about a feature, that change should be simple and easy to make. The difficulty in making such a change should be proportional only to the scope of the change, and not to the shape of the change.”[^pdf-note-32]

Architecting for the whole means therefore architecting for what makes software *soft*ware: It’s ability to change in order to function, that is adapting to the needs of stakeholders. “If you give me a program that does not work but is easy to change, then I can make it work, and keep it working as requirements change. Therefore the program will remain continually useful”[^pdf-note-33]. From an architectural point of view, thus, shape does not only not matter, it’s the architect’s job to guarantee that it does not matter.

> “The problem, of course, is the architecture of the system. The more this architecture prefers one shape over another, the more likely new features will be harder and harder to fit into that structure. Therefore architectures should be as shape agnostic are practical.”[^pdf-note-34]

But how do you bring about this shape agnosticism practically? The first and most important thing an architect has to do is to draw a distinction between policy and details.

> “All software systems can be decomposed into two major elements: policy and details. The policy element embodies all the business rules and procedures. The policy is where the true value of the system lives. The details are those things that are necessary to enable humans, other systems, and programmers to communicate with the policy, but that do not impact the behavior of the policy at all. They include IO devices, databases, web systems, servers, frameworks, communication protocols, and so forth.”[^pdf-note-35]

Details contain the functionalities that you expect to change rather frequently, policies contain the core functionalities you rarely or never expect to change. They represent what makes the system *the* system. The definition of what would completely destroy the system’s usefulness if absent.

This kind of a judgement is peculiar because it involves idealized expectations. You try to *counterfactually* anticipate all possible changes of the future stakeholder community. But of course you don’t perform this kind of judgement once and forever. By this forward looking judgement you also have to anticipate your future judgements of this same kind.

> “The way you keep software soft is to leave as many options open as possible, for as long as possible. What are the options that we need to leave open? They are the details that don’t matter [...] The goal of the architect is to create a shape for the system that recognizes policy as the most essential element of the system while making the details irrelevant to that policy. This allows decisions about those details to be delayed and deferred.”[^pdf-note-36]

That’s the whole secret about the whole and also the reason why Uncle Bob considers the *dependency inversion principle*[^pdf-note-37] the most important one. It combines the policy/detail distinction with the one between interesting/interested[^pdf-note-38] components in order to keep the functional whole functioning *over time*, ideally forever and for all imaginable stakeholders.

In this regard I would like to emphasize one of the famous SOLID Design Principles, namely the Single Responsibility Principle (SRP), because Uncle Bob transforms his historical meaning to a new one:

> “Historically, the SRP has been described this way:
>
> *A module should have one, and only one, reason to change.*
>
> Software systems are changed to satisfy users and stakeholders; those users and stakeholders *are* the ‘reason to change’ that the principle is talking about. Indeed, we can rephrase the principle to say this:
>
> *A module should be responsible to one, and only one, user or stakeholder.*
>
> Unfortunately, the words ‘user’ and ‘stakeholder’ aren’t really the right words to use here. There will likely be more than one user or stakeholder who wants the system changed in the same way. Instead, we’re really referring to a group—one or more people who require that change. We’ll refer to that group as an *actor*.”[^pdf-note-39]

To illustrate this let’s suppose one “actor”, which Uncle Bob defines as a group of stakeholders in the end, wants a module to output the text “foo” somewhere and another actor wants exactly the same module to output “bar” in one and the same place. In this example you don’t face a mere change. You have to deal with conflicting requirements between the actors which, in the extreme case, when the conflicting requirements cannot be conciliated, can result in the checkmate for your system.

The SRP solves the conflict by avoiding it *a priori*. You anticipate conflicting actors and give them their exclusive modules they can rule over respectively. Thus, what the SRP actually represents is a systemic mechanism to avoid dissent betweent potentially conflicting stakeholder parties.

## Learnings

Let’s draw some conclusions from the conversation above by reviewing the results of the different section types.

### 1. On naming

With respect to naming we registered that Kant did not use the name “architecture”, but “architectonic” for designating the “art of systems”. Uncle Bob, however, seems to call the craftsmanship of software systems and the concrete shape of a software system “architecture” likewise which might either evoke misunderstandings or the need to specify more precisely on the side of term users.

### 2. On the term “system”

What a system as system looks like for both architects is a continuously affine whole of specified homogeneities (Kant)/components (Uncle Bob) which are interested in (Kant)/dependent on (Uncle Bob) each other.

### 3. On craftsmanship

To me it seems that the real place for mutual learnings is the section about craftsmanship.

#### Uncle Bob to Kant

Is there somthing Kant can learn from Uncle Bob?

From my point of view the Kantian concept of architectonic has some deficits when it comes to dealing with change requests. Let me show you the following passage from the *Critique of Pure Reason* about Kant’s architectonic of sciences where he talks about the role of empirical psychology and its further perspective:

> “Empirical psychology must [...] be banished from the sphere of metaphysics, and is indeed excluded by the very idea of that science. In conformity, however, with scholastic usage, we must permit it to occupy a place in metaphysics—but only as an appendix to it. We adopt this course from motives of economy; as psychology is not as yet full enough to occupy our attention as an independent study, while it is, at the same time, of too great importance to be entirely excluded or placed where it has still less affinity than it has with the subject of metaphysics. It is a stranger who has been long a guest; and we make it welcome to stay, until it can take up a more suitable abode in a complete system of anthropology—the pendant to empirical physics.”[^pdf-note-40]

In other words: “Well, you know, now I banish empirical psychology from metaphysics, but not really, I keep it appended for economic reasons but at some later point I might do something else...” I mean: “what?” He’s talking about change requests for the system of sciences like an intern with hangover talks about the software design of his demo application. Uncle Bob’s architectonic seems to deal with changes in a way more elaborated fashion because he *“a priorically” bases* the architeconical perspective on such considerations.

#### Kant to Uncle Bob

What Kant might teach Uncle Bob, though, is that changes are more than an anonymous stream of change requests. They origin in the wills of stakeholders which you have a duty to comply with. That’s because, well, when Kant talks about practical reason, he always talks about *ethics* in fact. So what Kant emphasizes is the *responsibility* you have as an arichtect. You’re responsible to ideally anticipate the needs of a continuously feedbacking stakeholder community.

So maybe one could rephrase his famous Categorical Imperative the following way:

> “Make architectural decisions in a way that the will of you maxim is compatible with the ones of an idealizied community of stakeholders - and remember simultaneously that you have to make and revise such decisions all the time.”

Or at least somtehing like this, time will show...

Maybe there are even better ways out there to *idealize* the requirements of stakeholders than some abstract imperative formulas. Why not use plantUML[^pdf-note-41] diagrams instead, for example?

#### General

Are there also some general learnings for “mortal” developers and architects? If we dig deep enough, we can find numerous learnings, I guess, but the one I would like to highlight concludingly is the following: We really should think about considering the roles of “architect” and “developers” *not* as personally bound fixations, but as *functional*. Everytime you do something which supports the “changeability” of the system over time, e.g. following Uncle Bob’s design principles, document your code, or even just thinking about the name in a method signature which makes it easier for you to get back into your code at a latter point in time, well, everytime you do something like this, you already act functionally as an architect and, if you like and I’m not wrong, may proudly name yourself an *artisan of reason* in the Kantian sense.

## References

Baum, M. (2001). Systemform und Selbsterkenntnis der Vernunft bei Kant. In H. F. Fulda & J. Stolzenberg (Eds.), *Architektonik und System in der Philosophie Kants: System der Vernunft. Kant und der deutsche Idealismus* (Vol. 1, pp. 25–40). Meiner.

Kant, I. (1781/1787). *The critique of pure reason* (J. M. D. Meiklejohn, Trans.). Project Gutenberg. <https://www.gutenberg.org/ebooks/4280>

Kant, I. (1788). *The critique of practical reason* (T. K. Abbott, Trans.). Project Gutenberg. <https://www.gutenberg.org/ebooks/5683>

König, P. (2001). Die Selbsterkenntnis der Vernunft und das wahre System der Philosophie bei Kant. In H. F. Fulda & J. Stolzenberg (Eds.), *Architektonik und System in der Philosophie Kants: System der Vernunft. Kant und der deutsche Idealismus* (Vol. 1). Meiner.

La Rocca, C. (2013). Methode und System in Kants Philosophieauffassung. In S. Bacin, A. Ferrarin, C. La Rocca, & M. Ruffing (Eds.), *Kant und die Philosophie in weltbürgerlicher Absicht: Akten des XI. Internationalen Kant-Kongresses* (Vol. 1, pp. 277–297). De Gruyter. <https://doi.org/10.1515/9783110246490.277>

Martin, R. C. (2012, August 13). *The clean architecture*. The Clean Code Blog. <https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html>

Martin, R. C. (2018). *Clean architecture: A craftsman’s guide to software structure and design*. Prentice Hall.

Peirce, C. S. (1891). The architecture of theories. *The Monist, 1*(2), 161–176. <https://doi.org/10.5840/monist18911211>

## Notes
{: .footnotes-heading}

[^pdf-note-01]: <span lang="de">“Ich verstehe unter einer Architektonik die Kunst der Systeme”.</span> KrV, A 832/B 860.

    This latter expression is an international convention on how to cite Kant. “KrV” means “Kritik der reinen Vernunft”, the german original title. The letter “A” refers to the first and the letter “B” to the second and significantly revised second edition of the book. That’s why people who interpret Kant distinguish here. Thus, no worries about the syntax!

    Btw: How many authors do you know who have international conventions in place on how to cite them when they’re already dead for over 200 years? Notice carefully that, when *Kant* speaks, there speaks an eternal grand master of human intelligence. So there might be good reasons to listen, but to form your own judgement, as well. He doesn’t need to be always right. And surely isn’t.

[^pdf-note-02]: <https://www.gutenberg.org/files/4280/4280-h/4280-h.htm#chap106>.

    <span lang="de">“Ich verstehe aber unter einem Systeme die Einheit der mannigfaltigen Erkenntnissse unter einer Idee. Diese ist der Vernunftbegriff von der Form des Ganzen, so fern durch denselben der Umfang des Mannigfaltigen so wohl, als die Stelle der Teile unter einander, a priori bestimmt wird”.</span> KrV, A 832/B860. Read the expression “a priori” like “in advance” or so.

[^pdf-note-03]: <span lang="de">“Die Einheit des Zwecks, worauf sich alle Teile und in der Idee desselben auch unter einander beziehen, macht, daß ein jeder Teil bei der Kenntnis der übrigen vermißt werden kann”</span> KrV A 832-833/B 860-861.

[^pdf-note-04]: <span lang="de">“Der szientifische Vernunftbegriff enthält also den Zweck und die Form des Ganzen, das mit demselben kongruiert”.</span> KrV, A 832/B 860.

[^pdf-note-05]: Philosophers call this *“teleological”*. If you’re interested in the teleology of reason according to the Kantian system see (La Rocca, 2013, pp. 292–293) or (König, 2001, pp. 47–50).

[^pdf-note-06]: <https://www.gutenberg.org/files/4280/4280-h/4280-h.htm#chap106>.

    <span lang="de">“Die Idee bedarf zur Ausführung ein Schema, d.i. eine a priori aus dem Prinzip des Zwecks bestimmte wesentliche Mannigfaltigkeit und Ordnung der Teile. Das Schema, welches nicht nach einer Idee, d.i. aus dem Hauptzwecke der Vernunft, sondern empirisch, nach zufällig sich darbietenden Absichten (deren Menge man nicht voraus wissen kann), entworfen wird, gibt technische, dasjenige aber, was nur zu Folge einer Idee entspringt (wo die Vernunft die Zwecke a priori aufgibt, und nicht empirisch erwartet), gründet architektonische Einheit. Nicht technisch, wegen der Ähnlichkeit des Mannigfaltigen, oder des zufälligen Gebrauchs der Erkenntnis in concreto zu allerlei beliebigen äußeren Zwecken, sondern architektonisch, um der Verwandtschaft willen und der Ableitung von einem einigen obersten und inneren Zwecke, der das Ganze allererst möglich macht, kann dasjenige entspringen, was wir Wissenschaft nennen, dessen Schema den Umriß (monogramma) und die Einteilung des Ganzen in Glieder, der Idee gemäß, d.i. a priori enthalten, und dieses von allen anderen sicher und nach Prinzipien unterscheiden muß.”</span> KrV, A 833-834/B 861-862.

[^pdf-note-07]: Ibid.

[^pdf-note-08]: The linkage between the principles of understanding and architectonic is emphasized by (König, 2001, p. 45). Those principles, at least in my view, also show a stunning similarity to what (Peirce, 1891, p. 175) respectively calls “The First”, “The Second” and “The Third”. But this might just be superstition.

[^pdf-note-09]: <https://www.gutenberg.org/files/4280/4280-h/4280-h.htm#chap95>.

    <span lang="de">“Die Vernunft bereitet also dem Verstande sein Feld, 1. durch ein Prinzip der Gleichartigkeit des Mannigfaltigen unter höheren Gattungen, 2. durch einen Grundsatz der Varietät des Gleichartigen unter niederen Arten; und um die systematische Einheit zu vollenden, fügt sie 3. noch ein Gesetz der Affinität aller Begriffe hinzu, welches einen kontinuierlichen Übergang von einer jeden Art zu jeder anderen durch stufenartiges Wachstum der Verschiedenheit gebietet”.</span> KrV, A 657-658/B 685-686.

[^pdf-note-10]: <https://www.gutenberg.org/files/4280/4280-h/4280-h.htm#chap95>.

    <span lang="de">“Das dritte vereinigt jene beide, indem sie bei der höchsten Mannigfaltigkeit dennoch die Gleichartigkeit durch den stufenartigen Übergang von einer Spezies zur anderen vorschreibt, welches eine Art von Verwandtschaft der verschiedenen Zweige anzeigt, in so fern sie insgesamt aus einem Stamme entsprossen sind”.</span> KrV A 658/B 686.

[^pdf-note-11]: <https://www.gutenberg.org/files/4280/4280-h/4280-h.htm#chap95>.

    <span lang="de">“Man kann sich die systematische Einheit unter den drei logischen Prinzipien auf folgende Art sinnlich machen. Man kann einen jeden Begriff als einen Punkt ansehen, der, als der Standpunkt eines Zuschauers, seinen Horizont hat, d.i. eine Menge von Dingen, die aus demselben können vorgestellet und gleichsam überschauet werden. Innerhalb diesem Horizonte muß eine Menge von Punkten ins Unendliche angegeben werden können, deren jeder wiederum seinen engeren Gesichtskreis hat; d.i. jede Art enthält Unterarten, nach dem Prinzip der Spezifikation, und der logische Horizont besteht nur aus kleineren Horizonten (Unterarten), nicht aber aus Punkten, die keinen Umfang haben (Individuen). Aber zu verschiedenen Horizonten, d.i. Gattungen, die aus eben so viel Begriffen bestimmt werden, läßt sich ein gemeinschaftlicher Horizont, daraus man sie insgesamt als aus einem Mittelpunkte überschauet, gezogen denken, welcher die höhere Gattung ist, bis endlich die höchste Gattung der allgemeine und wahre Horizont ist, der aus dem Standpunkte des höchsten Begriffs bestimmt wird, und alle Mannigfaltigkeit, als Gattungen, Arten und Unterarten, unter sich befaßt.”</span> KrV, A 658-659/B 686-687

[^pdf-note-12]: <https://www.gutenberg.org/files/4280/4280-h/4280-h.htm#chap95>.

    <span lang="de">“Prinzipien der reinen Vernunft können dagegen nicht einmal in Ansehung der empirischen Begriffe konstitutiv sein, weil ihnen kein korrespondierendes Schema der Sinnlichkeit gegeben werden kann, und sie also keinen Gegenstand in concreto haben können. Wenn ich nun von einem solchen empirischen Gebrauch derselben, als konstitutiver Grundsätze, abgehe, wie will ich ihnen dennoch einen regulativen Gebrauch, und mit demselben einige objektive Gültigkeit sichern, und was kann derselbe für Bedeutung haben?”.</span> KrV, A 664/B 692.

[^pdf-note-13]: <https://www.gutenberg.org/files/4280/4280-h/4280-h.htm#chap95>.

    <span lang="de">“Allein, obgleich für die durchgängige systematische Einheit aller Verstandesbegriffe kein Schema in der Anschauung ausfündig gemacht werden kann, so kann und muß doch ein Analogen eines solchen Schema gegeben werden, welches die Idee des Maximum der Abteilung und der Vereinigung der Verstandeserkenntnis in einem Prinzip ist. Denn das Größeste und Absolutvollständige läßt sich bestimmt gedenken, weil alle restringierende Bedingungen, welche unbestimmte Mannigfaltigkeit geben, weggelassen werden. Also ist die Idee der Vernunft ein Analogon von einem Schema der Sinnlichkeit, aber mit dem Unterschiede, daß die Anwendung der Verstandesbegriffe auf das Schema der Vernunft nicht eben so eine Erkenntnis des Gegenstandes selbst ist (wie bei der Anwendung der Kategorien auf ihre sinnliche Schemate), sondern nur eine Regel oder Prinzip der systematischen Einheit alles Verstandesgebrauchs”.</span> KrV, A 665/B 693.

[^pdf-note-14]: <https://www.gutenberg.org/files/4280/4280-h/4280-h.htm#chap95>.

    <span lang="de">“Man siehet aber leicht, daß diese Kontinuität der Formen eine bloße Idee sei, der ein kongruierender Gegenstand in der Erfahrung gar nicht aufgewiesen werden kann, nicht allein um deswillen, weil die Spezies in der Natur wirklich abgeteilt sind, und daher an sich ein quantum discretum ausmachen müssen, und, wenn der stufenartige Fortgang in der Verwandtschaft derselben kontinuierlich wäre, sie auch eine wahre Unendlichkeit der Zwischenglieder, die innerhalb zweier gegebenen Arten lägen, enthalten müßte, welches unmöglich ist: sondern auch, weil wir von diesem Gesetz gar keinen bestimmten empirischen Gebrauch machen können, indem dadurch nicht das geringste Merkmal der Affinität angezeigt wird, nach welchem und wie weit wir die Gradfolge ihrer Verschiedenheit zu suchen, sondern nichts weiter, als eine allgemeine Anzeige, daß wir sie zu suchen haben”.</span> KrV, A 661/B 689.

[^pdf-note-15]: <https://www.gutenberg.org/files/5683/5683-h/5683-h.htm#link2H_4_0038>.

    <span lang="de">“Die Vernunft, als das Vermögen der Prinzipien, bestimmt das Interesse aller Gemütskräfte, das ihrige aber sich selbst. Das Interesse ihres spekulativen Gebrauchs besteht in der Erkenntnis des Objekts bis zu den höchsten Prinzipien a priori, das des praktischen Gebrauchs in der Bestimmung des Willens, in Ansehung des letzten und vollständigen Zwecks”.</span> KpV, AA 05: 119-120. That’s just the citation convention for the Critique of *practical* Reason.

[^pdf-note-16]: <https://www.gutenberg.org/files/5683/5683-h/5683-h.htm#link2H_4_0038>. <span lang="de">“Unter dem Primate zwischen zweien oder mehreren durch Vernunft verbundenen Dingen verstehe ich den Vorzug des einen, der erste Bestimmungsgrund der Verbindung mit allen übrigen zu sein. In engerer, praktischen Bedeutung bedeutet es den Vorzug des Interesse des einen, so fern ihm (welches keinem andern nachgesetzt werden kann) das Interesse der andern untergeordnet ist. Einem jeden Vermögen des Gemüts kann man ein Interesse beilegen, d.i. ein Prinzip, welches die Bedingung enthält, unter welcher allein die Ausübung desselben befördert wird”.</span> KpV, AA 05: 119

[^pdf-note-17]: That the purpose of pure reason lies in the practical law is also claimed by (Baum, 2001, pp. 32–33) who refers to the preface of the second edition of the *Critique of Pure Reason*.

[^pdf-note-18]: <https://www.gutenberg.org/files/5683/5683-h/5683-h.htm#link2H_4_0016>.

    <span lang="de">“Vorausgesetzt, daß ein Wille frei sei: das Gesetz zu finden, welches ihn allein notwendig zu bestimmen tauglich ist”.</span> KpV, AA 05: 29.

[^pdf-note-19]: Ibid.

    <span lang="de">“Da die Materie des praktischen Gesetzes, d.i. ein Objekt der Maxime, niemals anders als empirisch gegeben werden kann, der freie Wille aber, als von empirischen (d.i. zur Sinnenwelt gehörigen) Bedingungen unabhängig, dennoch bestimmbar sein muß: so muß ein freier Wille, unabhängig von der Materie des Gesetzes, dennoch einen Bestimmungsgrund in dem Gesetze antreffen. Es ist aber, außer der Materie des Gesetzes, nichts weiter in demselben, als die gesetzgebende Form enthalten. Also ist die gesetzgebende Form, so fern sie in der Maxime enthalten ist, das einzige, was einen Bestimmungsgrund des Willens ausmachen kann.”</span> Ibid.

[^pdf-note-20]: <span lang="de">“Wir können uns reiner praktischer Gesetze bewußt werden, eben so, wie wir uns reiner theoretischer Grundsätze bewußt sind, indem wir auf die Notwendigkeit, womit sie uns die Vernunft vorschreibt, und auf Absonderung aller empirischen Bedingungen, dazu uns jene hinweiset, Acht haben”.</span> KpV, AA 05: 30.

[^pdf-note-21]: (Martin, 2018, p. xix)

[^pdf-note-22]: (Martin, 2018, p. xx)

[^pdf-note-23]: (Martin, 2018, p. 136)

[^pdf-note-24]: (Martin, 2018, p. 4)

[^pdf-note-25]: (Martin, 2018, pp. 203-204)

[^pdf-note-26]: see (Martin, 2018, p. 46)

[^pdf-note-27]: (Martin, 2018, p. 46)

[^pdf-note-28]: see above on p. 6

[^pdf-note-29]: (Martin, 2018, p. xx)

[^pdf-note-30]: (Martin, 2018, p. xx)

[^pdf-note-31]: (Martin, 2018, p. 14)

[^pdf-note-32]: (Martin, 2018, pp. 14–15)

[^pdf-note-33]: (Martin, 2018, p. 15)

[^pdf-note-34]: Ibid.

[^pdf-note-35]: (Martin, 2018, p. 140)

[^pdf-note-36]: (Martin, 2018, p. 140)

[^pdf-note-37]: As already announced in the Kanitan section above. See p. 7.

[^pdf-note-38]: I really prefer the Kantian names for the concept of dependency tbh. It comes in handier and conceals to a lesser degree that dependency structures, in the end, originate in the interests of stakeholders

[^pdf-note-39]: (Martin, 2018, p. 62)

[^pdf-note-40]: <https://www.gutenberg.org/files/4280/4280-h/4280-h.htm#chap106>.

    <span lang="de">“Also muß empirische Psychologie aus der Metaphysik gänzlich verbannet sein, und ist schon durch die Idee derselben davon gänzlich ausgeschlossen. Gleichwohl wird man ihr nach dem Schulgebrauch doch noch immer (obzwar nur als Episode) ein Plätzchen darin verstatten müssen, und zwar aus ökonomischen Bewegursachen, weil sie noch nicht so reich ist, daß sie allein ein Studium ausmachen, und doch zu wichtig, als daß man sie ganz ausstoßen, oder anderwärts anheften sollte, wo sie noch weniger Verwandtschaft als in der Metaphysik antreffen dürfte. Es ist also bloß ein solange aufgenommener Fremdling, dem man auf einige Zeit einen Aufenthalt vergönnt, bis er in einer ausführlichen Anthropologie (dem Pendant zu der empirischen Naturlehre) seine eigene Behausung wird beziehen können”.</span> KrV, A 848-849/B 876-877

[^pdf-note-41]: see <https://plantuml.com/>
