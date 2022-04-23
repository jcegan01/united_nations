# A fun welcome message
message("Hi Jeff, welcome to R")
# Customise the R prompt that prefixes every command
# (use " " for a blank prompt)

#prompt and additonal settings
options(prompt = "un>", digits =4, continue = "  ")
#Ever been frustrated by unwanted + symbols that prevent copied and pasted multi-line functions from working? These potentially annoying +s can be eradicated by adding options(continue = " ") to your .Rprofile.


# `local` creates a new, empty environment
# This avoids polluting .GlobalEnv with the object r
# local({
#   r = getOption("repos")
#   r["CRAN"] = "https://cran.rstudio.com/"
#   options(repos = r)
# })
#The RStudio mirror is a virtual machine run by Amazon’s EC2 service, and it syncs with the main CRAN mirror in Austria once per day. Since RStudio is using Amazon’s CloudFront, the repository is automatically distributed around the world, so no matter where you are in the world, the data doesn’t need to travel very far, and is therefore fast to download.

#quote during startup
if(interactive()) 
  try(fortunes::fortune(), silent = TRUE)

# new functions that may be useful.
# ht == headtail
hashbind <- function(..., hash = "-") {
  lst <- list(...)
  Nchar <- max(rapply(lst, function(y) nchar(as.character(y)))) + 2
  do.call(
    rbind, 
    lapply(lst, function(x) {
      rbind(x, substr(paste(rep(hash, Nchar), collapse = ""), 1, Nchar))
    }))
}
ht = function(d, n=5) hashbind(head(d, n), tail(d, n))

