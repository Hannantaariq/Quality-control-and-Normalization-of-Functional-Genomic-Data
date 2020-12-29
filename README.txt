> library(ArrayExpress)
> files <- getAE("E-GEOD-44934", type="raw", path="DATA.DIR")
>  files <- files$rawFiles
> labels <- c(paste("C", c(1:11), sep=""), paste("T", c(1:11), sep=""))
> treatment <- c(rep("C", 11), rep("T", 11))
> desc.df <- data.frame(Sample=files, Label=labels, Treatment=treatment)
> write.table(desc.df, "description.txt", quote=FALSE, sep="\t", row.names=FALSE)
