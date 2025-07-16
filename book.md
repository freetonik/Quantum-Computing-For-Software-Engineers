# Preface

Quantum computing has always seen to be a bit of science fiction. On one hand, there are numerous publications by sceptics, from both general public, journalists, and esteemed scientists, explaining in seemingly indisputable detail why quantum computing is at best unachievable in any foreseeable future, or at worst fundamentally impossible. On the other hand, there are dozens of companies of all sizes, from industry behemoths like IBM and Google, to smaller startups focusing on one or several niche areas: algorithms, control electronics, calibration, software development frameworks, etc. The industry is experiencing quite a wave of interest, and naturally there is a lot of hype. Some companies make such bold claims, that one can understand the sceptics' views, especially when those claims are not demonstrated. 

So, who is right? Is quantum computing as unreal as intergalactic space travel, and we have no chance of seeing it in our lifetimes? Or is it already here and we just need to invest a bit more time and energy into making it practical?

This may be a bad analogy, but humor me: truly practical quantum computing may be compared to the colonization of the Solar system. In theory, it should be possible. Moreover, we have made a lot of progress in the last century, and have solved a lot of extremely hard engineering challenges allowing us to send probes to distant worlds and even put people on the Moon. General-purpose quantum computing is like saying "we have bases on multiple planets, with a reliable, efficient transport network". I'll be first to admit how bad the analogy is, especially because quantum computing is simultaneously easier and harder than the colonization of the Solar system. It's easier because just in terms of resources and the sheer number of engineering problems, it's a much smaller problem than interspace travel. It's much harder because nothing in the observed properties of physics seem to be stopping us from travelling in space, but the more you try to control the quantum world, the more the universe acts against your pursuit. I can believe that if the humanity decides to invest 1/10th of its wealth into space travel, we may have colonies on a few planets and moons in a few decades. I am absolutely not sure the same can be said about quantum computing: investing 1/10th of all wealth may not give us a machine with a few million of stable logical qubits. Space travel needs to solve very hard engineering problems, but they are the same level of problems that always existed: properties of materials, energy efficiency, food production, environment preservation, etc. Quantum computing needs to solve a completely new set of challenges, never seen before. 

But this is why it's such a fascinating industry. 

Having said all that, I want to stress one more point: quantum computers are already useful. Although no quantum computer has helped solve real-world problems yet (such as large quantum simulations, optimizations, NP-hard problems, cryptography, and other areas promoted by the hype), companies and scientific organizations purchase quantum computers to do research. Today, most QC devices can be considered research tools. There are three main areas of research:

1. Quantum physics
2. Quantum computing
3. Integration

Since quantum computers are essentially analog devices that allow you to control, in a limited fashion, a set of quantum objects, you can do some research in the foundational quantum physics. Certain things that require tremendous computational resources on a classical computer may be done easier and faster on a quantum computer. Still, given the current state of the industry, classical computers outperform most quantum systems. But the research applied to a smaller QCs can be scaled once the hardware scales. 

Of course, the main area is quantum computing itself. From abstract, mathematical notions of algorithms to very low-level questions of calibration, many universities and research organizations are eager to have a quantum computer available to prove their theories, and discover new properties. Commercial companies that deal with material science, battery technology, agriculture, chemistry are buying quantum computers (or at least buying access to one) because they want to be ready if and when truly large-scale QCs become available. It is known that with a robust, large-scale QC one can develop, for example, better chemicals or car batteries by efficiently simulating complex molecules and their interactions. Altghough you can't do it today, you can start developing the organizational knowledge and apply it to smaller-scale issues. In the same fashion as many organizations decided to try to "play" with the first computers back in the day, and as a result came better prepared for the digital age.

And finally, integration research. This is the least known and least discussed topic in the industry, but is very important. Its significance is one of the motivations for writing this book. Quantum computers, being research tools, are not normal products. They are driven by software, like anything else, but this software changes rapidly, and is rarely written with a long-term evolution in mind. If you buy a quantum computer today, chances are your code will not work on any other quantum computer, or even on the next iteration of the same machine. At the same time, researchers often need to work with mutliple types of machines simultaneously, and HPC (high-performance computing) centers, i.e. supercomputing data centers, want to integrate quantum computers into their existing infrastructure and provide a "quantum compute" service to its users. 

# Chapter 1. Groundwork

## Quantum physics 101

- Quantum level by example of spectroscopy
  - Why we know the chemical composition of distant planets better than that of Earth's core
  - Why simulating quantum systems is so challenging
  - Why even simulate it?
- Should a qubit be an electron? An atom? A molecule? Something else entirely?
  - Different modalities of QCs
  - What makes superconducting technology a promising choice
- Myths about quantum computers
