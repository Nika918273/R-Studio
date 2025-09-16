3MMA

library(zoo)
unemployment <-c(3.4, 3.8, 4.1, 4.0, 3.5, 3.6, 3.7, 3.6, 4.1, 4.1, 3.9, 3.6, 3.7, 3.8, 4.0, 4.2)
mma3 <- rollmean(unemployment, 3, fill = NA, align = "right")
mma3


unemployment curve


values <- c(3.4, 3.8, 4.1, 4.0, 3.5, 3.6, 3.7, 3.6, 4.1, 4.1, 3.9, 3.6, 3.7, 3.8, 4.0, 4.2)
time <- 1:length(values)
plot(time, values, type = "o", col = "blue", lwd = 2,
xlab = "months",
ylab = "Unemployment rate",
main = "unemployment")
grid()


HP filter

library(hpfilter)
y = data.frame(gdp=c(18279.784,18401.626,18435.137,18525.933,18711.702,18892.639,19089.379,19280.084,19438.643,19692.595,20037.088,20328.553,20580.912,20798.730,20917.867,21111.600,21397.938,21717.171,21933.217,21727.657,19935.444,21684.551,22068.767,22656.793,23368.861,23921.991,24777.038,25215.491,25805.791,26272.011,26734.277,27164.359,27453.815,27967.697,28296.967,28624.069,29016.714,29374.914,29723.864,29962.047,30353.902))
ytrend = hp2(y)
ycycle = y - ytrend
plot(y$gdp, type="l", col="black", lty=1)
lines(ytrend$gdp, col="#066462", lwd=2)
legend("topleft", legend=c("GDP","Trend"),
col=c("black","#066462"), lty=1, lwd=2, bty="n")
plot(x, type="l", col="blue", lwd=2)
abline(h=0, col="red", lty=2)
                                               
                           
