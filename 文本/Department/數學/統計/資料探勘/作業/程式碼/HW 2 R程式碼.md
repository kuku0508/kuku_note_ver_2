# (1)
#設定函式
splitdata = function(data,p=0.9,seed)
{
set.seed(seed)
index = sample(2,nrow(data),replace = TRUE,prob = c(p,1-p))  
train = data[index == 1,]
test = data[index == 2,]
out = list(train=train,test=test)
return(out)
}

# 測試函式跟種子有沒有可以
test_out <- splitdata(iris,0.7,1027)
test_train <- test_out$train
test_test <- test_out$test
nrow(test_train)
nrow(test_test)
head(test_train,5)
head(test_test,5)

#匯入資料
raw_data <- read.csv("C:/Users/kuku/Downloads/heartdisease.csv")
out <- splitdata(raw_data,0.7,1027)
train <- out$train
test <- out$test

variable.names(out$train)
# (2)
summary(train$Age)

# AI footstep 我在想除了用14個summary以外，
# 還有什麼比較簡潔的方法，所以我問了chatgpt
