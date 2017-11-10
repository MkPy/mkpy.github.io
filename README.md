# MkPy:  Maunakea Python Workshop 2017

The MkPy workshop has the goal of bringing together programmers and scientists from all of the Maunakea Observatories.  The general structure will be two days, each with a half day of talks and a half day of "unconference sessions".  We will have keynote speakers and a series of talks given by attendees.  The goal is to foster collaboration between scientists and programmers and across organizations.  The afternoon unconference sessions may include additional tutorials, lightning talks, discussion panels, and hack sessions.

# MkPy Agenda

Nov 8-9 at the Subaru Base Facility Conference Suite (650 N. Aohoku Pl, Hilo, HI)

### Agenda: Wednesday, Nov. 8

| Time | Session |
|------|---------|
| 08:30 | Coffee |
| 08:50 | SOC welcome and instructions for attendees, speakers |
| 09:10 | Keynote: Astropy and the Python in Astronomy Ecosystem (Erik Tollerud, Space Telescope Science Institute, member astropy project coordinators) |
| 10:00 | Invited Talk 1: (“Let them evolve!”: Automatic scheduling using Python and Biology)[mpohlen_PythonScheduling.pdf] (Michael Pohlen, Gemini Observatory) |
| 10:20 | Coffee break |
| 10:40 | Invited Talk 2: (Making a simple instrument utility using ginga and astropy)[joshw_CSU_initializer.pdf] (Josh Walawender, Keck Observatory) |
| 11:00 | Invited Talk 3: Using Flask to create simple, dynamic web pages (Sarah Graves, EAO Observatory) |
| 11:20 | Invited Talk 4: Remote Debugging with Advanced PyCharm Capabilities (Matt Wilson, CFHT Observatory) |
| 11:40 | Lightning Talks |
| 12:00 | Lunch (provided) |
| 13:00 | Unconference Sessions 1 |
| 14:00 | Unconference Sessions 2 |
| 15:00 | Coffee break |
| 15:30 | Unconference Sessions 3 |
| 16:30 | Unconference Sessions 4 |
| 17:30 | Unconference Wrap up |
| 18:00 | BBQ (and Potluck) |

### Agenda: Thursday, Nov. 9

| Time | Session |
|------|---------|
| 08:30 | Coffee |
| 09:00 | SOC call to order |
| 09:10 | Keynote: Redesigning LSST's Processing Middleware (Jim Bosch, Princeton University, Data Release Production Scientist with LSST) |
| 10:00 | Invited Talk 5: (Digital plumbing with Python/C)[KLanclos_DigitalPlumbingWithPhython.pdf] (Kyle Lanclos, W. M. Keck Observatory) |
| 10:20 | Coffee break |
| 10:40 | Invited Talk 6: (Parallel Processing in Python)[SKwok_ParallelProcessingInPython.pdf] (Shui Kwok, W. M. Keck Observatory) |
| 11:00 | Invited Talk 7: (Wrapping C Libraries with Cython)[berthold_cython.pdf] (Ryan Berthold, EAO Observatory) |
| 11:20 | Invited Talk 8:  Building Applications for Jupyter Notebooks (Eric Jeschke, National Astronomical Observatory of Japan) |
| 11:40 | Lightning Talks |
| 12:00 | Lunch (provided) |
| 13:00 | Unconference Sessions 5 |
| 13:45 | Unconference Sessions 6 |
| 14:30 | Coffee break |
| 15:00 | Unconference Sessions 7 |
| 15:45 | Unconference Sessions 8 |
| 16:30 | Workshop adjourned |

### Lightning talks

* (Kathleen Labrie: AstroData)[Kathleen_LabrieLightningMKPython.pdf]
* (Josh Walawender: Fun With DSLR Cameras)[joshw Lightning Talk DSLRs.pdf]


## Talk Abstracts

__Keynote: Astropy and the Python in Astronomy Ecosystem__ (Erik Tollerud, Space Telescope Science Institute, member astropy project coordinators)

I will describe recent and coming developments in the Astropy Project.  I will describe the Astropy workflow and summarize key elements that have allowed it to be successful in bringing together scientists and developers from around the globe.  I will also outline major areas of current activity in the Astropy Project, particularly progress in the spectroscopy and photometry packages.  I will also discuss some of the new planned organizational changes for Astropy that we hope will help foster further collaboration and interoperability in the Python astronomy community as a whole.

__Invited Talk 1: “Let them evolve!”: Automatic scheduling using Python and Biology__ (Michael Pohlen, Gemini Observatory)

I will present the result from my attempts to use Python's excellent object-oriented framework together with a multi-objective optimization method inspired by biology (Non-dominated Sorting Genetic Algorithm-II)  to optimally schedule a set of observations across a number of observing nights at a given telescope. The current version can optimize the schedule in regards to elevation (the higher, the better) and science band (the higher ranked, the better), but other goals can easily be added. Starting with a random distribution of schedules it evolves them by mating the best schedules per night creating children. These are then ranked together with their parents and the best ones mate for the next cycle in the evolution.

__Invited Talk 2: Making a simple instrument utility using ginga and astropy__ (Josh Walawender, W. M. Keck Observatory)

The ginga FITS viewer plugin architecture provides a tool to make instrument utilities with a graphical interface.  I’ll present a small project being written by non-programmers to create a powerful tool to assist nighttime trouble recovery on the MOSFIRE instrument on Keck 1.

The MOSFIRE Configurable Slit Unit (CSU) has a failure mode (called a “fatal error”) which is rare, but can take up to 90 minutes to recover.  Experienced support personnel with detailed knowledge of the CSU operation, can optimize the recovery process to significantly reduce the recovery time.  However, this faster recovery process involves a complex decision tree which must be repeated many times, so for all but the most experienced support personnel, the "fast" recovery process can end up taking nearly as long as the "slow" process and adds many opportunities for mistakes.  The features of this process (a decision tree repeated many times) make it ideal for a scripted solution, however because of the nature of the error, human oversight is critical, so a graphical tool is needed.  Our solution for this is a plugin for the ginga FITS "reference viewer".

__Invited Talk 3: Using flask to create simple dynamic web pages__ (Sarah Graves, EAO Observatory)

Frequently, it is very convenient to be able to quickly make dynamic monitoring web pages to keep track of e.g. observatory status, project completion etc. Flask is a python micro web framework which, together with Jinja2 templates makes small python web apps simple to create. This talk will provide a brief overview of how to use Flask and its ecosystem of plugins to quickly make a small web app monitoring information in an observatory database.

__Invited Talk 4: Remote Debugging with Advanced PyCharm Capabilities__ (Matt Wilson, CFHT Observatory)

Have you ever had a code problem which only presents itself in the production environment with real operating conditions? Have you spent hours brainstorming theories, adding log lines, reading tea leaves, and praying for divine intervention? In this talk we'll look at PyCharm's remote debugging capabilities, and show how it can be an indispensable tool for gaining visibility into unreproducible situations.

__Keynote: Redesigning LSST's Processing Middleware__ (Jim Bosch, Princeton University, Data Release Production Scientist with LSST)

LSST's pipeline software is built around a few core components: a configuration system based on executable Python files, a Task concept that allows algorithms to composed and configured at runtime, and a dataset management system we call the Butler.  Until recently, these have been very successful at enabling algorithm development and supporting mid-scale pipeline execution for data from a number of cameras.  The incremental, build-it-as-you-need it development approach to we'd taken doesn't seem to provide a way out of their current limitations, however, and over the past year, we have undertaken a major effort to redesign these components for the future.  In this talk, I'll describe the lessons learned from that story and the designs we'll be moving to in the future.

__Invited Talk 5: Digital plumbing with Python/C__ (Kyle Lanclos, W. M. Keck Observatory)

There are two common reasons for a Python programmer to augment their code with C: speed and compatibility with existing interfaces. Multiple options exist to blend the boundaries between Python and C, each with their own compromise with respect to elegance, performance, and control. This talk focuses on the pure control approach: readable code written in pure C using the Python/C interface. Specific examples will include the definition and unique utility of creating Python classes in C, integration with C-only interfaces using asynchronous events, and multiprocessing with the pthread library.

__Invited Talk 6: Parallel Processing in Python__ (Shui Kwok, W. M. Keck Observatory)

Python provides many ways to carry out tasks in parallel. In this talk, we will present two common approaches: threads and processes. We will show examples of synchronization and inter-process communication, as well as how to use pools. Python also provides the concept of asynchronous processing, which facilitate the structuring of large sequential programs.  We will present how to use generators and coroutines with examples.

