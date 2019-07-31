# jasper-CSV-datasource-for-subreport

I have two reports in jaspersoft studio based on two different CSV files with different columns
I want show you how to fix display data on SubReport.
You have two sample file csv for subreport. noi_gui_3.csv with columns header. noi_gui_2 without column header
Add parameter to your main source report:
```
<parameter name="SUBREPORT_DATA_SOURCE" class="net.sf.jasperreports.engine.data.JRCsvDataSource" isForPrompting="false">
		<defaultValueExpression><![CDATA[new net.sf.jasperreports.engine.data.JRCsvDataSource(new File("C:\\Users\\VAN_HOAI\\JaspersoftWorkspace\\testFolder\\noi_gui_3.csv"))]]></defaultValueExpression>
	</parameter>
```

where C:\\Users\\VAN_HOAI\\JaspersoftWorkspace\\testFolder\\noi_gui_3.csv 

is file csv for subreport.
You need two sample csv files for subreport. 

noi_gui_3 one with column header, which use for data set in subreport

On file noi_gui_2 for main parameter without column. only have data.

-in property subreport past Data source Expression with $P{SUBREPORT_DATA_SOURCE}

https://files.laptrinhwebs.com/report_fix5d4130ab1078e.png

Thanks you.
