# SCEDBayesGithubLocal
library(devtools)
devtools::install("~/Desktop/SCEDbayes")
library(SCEDbayes)
dat = subset(LAMBERT, LAMBERT$STUDENT==1)
y = dat$DATA.POINT; P = dat$PHASE; s = dat$SESSION;
model1 = ABABmodel(y, P, s, model = 'trend', diagnostics = TRUE) # Intercepts only model