__Invited Talk 7: Wrapping C Libraries with Cython__ (Ryan Berthold, EAO Observatory)

Cython, a static compiler for Python, makes it easy to write C extensions. Python code is translated to C and compiled as a shared library, which the interpreter then imports as a module. Static type declarations allow Cython to generate optimized loops that approach the performance of raw C code. Cython can also call C code directly, which makes it useful as a foreign function interface for wrapping external libraries.

At the JCMT we've created a Cython wrapper for DRAMA, the communication framework developed at the AAO, which is used in much of our instrument control software. The extension module gives Python scripts the ability to interact directly with existing DRAMA tasks, instead of relying on system calls to separate tools, and will allow pure-Python development of future control tasks and GUIs.

__Invited Talk 8: Building Applications for Jupyter Notebooks__ (Eric Jeschke, National Astronomical Observatory of Japan)

Jupyter Notebooks are a powerful tool for developing and documenting Python workflows.  With new modules being developed explicitly for the notebook environment it is enabling new possibilities for application deployment, documentation and collaboration.  In this talk I will describe and demonstrate one such new framework for running applications in the notebook.

## Attendee List

| Name | Affiliation |
|------|-------------|
| Al Honey | W. M. Keck Observatory |
| Andre-Nicolas Chene | Gemini |
| Andrew Weis | SMA |
| Anubhav Agarwal | IRTF/IfA |
| Benjamin Berkey | MLSO |
| Brian Force | SMA |
| Callie Crowder | CFHT |
| Carlos Alvarez | W. M. Keck Observatory |
| Catherine Ishida | UH Hilo |
| Charles Lockhart | IRTF/IfA |
| Chi-Hung Yan | ASIAA, Subaru |
| Christoph Baranec | IfA |
| Claire Moutou | CFHT |
| Dan Bintley | EAO/JCMT |
| Eric Jeschke | Subaru |
| Eric Takasugi | CERN |
| Etsuko Mieda | Subaru |
| Gianni Cataldi | Subaru |
| Harriet Parsons | EAO/JCMT |
| Hiroshige Yoshida | Subaru |
| Holly Thomas | SMA |
| Jessica Stasik | IfA |
| Ji Hoon Kim | Subaru |
| Jim Bosch | LSST/Princeton |
| Jon Chock | W. M. Keck Observatory |
| Josh Walawender | W. M. Keck Observatory |
| Julien Rousselle | Subaru |
| Justin Stevick | College of San Mateo |
| Kathleen Labrie | Gemini |
| Kristen Laguana | ASIAA |
| Kyle Lanclos | W. M. Keck Observatory |
| Laurie Rousseau-Nepton | CFHT |
| Layre CATALA | Gemini |
| Lee, Chien-Hsiu | Subaru |
| Luca Rizzi | W. M. Keck Observatory |
| Lucas Fuhrman | Gemini |
| Luke McKay | IfA |
| Mac Cooper | SMA |
| Maren Purves | EAO/JCMT |
| Mark Rawlings | EAO/JCMT |
| Masato Onodera | Subaru |
| Matt Taylor | Gemini |
| Matt Wilson | CFHT |
| Michael Lemmen | Subaru |
| Michael Pohlen | Gemini |
| Michael Radica | CFHT |
| Mike Connelley | IRTF/IfA |
| Miranda Hawarden-Ogata | IRTF/IfA |
| Miriam Fuchs | SMA |
| Mirko Simunovic | Gemini |
| Natalia Gonzalez | Gemini |
| Pascal Fouque | CFHT |
| Per Friberg | EAO/JCMT |
| Philip Tait | Subaru |
| Prashant Pathak | Subaru |
| Ramprasad Rao | ASIAA |
| Ranjani Srinivasan | ASIAA |
| Rita Morris | Subaru |
| Russell Kackley | Subaru |
| Ryan Berthold | EAO/JCMT |
| Sam Benigni | UKIRT |
| Sarah Graves | EAO/JCMT |
| Shui Hung Kwok | W. M. Keck Observatory |
| Siyi Xu | Gemini |
| Steve Mairs | EAO/JCMT |
| Thayne Currie | Subaru |
| Tim Jenness | LSST |
| Tsuyoshi Terai | Subaru |
| Watson P. Varricattu | UKIRT |
