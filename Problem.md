## Display student information using different data types:
    START
    INITIALIZE studentName AS STRING
    INITIALIZE rollNumber AS INTEGER
    INITIALIZE gpa AS FLOAT
    INITIALIZE section AS CHARACTER

    OUTPUT "Enter student name: "
    INPUT studentName

    OUTPUT "Enter roll number: "
    INPUT rollNumber

    OUTPUT "Enter GPA: "
    INPUT gpa

    OUTPUT "Enter section: "
    INPUT section

    DISPLAY "Name: " + studentName
    DISPLAY "Roll Number: " + rollNumber
    DISPLAY "GPA: " + gpa
    DISPLAY "Section: " + section
    END

## Read and display a character using getchar() and putchar():
    START
    DECLARE ch AS CHARACTER

    OUTPUT "Enter a character: "
    ch = getchar()

    OUTPUT "You entered: "
    putchar(ch)
    END

## Display a floating-point value using different precision settings:
    START
    DECLARE num AS FLOAT

    OUTPUT "Enter a floating-point number: "
    INPUT num

    DISPLAY num WITH 0 DECIMAL PLACES
    DISPLAY num WITH 1 DECIMAL PLACE
    DISPLAY num WITH 2 DECIMAL PLACES
    END
