# Casino

die <- 1:6
roll <- function(roll) {sample(x=die,size=2,replace=TRUE)}
replicate(10, roll())
qplot(x=replicate(100,roll()),binwidth=0.5)

wroll <- function(wroll) {sample(x=die,size=5,replace=TRUE,prob=c(0.5/6, 1/6,1/6,1/6,1/6,4/6))}
qplot(x=replicate(100000,wroll()),binwidth=0.5)

