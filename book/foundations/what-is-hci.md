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

```{admonition} Co-author note
:class: tip
The "five senses" list is a useful starting point, but HCI needs a richer one. We also sense
**temperature, pain, body position and movement (proprioception), balance (vestibular sense)** and internal
states. Proprioception is why you can type without looking at your hand, and the vestibular sense is why
VR can make people feel sick. **TODO:** decide whether to keep "five" as the hook and then expand it in
[The Human](the-human.md), or to introduce the fuller list here.
```

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

## Further reading

- {cite}`norman2013design`, chapters 1–2: affordances, signifiers, and why everyday things confuse us.
- See the [resource list](../appendix/resources.md).
