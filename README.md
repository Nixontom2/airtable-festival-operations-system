// Bulk update event status
let table = base.getTable("Events");
let records = await table.selectRecordsAsync();

for (let record of records.records) {
    let status = record.getCellValue("Status");
    if (status && status.name === "Planning") {
        await table.updateRecordAsync(record.id, {
            "Status": { name: "Confirmed" }
        });
    }
}

