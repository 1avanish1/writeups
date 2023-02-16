# Cache Me Outside

Allocator

    An allocator is a module that manages the heap of a program. Thus, it is easier for a programmer to use it, through the malloc and free functions. In this post, we will review the glibc allocator, which is a fork of the ptmalloc2 allocator. However, there are more allocators, like jemalloc or tcmalloc.
Chunks

    Chunks, as the name suggests, are chunks of memory that can be used to store any type of data. This are allocated for the program by using the malloc, calloc or realloc functions, and released with free. Chunks are found in a memory region known as heap.
Heap

    A heap is a contigous region of memory which can be splitted to create chunks. Each heap belongs to an arena, and several can exists in the same program. The main heap is allocated in the memory region named [heap].
Arena

    A arena is composed by a malloc_state structure, where bins are stored, and one or several heaps. A program can hold many arenas, that are created when new threads are spawned. The initial arena is the main_arena.
Bins

    Bins are lists of chunks that are available to be used. There are different types of bins, that are used based on the situation. These are:

        Unsorted Bin -> Bin to insert chunks quickly, before insert them in other bins.

        Small bins -> For small chunks.

        Large bins -> For large chunks.

        Fast bins -> Cache bins for very small chunks.

        Tcaches -> Cache bins that allows to several threads to access to small chunks without blocking the arena.

Also, I will let explanations for some interesting phenomenons that happens in the memory management:

Consolidation

    It happens when a process asks for a chunk bigger than those that a small bin can contain (and also the fast bins). In the consolidation the chunks of the fast bins are moved to the unsorted bin, thus allowing these to merge between them to avoid fragmentation, since it is expected that the program will require big chunks.
Tcaches Recharging

    When the allocator is searching for chunks in a fast bin or an small bin, it takes the opportunity to moved as many chunks to the tcaches as it can. This also happens when it is discarding chunks from the unsorted bin. This way the tcaches are full of chunks and the locks of the arena are decreased.

In this post, I will describe these entities with more detail. However, in case you need more help to understand the topic, you can check the following resources:

    glibc wiki: MallocInternals

    Heap exploitation book

    Azeria Labs: Understanding the glibc heap implementation

    Understanding glibc malloc

Moreover, in order to practice, you should check the how2heap repository, which teach different heap exploiting techniques. 
