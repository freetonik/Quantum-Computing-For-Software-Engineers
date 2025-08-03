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

# Chapter 2. Levels of Abstraction of a Superconducting Quantum Computer

## Crafting a qubit with superconductivity

Quantum computing is often imagined as something delicate and ethereal: electrons hovering in superposition, photons zipping through fiber-optic mazes. And while those images reflect real research directions, one of the most powerful approaches to building quantum computers is surprisingly tangible: circuits made of wire and metal, etched onto chips. In this chapter, we explore how quantum information—the elusive qubit—can live not just in particles, but in entire electrical circuits, made practical by the strange and remarkable world of superconductivity.

For me this fact was probably the most mind-blowing. I knew about quantum computers in general before starting to work in the industry, but I always thought a quantum computer is built with stereotypical quantum things. The majority of popular science books and even university textbooks always describe quantum physics via properties of photos and electrons, so naturally when it comes to utilizing the quantum effects for computation, the same objects are re-used. Apart from engineering concerns, it doesn't really matter which one to use, just like with classical computers we could built processors out of vacuum tubes or transistors. The theoretical computation is equivalent, but the engineering tradeoffs are huge. 

TODO: stricter definition of a qubit.

At its core, a qubit is just a two-level quantum system. Any physical object that can exist in two distinct quantum states—and, crucially, in superpositions of those states—can serve as a qubit. Electrons, with their spin states, or photons, with their polarization, are natural candidates. But quantum mechanics doesn’t limit us to the microscopic. With careful engineering, even something as macroscopic as a loop of wire can be coaxed into behaving quantum mechanically.

This leads to a bold idea: we can create a qubit out of a simple electrical circuit, such as a loop containing a capacitor and an inductor. The capacitor stores energy in an electric field, the inductor in a magnetic field. Together, they form an LC oscillator—essentially a quantum harmonic oscillator when cooled and isolated enough. The energy in this circuit oscillates back and forth between the electric and magnetic fields, just like a mass on a spring.

But real wires aren’t perfect. In ordinary circuits, resistance drains energy over time, converting it into heat. This dissipation erases the quantum information stored in the circuit’s oscillations. A qubit that leaks energy is like a memory cell that forgets its value—it’s useless for computation.

To maintain coherence—the ability to hold quantum information—we need to eliminate resistance. Luckily, the rules of the universe happen to have a property that can help us: superconductivity. 

Superconductors are materials that, when cooled below a certain temperature, exhibit zero electrical resistance. Current can flow essentially forever in a superconducting loop without any loss. When we build our LC circuit from superconducting materials, we get a high-quality quantum oscillator that can retain energy—and quantum information—for much longer.

With superconductivity, our circuit is no longer just an analog of quantum mechanics—it becomes a bona fide quantum system. It exhibits quantized energy levels, and under the right conditions, can even show superpositions and entanglement. But there’s still a problem: such a circuit has evenly spaced energy levels. It’s like a ladder with rungs at perfectly regular intervals. That’s fine for physics experiments, but not great for quantum computing.

To perform quantum gates, we need to isolate just two energy levels—say, the ground state and the first excited state—and control transitions between them. But in a harmonic oscillator, applying energy that flips the qubit from |0⟩ to |1⟩ can just as easily excite it from |1⟩ to |2⟩, or beyond. That means our circuit isn’t just a qubit—it’s a “qutrit,” or worse. It’s hard to address just two levels in a harmonic system. To solve this, we need to make the energy levels uneven—_anharmonic_.

The breakthrough came with the Josephson junction: a thin insulating barrier between two superconductors. It behaves in a non-linear way, introducing exactly the anharmonicity we need. By adding a Josephson junction to the circuit we create a non-linear oscillator whose energy levels are no longer equally spaced.

Now, the transition from |0⟩ to |1⟩ requires a different energy than the transition from |1⟩ to |2⟩. This spacing allows us to selectively excite and manipulate just the lowest two levels, effectively creating a true qubit. These are called _transmon qubits_, one of the most widely used types in today’s superconducting quantum computers.

