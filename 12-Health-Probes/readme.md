Probes :- it is a some process that monitoring our system,and taking some necessary action, and 
        grep some status like every things is working properly or not..


        liveness : if our system cresh and problem solve by restarting it, than this prob is take care of that..
            means something went wrong with your application..

        readiness : check if you application is ready before you system actually serve a traffic..

        startup : some application take more time too start.. (like your application wait for sometime after it's get ready..)

        sequece:- 
        startup prob => readiness prob => liveness prob
        executing in this flow..




we can perform 3 type of health check :-
    http, tcp or command