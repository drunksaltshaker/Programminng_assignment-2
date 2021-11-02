# Programminng_assignment-2
makecachematrix <- function(m = matrix()) {
  n <- NULL
  
  set <- function(matrix) {
    m <<- matrix
    n <<- NULL
  }
  
  get <- function() {m
    }
  setInverse <- function(Inverse) 
    i <<- Inverse
  
  getInverse <- function() {i
  }
  
  list(set = set, get = get,
       setInverse = Inverse,
       getInverse = getInverse)
}

cachemean <- function(x, ...) {
  m <- x$getInverse()
  if(!is.null(m)) {
    message("getting cache data")
    return(m)
  }
  
  data <- x$get()
  m <- solve(data)%%data
  x$setInverse(m)
  m
  
}
