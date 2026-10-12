# What is Human–Computer Interaction?

```{admonition} Status: Draft
:class: note
First draft based on the author's notes. Items marked **TODO** are open for the next writing session.
```

```{admonition} Learning objectives
After this chapter you should be able to:
- define *human*, *computer* and *interaction* in the context of HCI, and say why each definition matters;
- name the human senses and explain why they bound what an interface can communicate;
- compare spoken, written and manual (mouse, touch) interaction in terms of naturalness and fidelity;
- argue, with an example, why the best interface is often the simplest one.
```

To answer the question "what is HCI?", it helps to take the three words one at a time.

## Human

We are the users. We have a limited set of channels to understand and act on the external world. The classic
list is five senses: **sight, hearing, touch, smell and taste**. An interaction has to be delivered
through one of them. Anything outside what we can see, hear or otherwise sense, such as infrared light or
ultrasound, is not perceived in the first place, so we cannot interact with it directly. A sensor can
translate it into something we *can* perceive, but then the translation is the interface.

Strictly, the list is longer. We also sense **temperature, pain, body position and movement
(proprioception)** and **balance (the vestibular sense)**. These matter, but for interaction with computers
the first five are the most important, and above all **sight and hearing**: so far, these are the two
channels through which computers communicate with us almost entirely. The extended list is picked up again
in [The Human](the-human.md).

The computer side is just as uneven. Computers have mature sensors for sight (cameras) and hearing
(microphones). For touch there has been some development, driven by robotics (pressure and tactile sensors)
and by vibration sensors, but it is still quite limited. For **smell and taste** there are no good
computational sensors at all in comparison. This asymmetry is one reason interfaces are overwhelmingly
visual and auditory.

Humans are also not only receivers. We **act**: we speak, type, point, gesture, look, and (in the
research settings of Part V) generate brain signals. HCI is concerned with both directions, *input* and
*output*, and with the loop between them.

## Computer

A computer is an electrical machine, not a biological one. It runs on binary hardware: everything it senses,
stores and does is ultimately encoded as bits.

For most of computing history, computers did exactly what a human programmer specified, step by step: an
algorithm is a clear set of instructions. That is no longer the whole picture. With modern AI, computers
can **learn** behaviour from data instead of following hand-written rules. This changes HCI in a deep way:

- the computer's behaviour can be *surprising*, even to its designers;
- it can adapt to the individual user, for better (personalisation) or worse (manipulation);
- its reach now touches individuals, institutions, and society as a whole.

This is why this book gives AI its own Part ([Part IV](../ai/conversational-agents.md)) rather than a closing
section.

## Interaction

Interaction is the loop between the two: the human perceives something, decides, acts, and the computer
senses that action, processes it, and responds. Where and how this loop happens defines the interface.

### An example: how the author interacted today

Take this very text. It is being typed on a **keyboard**, in **English**, to a language-model agent running in
a **browser**, which sends the prompt to a server. Several interaction choices are hidden in that sentence:

- *Typing* could be replaced by *speaking* into a microphone. Which is better?
- *English* is a natural language, but not the only possible command language.
- The *browser* is a layer of interface between the user and the model.

### Spoken versus written language

Speech has a far longer history than writing, and it is what children learn first, before they can read
or write. It is arguably what distinguishes us from other animals, which makes it feel **natural**.

Writing came later and gave us something speech cannot: **fidelity across time and people**. Knowledge can be
passed to later generations without being lost or deliberately altered when it is quoted from one person
to the next. Written language preserves information better than spoken language.

So which is the better *interface*? It depends:

| | Speech | Writing |
|---|---|---|
| Learned | Early, effortlessly | Later, with instruction |
| Speed of production | Fast | Slower |
| Fidelity / permanence | Low (unless recorded) | High |
| Privacy in public | Poor | Good |
| Editing before sending | Hard | Easy |
| Hands/eyes free | Yes | No |

Personal preference matters too. The author mostly avoids voice commands and does not send voice messages
on messaging apps, because a written message is more concise and easier to scan. Other people find voice
easier. **There is no universally best modality**, and one of the lessons of HCI is that preferences,
context and ability all matter.

