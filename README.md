# LinuxShell_fgbg
前景執行與背景執行

# foreground 前景執行

    $ fg 指令 參數 
    

    ➜  ~ git:(react2) ✗ ping google.com
    PING google.com (172.217.160.78): 56 data bytes
    64 bytes from 172.217.160.78: icmp_seq=0 ttl=55 time=4.340 ms
    64 bytes from 172.217.160.78: icmp_seq=1 ttl=55 time=4.430 ms
    64 bytes from 172.217.160.78: icmp_seq=2 ttl=55 time=4.864 ms
    
    ^Z
    
    [1]  + 2383 suspended  ping google.com
    
    
    ➜  ~ git:(react2) ✗ fg google.com
    fg: job not found: google.com
    ➜  ~ git:(react2) ✗ fg ping google.com
    [1]  + 2383 continued  ping google.com
    64 bytes from 172.217.160.78: icmp_seq=3 ttl=55 time=4.371 ms
    64 bytes from 172.217.160.78: icmp_seq=4 ttl=55 time=3.581 ms
    64 bytes from 172.217.160.78: icmp_seq=5 ttl=55 time=10.536 ms
    64 bytes from 172.217.160.78: icmp_seq=6 ttl=55 time=4.493 ms
    64 bytes from 172.217.160.78: icmp_seq=7 ttl=55 time=4.495 ms


# background 背景執行

    $ bg 指令 參數 


    ^Z
    [1]  + 2383 suspended  ping google.com
    fg: job not found: google.com
    
    ➜  ~ git:(react2) ✗ bg ping google.com
    [1]  + 2383 continued  ping google.com
    
    bg: job not found: google.com
    
    64 bytes from 172.217.160.78: icmp_seq=8 ttl=55 time=4.064 ms                   
    ➜  ~ git:(react2) ✗ 64 bytes from 172.217.160.78: icmp_seq=9 ttl=55 time=4.777 ms
    64 bytes from 172.217.160.78: icmp_seq=10 ttl=55 time=4.692 ms
    64 bytes from 172.217.160.78: icmp_seq=11 ttl=55 time=6.541 ms
    64 bytes from 172.217.160.78: icmp_seq=12 ttl=55 time=5.915 ms
    64 bytes from 172.217.160.78: icmp_seq=13 ttl=55 time=4.539 ms
