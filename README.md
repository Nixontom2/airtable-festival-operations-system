// Automatically generates a unique event code
let table = base.getTable("Events");
let record = await input.recordAsync("Select Event", table);

let name = record.getCellValue("Event Name");
let code = name.substring(0,3).toUpperCase() + "-" + Date.now();

await table.updateRecordAsync(record.id, {
    "Event Code": code
});



