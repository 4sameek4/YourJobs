# Job Application Tracker Widget

A lightweight, offline Windows desktop widget for tracking job applications with an Excel backend.

## Features

✅ **Modern UI** - Clean, borderless widget with custom styling
✅ **Always-On-Top** - Stays visible above other windows
✅ **Bottom-Right Positioning** - Automatically positioned above the Windows taskbar
✅ **Excel Storage** - First-run file picker with auto-created workbook and columns
✅ **Error Handling** - Graceful handling of file access conflicts
✅ **Success Feedback** - Temporary success message with fade-out effect
✅ **Draggable** - Custom title bar allows repositioning
✅ **Tab Navigation** - Full keyboard support with Enter to submit

## Installation

### Run the EXE

1. Download `YourJobs.exe`
2. Download the '_internal' folder
3. Keep the 'YourJobs.exe' and '_internal' in the same directory
4. Double-click `YourJobs.exe` to launch — no Python installation required


## First Launch

- On first run, the widget will prompt you to pick where to save the Excel workbook
- That location is saved for your Windows user profile
- If the workbook doesn't exist yet, it will be created automatically

## Usage

1. **Launch the Widget**
   - The widget appears in the bottom-right corner
   - The cursor is automatically focused on the "Company Name" field

2. **Enter Application Details**
   - **Company Name**: Name of the company (required)
   - **Role**: Job title/position (required)
   - **URL**: Link to the job posting (optional)

3. **Submit Entry**
   - Click "Log Application" or press Enter
   - A success message appears and disappears after 4 seconds
   - Input fields clear automatically after successful submission

4. **Move the Widget**
   - Click and drag the title bar to reposition
   - Widget stays "always on top"

5. **Close the Widget**
   - Click the "×" button in the top-right corner

## Excel File Structure

The application creates or updates the Excel file at the location you choose on first launch.

### Columns (in order)
1. **Serial Number** - Auto-incrementing ID
2. **Applied Date** - Date in MM-DD-YYYY format
3. **Company Name** - Company name from input
4. **Role** - Job role/title from input
5. **Job Post URL** - URL from input

### Format
- Header row is formatted with blue background and white bold text
- Column widths are optimized for readability
- All dates are in MM-DD-YYYY format
- Serial numbers are auto-calculated based on row count

## Error Handling

### File Locked Error
If you see: *"The Excel file is currently open in another application"*
- Close the Excel file in the background
- Click "Log Application" again
- The application won't crash or lose data

### Missing Fields
If "Company Name" or "Role" is empty:
- A warning pop-up will notify you
- Complete the required fields and try again

## Troubleshooting

**Problem**: Widget appears offscreen
- **Solution**: Restart the application; it will reposition itself

**Problem**: Excel file not created
- **Solution**: Ensure the folder you chose is accessible and you have write permissions


## Performance Notes

- Lightweight (~5-10MB memory footprint)
- Ideal for continuous background operation
- Supports thousands of entries without performance degradation

## Future Enhancements

Potential improvements:
- Statistics dashboard (apps per company, date ranges, etc.)
- Search/filter functionality
- Data export options (CSV, PDF)
- Tray icon for minimization
- Application history view

## License

This project is provided as-is for personal use.
