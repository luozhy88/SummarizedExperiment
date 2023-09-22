# 安装和加载SummarizedExperiment包（如果尚未安装）
install.packages("SummarizedExperiment")
library(SummarizedExperiment)

# 创建虚构的基因表达矩阵
set.seed(123)
num_genes <- 1000
num_samples <- 10

gene_names <- paste("Gene", 1:num_genes, sep = "")
sample_names <- paste("Sample", 1:num_samples, sep = "")

expression_matrix <- matrix(rnorm(num_genes * num_samples), nrow = num_genes)
colnames(expression_matrix) <- sample_names
rownames(expression_matrix) <- gene_names

# 创建样本信息数据框
sample_info <- data.frame(
  SampleName = sample_names,
  Condition = factor(rep(c("Control", "Treatment"), each = num_samples/2))
)

# 创建SummarizedExperiment对象
se <- SummarizedExperiment(
  assays = list(counts = expression_matrix),
  colData = sample_info
)

# 查看SummarizedExperiment对象的摘要
se
