# angular-1515
匯出excel:
onExportDataAsExcel() {
		const params = {
			allColumns: true,
			columnGroups: true
		};
		this.getGridOptions().api.exportDataAsExcel(params);
    };
generateColumns() {
        this.colunbDefs.push(
            {
                headerName: this.translateService.instant(''),
                field: '',
                width: 150,
                sortable: true,
                suppressSizeToFit: true,
            });
 setGridOption() {
		this.getGridOptions().onGridReady = () => {
			this.getGridOptions().api.setColumnDefs(this.generateColumns());
			this.reloadRows();
		};
	}
  
 日期:
 days:
 moment(new Date()).add(-7,'days').toDate()
 months:
 years:
    

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/angular-1515)
