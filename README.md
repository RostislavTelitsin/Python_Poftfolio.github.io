# Rostislav Telitsin Python Portfolio
python portfolio

All my projects in python are developed for internal using only and ralated to my current work of support team. That's why I cannot publish them. But I can breafly describe the methods I used to create them

## OS and files

Sometime I need to work with some files, uzip them and rename. For example this part of code renames all "*.dat" files using serial number contained in the file
~~~
for file in files:
    if file[-3:]=='dat':
        f = open(file, 'r', encoding="utf-8")
        serial_num = f.readlines()[14]
        serial_num = serial_num.split('\"')[1]
        print(serial_num)
        for row_num in range (1, sheet.max_row + 1):
            if sheet.cell(row=row_num, column=2).value == serial_num:
                print(sheet.cell(row=row_num, column=1).value)
                new_filename = sheet.cell(row=row_num, column=1).value + "_" + file
                print(new_filename)
        f.close()
        os.rename(file, new_filename)

~~~
