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
credits | No | The credits of the course

## Lesson
A data type describing common lesson information. Should be extended with `Course` data.

Field | Optional? | Description
------------ | ------------- | -------------
id | No | The id of the lesson
startDate | No | The lesson's date of start in _YYYY-MM-DDThh:mm:ss format_,
endDate | No | The lesson's date of start in _YYYY-MM-DDThh:mm:ss format_,
roomId | Yes | The id of the lesson's room
roomDescription | Yes | The description of the lesson's room
status | Yes | The status of the record
courseId | No | The id of the course

## Exam
A data type describing common exam information. Should be extended with `Course` data.

Field | Optional? | Description
------------ | ------------- | -------------
id | No | The id of the exam
moed | No | The moed of the exam as _number_
semester | Yes | The semester of the exam as _number_ or _zero_ if _annual_
startDate | No | The exam's date of start in _YYYY-MM-DDThh:mm:ss format_,
endDate | No | The exam's date of start in _YYYY-MM-DDThh:mm:ss	format_,
roomId | Yes | The id of the exam's room
roomDescription | Yes | The description of the exam's room
status | Yes | The status of the record
type | Yes | The type of exam
courseId | No | The id of the course

## Grade

Field | Optional? | Description
------------ | ------------- | -------------
id | No | The id of the grade
userId | No | The id of the user
type | Yes | The type of the grade
credits | Yes | The email of the grade
moed | Yes | The moed of the grade
failed | Yes | The failed of the grade, as boolean
value | Yes | The value of the grade
semester | Yes | The semester property of the grade
courseId | No | The id of the course

## Message
A data type describing a message.

Field | Optional? | Description
------------ | ------------- | -------------
id | Yes | The id of the message
userId | No | The id of the user
title | No | The title of the message
message | No | The message content
attachment | Yes? | The attachment of the message as _link_
sender | Yes | The name of message sender
createAt | No | The createdAt date in _YYYY-MM-DDThh:mm:ss	format_,
updatedAt | No | The updatedAt date in _YYYY-MM-DDThh:mm:ss	format_,
courseId | Yes | The id of the course

# JSON
```
{
  "users": [
    {
      "id": "string",
      "username": "string",
      "phone": "string",
      "password": "string",
      "firstName": "string",
      "lastName": "string",
      "email": "string",
      "avatar": "string",
      "lessons": [
        {
          "id": "string",
          "courseId": "string",
          "groupId": "string",
          "startDate": "string",
          "endDate": "string",
          "roomId": "string",
          "roomDescription": "string",
          "status": "string",
          "department": "string",
          "name": "string",
          "credits": "string",
          "teacherName": "string"
        }
      ],
      "exams": [
        {
          "id": "string",
          "courseId": "string",
          "groupId": "string",
          "startDate": "string",
          "endDate": "string",
          "roomId": "string",
          "roomDescription": "string",
          "status": "string",
          "department": "string",
          "name": "string",
          "credits": "string",
          "teacherName": "string",
          "moed": "string",
          "type": "string"
        }
      ],
      "grades": [
        {
          "id": "string",
          "courseId": "string",
          "department": "string",
          "name": "string",
          "credits": "string",
          "teacherName": "string",
          "values": [
            {
              "id": "string",
              "type": "string",
              "credits": "string",
              "moed": "string",
              "failed": "boolean",
              "value": "string",
              "semester": "string"
            }
          ]
        }
      ]
    }
  ],
  "courses": [
    {
      "id": "string",
      "department": "string",
      "name": "string",
      "credits": "string",
      "teacherName": "string"
    }
  ]
}
```

# XML
```
<?xml version="1.0" encoding="UTF-8" ?>
<root>
	<users>
		<id>string</id>
		<username>string</username>
		<phone>string</phone>
		<password>string</password>
		<firstName>string</firstName>
		<lastName>string</lastName>
		<email>string</email>
		<avatar>string</avatar>
		<lessons>
			<id>string</id>
			<courseId>string</courseId>
			<groupId>string</groupId>
			<startDate>string</startDate>
			<endDate>string</endDate>
			<roomId>string</roomId>
			<roomDescription>string</roomDescription>
			<status>string</status>
			<department>string</department>
			<name>string</name>
			<credits>string</credits>
			<teacherName>string</teacherName>
		</lessons>
		<exams>
			<id>string</id>
			<courseId>string</courseId>
			<groupId>string</groupId>
			<startDate>string</startDate>
			<endDate>string</endDate>
			<roomId>string</roomId>
			<roomDescription>string</roomDescription>
			<status>string</status>
			<department>string</department>
			<name>string</name>
			<credits>string</credits>
			<teacherName>string</teacherName>
			<moed>string</moed>
			<type>string</type>
		</exams>
		<grades>
			<id>string</id>
			<courseId>string</courseId>
			<department>string</department>
			<name>string</name>
			<credits>string</credits>
			<teacherName>string</teacherName>
			<values>
				<id>string</id>
				<type>string</type>
				<credits>string</credits>
				<moed>string</moed>
				<failed>boolean</failed>
				<value>string</value>
				<semester>string</semester>
			</values>
		</grades>
	</users>
	<courses>
		<id>string</id>
		<department>string</department>
		<name>string</name>
		<credits>string</credits>
		<teacherName>string</teacherName>
	</courses>
</root>
```
