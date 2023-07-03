# LoggingAnalyzerRepro
Repro of issue with Microsoft.Azure.WebJobs

## Problem

Adding a reference to Microsoft.Azure.WebJobs somehow suppresses various analyzer warnings related to logging,
including `CA1727`, `CA2253` and `CA2254`.

The [WithoutReference](tree/main/src/WithoutReference) project correctly raises errors for these analyzers.

The [WithReference](tree/main/src/WithReference) project does not raise errors for these analyzers.
