// Flags staff members with high workload
let table = base.getTable("Staff");
let records = await table.selectRecordsAsync();

for (let record of records.records) {
    let events = record.getCellValue("Assigned Events");
    if (events && events.length > 5) {
        await table.updateRecordAsync(record.id, {
            "Notes": "High workload - review assignments"
        });
    }
}

