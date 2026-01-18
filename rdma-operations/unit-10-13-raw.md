# Unit 10 - 13 (Raw)

Unit 10 - Send and Receive

how to SR using RDMA

Send operation - receiver must be ready - Post request - for buffer -&#x20;

Post SR -> Over the wire - written into those buffer

in reliable transport, receiver will send acknowlegement that data has arrived

Send operation

when the sender is ready  - create the work requset - post in in send queue - work queue entry - point it in data we want send

when hardware sees the entry, send it over the wire - means it's on the way to the receive side

hardware generate completion queue entry

software check completion queue - get notification in the form of the work of completion means send is completed successfully



Unit 11 - RDMA Write

2nd type of RDMA operation

one-side operation

sender initiave operation - receive side sofwtare remained uninvolved

when the data arrives at the receives side - hardwware responsibile pinpoint the memory location...

hardware ...

<figure><img src="../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>



when the data arrives at the receive side, first look at memory registration and data should be ewriten into it, if allow, written into the location

hardware send back to sender and notify it that it's completed

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



Unit 12 - RDMA Read

3rd type of RDMA operation - RDMA Read

one side operation - but data lies on the receive side

when sender wants a data - sen da message containing location nad data it wanted

when message reaches receive side, hardware responsibile to read the data and send back to sender

when RDMA - hardware looks at memory registration where the data resides - it permitted, takes the data, read it, and send back to the sender





Unit 13 - Atomic Operations

4th type o RDMA oepration - ATomic operatin

rely on hardware capabilities to do several steps without any interruptions

hardware - fetch & add comparing swap

2 steps of fetch & add:

1. Fetch data from memory
2. Increase value

2 steps of Comparing swap;

1. Compare the current value
2. if Match - replace with new value



handled by the hardware on the receive side

when atomic operation arrrives - hardware check destination - permittted if -> atomic operation is executed



why do we need atomic operation?

eg. soup - taste it - missing salt

luckly there's salt in another room

but roommate would tends to taste everything you made when you're not arround and look for salt as well

then u add salt and go back for ur day

but roommate back - unaware and add salt&#x20;

Atomic operation - taste and add salt simultaneously - (remove interruptions)









Unit 13 - Knowledge Check



In RDMA read, where is the data to be read stored?

Question 1Select one:

On the sender’s work queue

On the wire – ready to be read and transferred

On the receiver’s memory

<i class="fa-check">:check:</i>

On the receiver’s work queue

#### Question 2

CorrectMark 1.00 out of 1.00![](https://academy.nvidia.com/theme/image.php/academi/core/1760247428/i/unflagged)Flag question

**Question text**

In RDMA write, which of the following is sent from the Sender to the Receiver?

Select the two most correct answers:

Question 2Select one or more:

A completion acknowledgment

The memory address it must be written to

<i class="fa-check">:check:</i>

The local memory address which the data was copied from

The data

<i class="fa-check">:check:</i>

#### Question 3

CorrectMark 1.00 out of 1.00![](https://academy.nvidia.com/theme/image.php/academi/core/1760247428/i/unflagged)Flag question

**Question text**

Why are atomic operations needed?

Question 3Select one:

Because salty soups are the worst

Atomic operations are easier for the hardware to handle

They allow for faster manipulation of data

They prevent interruption during sets of operations

<i class="fa-check">:check:</i><br>
