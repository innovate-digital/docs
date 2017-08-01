# Expecting data types

## User
A data type describing an user profile.

Field | Optional? | Description
------------ | ------------- | -------------
id | No | The user id
username | No | The username - an alias for _ID_
phone | No | The phone of the user
personalId | _No?_ | The extra id of the user
password | _No?_ | The password of the user
firstName | No | The first name of the user
lastName | No | The last name of the user
email | Yes | The email of the user
avatar | Yes | The user's avatar

## Course
A data type describing common course information. Can be mentioned as `subject`

Field | Optional? | Description
------------ | ------------- | -------------
id | No | The id of the course
department | No | The name of the department of the course
courseName | No | The name of the course
teacherName | No | The name of the teacher
credits | No | The credits of the course as _'0.0'_ string

## Lesson
A data type describing common lesson information. Should be extended with `Course` data.

Field | Optional? | Description
------------ | ------------- | -------------
id | No | The id of the lesson
startDate | No | The lesson's date of start in _ISO 8601 format_,
endDate | No | The lesson's date of start in _ISO 8601 format_,
roomId | Yes | The id of the lesson's room
roomDescription | Yes | The description of the lesson's room
status | Yes | The status of the record

**Lesson extra fields**

Field | Optional? | Description
------------ | ------------- | -------------
courseId | No | The id of the course
department | No | The name of the department of the course
courseName | No | The name of the course
teacherName | No | The name of the teacher
credits | No | The credits of the course as _'0.0'_ string


## Exam
A data type describing common exam information. Should be extended with `Course` data.

Field | Optional? | Description
------------ | ------------- | -------------
id | No | The id of the exam
moed | Yes | The moed of the exam as _number_
semester | Yes | The semester of the exam as _number_ or _zero_ if _annual_
startDate | No | The exam's date of start in _ISO 8601 format_,
endDate | No | The exam's date of start in _ISO 8601 format_,
roomId | Yes | The id of the exam's room
roomDescription | Yes | The description of the exam's room
status | Yes | The status of the record
type | Yes | The type of exam

**Exam extra fields**

Field | Optional? | Description
------------ | ------------- | -------------
courseId | No | The id of the course
department | No | The name of the department of the course
courseName | No | The name of the course
teacherName | No | The name of the teacher
credits | No | The credits of the course as _'0.0'_ string

## Grade

Field | Optional? | Description
------------ | ------------- | -------------
type | Yes | The type of the grade
credits | Yes | The email of the user
moed | Yes | The phone of the user
failed | Yes | The firstName of the user
value | Yes | The lastName of the user
semester | Yes | The userPicture of the user

**Grade extra fields**

Field | Optional? | Description
------------ | ------------- | -------------
courseId | No | The id of the course
department | No | The name of the department of the course
courseName | No | The name of the course
teacherName | No | The name of the teacher
credits | No | The credits of the course as _'0.0'_ string

## Message
A data type describing a message.

Field | Optional? | Description
------------ | ------------- | -------------
title | No | The title of the message
message | No | The message content
attachment | Yes | The attachment of the message as _link_
sender | Yes | The name of message sender
createAt | No | The createdAt date in _ISO 8601 format_,
updatedAt | No | The updatedAt date in _ISO 8601 format_,

**Message extra fields**

Field | Optional? | Description
------------ | ------------- | -------------
courseId | No | The id of the course
department | No | The name of the department of the course
courseName | No | The name of the course
teacherName | No | The name of the teacher
