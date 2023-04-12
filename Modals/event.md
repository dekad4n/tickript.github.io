# Event Modal
Event modal used through creation of events, update of events processes. An event model has many fields, let's describe them.

## owner
owner field is a required string field. It is the public address of event creator

## coverImageURL
coverImageURL field is a required string field. We generally use cloudinary links for cover images. It is the image when you click an event.

## title
title field is a required string field. It is the title when you click an event.

## startDate
startDate field is a required string field (not Date!).

## endDate
endDate field is a required string field (not Date!).

## startTime
startTime field is a required string field (not Date!).

## endTime
endTime field is a required string field (not Date!).

## category
category field is foreign key of category names. It is a required string field. 

## description
description is a required string field.

## integerId
When we are creating event models, we wanted to have an integer id to send to chain. Since our contract doesn't work with string ids, we have created integerId field. This field is fed from an automatic sequence, therefore, you do not need to input it anywhere. The type of integerId is Number, and since it is automatically generated it is not required but always exists.