```{admonition} Question for discussion
:class: seealso
You are cooking, hands covered in flour, and want to set a timer. Which modality do you want? Now you are
on a crowded train and want to reply to a message. Which one now? What changed?
```

### The same person, many interactions

In a normal day the author's interactions with computers are mostly digital where they used to be analogue
(messaging, calling), and mostly through **mouse, keyboard and touch**. These three have lasted for decades
because they are precise, private, and low in effort. **TODO:** add a short history timeline (punch cards →
command line → GUI/WIMP → touch → voice/LLM → …).

### Simplicity is a merit

Consider a **baby monitor**. Would you want a language-command interface on it? Probably not: three buttons
are enough (power, volume, perhaps a light). The temptation in modern product design is to add
capabilities (voice, apps, accounts, notifications) because they are *possible*. HCI asks instead whether
they are *needed* for the task and the user.

```{admonition} Design principle: simplicity
:class: important
The right amount of interface is the *least* that lets the intended user do the intended task, reliably,
in their real context. Added complexity has costs in learning, errors, failure modes, and (for connected
devices) privacy and security.
```

### Another example: a coffee machine

We recently bought a coffee machine and we are happy with it. It has four functions: **espresso, coffee,
hot water and steam**. For the first two you choose the strength of the coffee and the mug size, and then
you press play. That is about the right amount of interface.

Even a good design leaves room for improvement:

- **Communicating what the machine is doing.** When it starts, it cleans its pipes. That is great, but
  nothing tells the user. I know it by now; a first-time user, such as a guest, does not, and may wonder
  whether the machine is broken.
- **Redundant options.** You can choose "double espresso" and "espresso", but you can already choose the cup
  size and the strength. The difference between the two is the quantity of coffee, which is what the mug
  size already expresses.
- **Automatic switch-off.** The machine turns itself off after a timer. This could be improved by showing
  when it will switch off, perhaps with natural language: "switching off soon, any last coffee?", like the
  last call for drinks in a British pub.

Now the opposite temptation. Do you want to make your coffee machine more complicated? Connect it to the
internet, so that it orders coffee beans by itself when the bin is nearly empty? Order a coffee from your
phone while you are working upstairs, and be notified when it is ready? That saves perhaps one minute of
your life. Is it worth the added complexity, the account, the failure modes and the privacy risk? This is
the real question of HCI: not *what is possible*, but *what is the point*.

### When "smart" systems frustrate

Not all computer interaction is as benign as a coffee machine. My flight from Manchester to Frankfurt was
cancelled the other day and I had to rebook through the airline's online chatbot. It simply went round in
loops, with no way back. It was not smart at all.

By *smart* I mean **flexible**: trying to find a solution to *my* problem. This system was a simple state
machine with about five states that could not foresee any other path. Humans are not like that: we find a
way. When I called an assistant, they helped me rebook one way or another. We do not want computer systems
that leave us frustrated and stuck.

```{admonition} Question for discussion
:class: seealso
Sketch the chatbot as a state machine: what states and transitions would you need so that the user is
never trapped? What should it do when the user's problem is not in any of its states?
```

## Putting it together

A working definition for this book:

> **Human–computer interaction** is the study and design of how people and computational systems exchange
> information and influence each other in order to get something done, through the human's senses and
> actions on one side, and the computer's sensors, computation and outputs on the other.

## Exercises

1. **Inventory.** For one day, list every computer you interact with (phone, laptop, car, fridge, ticket
   machine…). For each, note the input modality and output modality. Which interactions did you not
   consciously notice?
2. **Modality swap.** Pick a task you do by typing (e.g. set an alarm). Do it by voice. Time both and note
   errors, effort and how you felt. When would you choose each?
3. **Less is more.** Take a gadget with too many features. Design (on paper) a version with at most three
   controls. What did you remove, and who loses out?
4. **Beyond the senses.** Which interactions might use senses beyond the classic five? Name two products
   that do.
5. **Improve a machine.** Pick an appliance at home (coffee machine, washing machine, microwave). List
   what it fails to communicate to a first-time user, and which of its options are redundant.
6. **Escape the loop.** Find an automated phone or chat system that trapped you. Which path was missing?

## Further reading

- {cite}`norman2013design`, chapters 1–2: affordances, signifiers, and why everyday things confuse us.
- See the [resource list](../appendix/resources.md).
