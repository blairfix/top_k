# top_k

`top_k` is an R function for finding the elements of one vector associated with the top k elements of another vector. 


### Inputs

* `sort_vec` = the vector that you would like to find the largest elements of
* `data_vec` = a vector of values associated with `sort_vec`. Think ordered pairs: (`sort_vec`, `data_vec`) 
* `k` =  the number of largest elements to be returned


### Output
`top_k` returns the `k` values of `data_vec` associated with the top `k` values of `sort_vec` (in descending order of `sort_vec`).


### Example:

```R
library(RcppArmadillo)
library(Rcpp)

sourceCpp("top_k.cpp")

sort_vec = c(10 , 2  , 3.5, 100, 4)
data_vec = c(3.0, 0.5, 2  , 2.1, 20)

# get elements in data_vec associated with
# 2 largest elements in sort_vec
top_k(sort_vec, data_vec, 2)

    [,1] [,2]
[1,]  2.1    3

```



### Installation
To use `top_k`, install the following R packages:
 * [Rcpp](https://cran.r-project.org/web/packages/Rcpp/index.html) 
 * [RcppArmadillo](https://cran.r-project.org/web/packages/RcppArmadillo/index.html) 

Put the source code (`top_k.cpp`) in the directory of your R script. Then source it with the command `sourceCpp('top_k.cpp')`.

