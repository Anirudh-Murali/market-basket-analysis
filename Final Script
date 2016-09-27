require(arules)
require(arulesViz)

#load the dataset and convert it into a sparse matri
data <- read.csv("groceries.csv")
Groc <- read.transactions("groceries.csv", sep=',')

#graphs
png(file = "mostBought.png")
itemFrequencyPlot(Groc , topN = 5)
dev.off()
png(file = "support.png")
itemFrequencyPlot(Groc , support = 0.10)
dev.off()

data(Groceries)
rules <- apriori(Groceries, parameter=list(support=0.005, confidence=0.5))
rules
## Scatterplot
##plot(rules)
inspect(sort(rules, by = "lift")[1:10])

##png(file = "comparison.png")
##plot(rules)
##dev.off()

#plot(rules, measure=c("support", "lift"), shading="confidence")
