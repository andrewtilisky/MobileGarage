# MobileGarage
An app that uses info about your vehicles to alert you to probable maintenance dates

The app features a handful of views for the user to view their 'garage', add vehicles to it, view service events, and schedule new events.

The code largely consists of the necessary view controllers and model classes. To enforce a separation of concerns, PList operations are refactored to PListUtils.swift, which also dictates the markup schema. iOS 8-compatible Cloudkit key-value storage logic is still in AddVehicleViewController.swift. That logic is not complete because there was no practical iOS 8 device to work with.

![add](http://i.imgur.com/wwpSlRN.png)

Add a vehicle to your garage, including a few necessary parameters.

![view](http://i.imgur.com/ZAaDU84.png)

Once it's been added, you can input your weekly mileage manually or calibrate a trip.  This feature uses Swift's CoreLocation framework.

![event](http://i.imgur.com/PTnH7ji.png)

Add maintenance events like oil changes, tire rotations, and other inspections.

![Imgur](http://i.imgur.com/FN5JZKj.png)

Based on your weekly mileage and the distance between service events, the app calculates a probably date by which the maintenance should be performed.

Unfinished features include:
1. Deleting vehicles
2. Deleting maintenance events
3. Kicking off notifications correctly.
4. Implementing iCloud key-value storage.  This isn't feasible without an iOS 8 device and $99 Developer license.
