# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Piecewise constant hazard models Use pchreg (pch) With (In) R Software
install.packages("pch")
library("pch")
pchreg = read.csv("https://raw.githubusercontent.com/timbulwidodostp/pchreg/main/pchreg/pchreg.csv",sep = ";")
# Estimation Piecewise constant hazard models Use pchreg (pch) With (In) R Software
z <- pchreg$z
y <- pchreg$y
d <- pchreg$d
x <- pchreg$x
model <- pchreg(Surv(z,y,d) ~ x, breaks = 10)
summary(model)
pred <- predict(model, type = "distr")
plot(pred$Surv, 1 - pnorm(y, 1 + x, 1 + x)); abline(0,1) 
# Piecewise constant hazard models Use pchreg (pch) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished