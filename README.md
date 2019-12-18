# WPFGlobalization
WPF Globalization/Localization relies on a utility called LocBaml.exe, which is still quite inconvinient

Commands
REM The current directory is bin\Debug

REM Step 1: Parse satellite assembly into CSV
LocBaml.exe /parse en-US\WPFGlobalization.resources.dll /out:1.csv

REM Step 2: Edit CSV, translate the localizable strings

REM Step 3: Generate satellite assembly for zh-CN, which takes the satellite assembly of neutral culture (en-US) and the translated material as input.

LocBaml.exe /generate en-US\WPFGlobalization.resources.dll /trans:1.csv /out: zh-CN /cul:zh-CN

See also: [Combine LocBaml and Resources in single satellite assembly](https://stackoverflow.com/questions/278121/combine-locbaml-and-resources-in-single-satellite-assembly)
