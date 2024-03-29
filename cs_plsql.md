# PLSQL Cheat Sheet

## Sources & Links
- [SQL*Plus Substitution Variables](https://blogs.oracle.com/opal/post/sql*plus-substitution-variables-define-variables-and-parameters-in-sql-queries#5_3)

## Controlers/Enablers
- `SET ECHO ON/OFF`
  - The SET ECHO statement controls whether or not the text of a file is displayed.
- `SET VERIFY ON/OFF`
  - The SET VERIFY statement is used to turn on and off the display of command lines that have had substitutions performed.
- `SET DEFINE ON/OFF`
  - <tbd>
- `SET TERM ON/OFF`
  - The SET TERMOUT statement controls the display of the output generated by statements executed from a file. 
- `SET SPACE 0`
  - The SET SPACE statement is used to specify how many spaces separate columns in displays and printouts. The default value is one (1).
- `SET FEEDBACK ON/OFF`
  - The SET FEEDBACK statement controls whether or not SQLPLUS displays the "x rows returned" messages. By default, feedback is on.
- `SET HEADING ON/OFF`
  - The SET HEADING statement controls the printing of headers for reports.
- `SET PAGES 10000`
  - The SET PAGESIZE statement sets the length of the report in lines.
- `SET LINE 10000`
  - The SET LINESIZE statement sets the default length for SQLPLUS script lines.
- `SET TRIMS ON/OFF`
  - The SET TRIMSPOOL statement determines whether SQL*Plus allows trailing blanks at the end of each spooled line.
- `SET SPOOL ON/OFF/FILENAME`
  - <tbd>
- `SET SERVEROUTPUT ON/OFF`
  - The SET SERVEROUTPUT statement controls whether or not serveroutput. It can be used to set limit.
    - `SET SERVEROUTPUT ON SIZE UNLIMITED`
    - `SET SERVEROUTPUT ON SIZE 10000`

## Others
- `REM` - meaning "REMOVE", inline comment or just unused/ignored row
- `ACCEPT`
- `DEFINE`
- `PROMPT` - write a comment, writes as serveroutput and spool