Note that accessing higher state like |2⟩ can still be useful for certain areas of research and even for certain computational tasks. Some scientists working on simulating chemical reactions would like to be able to access higher states inside of a quantum processor because those state might have better correlation to the underlying models they're trying to simulate. But for general purpose quantum computing, just two states  |0⟩ and |1⟩ are enough, and unlocking higher states does not expand the domain of problems that can be solved.

There are different ways to implement superconducting qubits, depending on which variable—charge or flux—you use to store and manipulate quantum information.

- **Charge qubits** rely on the number of Cooper pairs (paired electrons) on a small superconducting island. They’re sensitive to charge fluctuations, which can be both a blessing and a curse. While they can be manipulated quickly, they’re also vulnerable to noise.
- **Flux qubits**, on the other hand, encode information in the direction of current flowing around a superconducting loop. This current generates a magnetic flux, hence the name. Flux qubits are typically more robust against charge noise, but can be more complex to control and fabricate.

There’s a third kind, called the _phase qubit_, which uses the phase difference across a Josephson junction as its state variable. And the _transmon_ qubit—a sort of refined charge qubit with reduced sensitivity to noise—has become the dominant platform in many quantum computing systems today.

Don't worry, we don't have to dive much deeper than this. I mean, you totally can if this sounds interesting, but we are going to move up the ladder of abstraction now and start treating qubits as generic objects with certain limited amount of properties. However, you will soon start noticing that in modern quantum computing most abstractions leak, both upwards and downwards. 

1. Calibration
	1. the problem of drift
	2. initial calibration
	3. re-calibration
	4. derived properties and "architectures"
	5. dynamic topology
2. High level: quantum algorithms
	1. theory
	2. practical limitations
3. Quantum circuits and classical computing
	1. direct analogy to logic gates, assembly language
4. Pulse-level
	1. why break the abstraction barrier
	2. who needs this
5. Control instruments
	1. from lab equipment to industrial tooling
	2. the zoo of architectures
6. QPU
	1. chip, connections, holder
	2. cryostat

# Chapter 3

## SDKs and formats (Qiskit, Cirq, CUDA, QASM, QIR, etc.)

- Overview

## Transpilation and routing

draft; this section assumes the following topics are covered
- quantum circuits, generic overview
- quantum gates in a mathematical sense
- the notion of qubits

Now that we have a quantum circuit, it may seem like it should be straight-forward to "apply" it onto a physical quantum chip. But it's not; or at least, not usually.

When hardware vendors design and build quantum chips and control electronics, they usually have a small set of operations in mind. Let's call them "native operations" or "native gates". This set needs to be universal, in other words, it should be possible to represent any operation from the theory of quantum computing as a combination of native gates. 

This, once again, is very similar to logic gates of classical computers. If you're building a CPU, then you can choose to support `AND`, `OR` and `NOT` gates only. All other gates (e.g. `XOR`, `NAND`, etc.) can be expressed as combinations of those universal gates. 

Note that the choice of native quantum gates is not set in stone. It's not a physical property of the chip, or the manufacturing process. It's implied by those physical properties, but is ultimately driven by calibration. [TODO: refer to the calibration section; decide how to split the topics of calibration procedures and deriving quantum architectures]

- Generally, the process of re-expressing a circuit in terms of a specific set of gates is called "transpilation" or "synthesis"
	- Transpilation in computing usually refers to a process of converting source code from one language to another language on the same level of abstraction. For example, transpiling TypeScript code into JavaScript.
	- As opposed to compilation, which usually refers to a process of converting source code from one level of abstraction onto a lower level. For example, compiling Java code into bytecode.
- Quantum SDKs like Qiskit or Cirq have a transpiler module built in
- Transpilation should be combined with routing
	- The original circuit assumes all qubits are connected
	- In practice, superconducting QPUs have limited connectivity
		- [TODO: refer to chip topologies section of the modalities chapter]
	- We need an algorithm to
		- decide how to map logical qubits of the original circuit onto physical qubits on the QPU
			- note that by "logical qubits" here we don't mean QEC logical
	- add necessary SWAP operations
	- do it all in an efficient way, and minimize SWAPs
	- bonus goal: take into account real-time calibration and fidelity data in order to make the best choices of qubits
		- e.g. certain qubits have better quality gate `A`, while others have better quality gate `B`, which means not only connectivity matters

TODO: add a section on NISQ-level transpilation vs QEC-level transpilation
