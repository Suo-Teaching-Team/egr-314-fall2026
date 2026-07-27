---
title: Web Interaction Design
---


* [MQTT Topic Naming Best Practices](https://www.hivemq.com/blog/mqtt-essentials-part-5-mqtt-topics-best-practices/)
* [Team Topic Table (template)](https://www.dropbox.com/s/pdt82mkwr3oty3o/Team%20Topic%20Table%20%28template%29.xlsx?dl=0)

### MQTT

MQTT uses topics to organize and route messages between publishers and subscribers. A topic is a string that identifies the subject of the message being published or subscribed to. Topics are structured as a hierarchy of topic levels, separated by forward slashes (/).

For example, a topic could be structured as follows:

```
/devices/sensor1/temperature
```

In this example, "devices" is the top-level topic level, "sensor1" is a sub-topic level, and "temperature" is a sub-topic level under "sensor1".

Please read through the [MQTT Topic Naming Best Practices](https://www.hivemq.com/blog/mqtt-essentials-part-5-mqtt-topics-best-practices/) link to learn more about MQTT naming conventions, separators, wildcards, etc.


1. **Create a table describing your team's published topics.** Make a copy of the team topic table template, and enter the following information, for each topic your team publishes:
    1. **Team #**
    1. **Team Name:** Enter the team's name
    1. **Topic:** Please use the following format: *"EGR314/TeamXYZ/MyTopicName1"* where XYZ are your initials and MyTopicName1 is a custom topic name of your team's choosing. For each topic, include

        > Note: Multiple values can be published to topics, so you will need to state what values will be sent, in what order, and the character(s) that will separate them.

        1. **Entities Publishing** to this topic.  What devices will be sending data (publishing) to this topic?  (ex: Main Board, Secondary Board, Phone, PC, etc)
        1. **Entities Subscribing** to this topic. What devices will be receiving data published to this topic? (ex: Main Board, Secondary Board, Phone, PC, etc)
        1. **Topic Value Separator:** Indicate the character that will be used to separate multiple values within a single message. This may be optional, depending on your team's selected network layout. For example, if only one value is published per topic, you may omit the separator. If teams use one topic to send multiple pieces of information, however, it is required.
        1. **Value 1:** For value1 sent within the topic, please include
            1. **Value Name:** Short and unique identifier for each unique value.
            1. **Value Description:** Please provide a brief description of the value you are publishing
            1. **Unit System:** Please describe the unit system that the value is measured in. Say "raw" if the number is a raw, unscaled value directly from the sensor.
            1. **Value Minimum:** Please provide the lower limit that your value can ever reach as defined by hardware setup or data type. For example, if you have a 12-bit ADC, the lowest value for an unsigned long int is zero.
            1. **Value Maximum:** Please provide the upper limit that your value can ever reach as defined by hardware setup or data type. For example, if you have a 12-bit ADC, the highest value it can reach is $(2^{12})-1 = 4095$.
            1. **Value Type:** Please use the variable type you use to store value1 in C.
            1. **Value Format String:** Please provide the C format string you will be using to convert the stored value to a string. See [this reference for more information](http://www.cplusplus.com/reference/cstdio/printf/)
            1. **Value Unique Identifier:** Please provide a ***unique*** single character that indicates the value immediately follows. You may only use that character for one type of data for all messages transmitted across your topic. This is required if the values in each message are sent in different orders, or if not all values are sent each time.
        1. **Value X (optional):** please provide the same items above (i-viii) for each subsequent value sent within the same topic.
        1. **Full Topic Example:** Please provide an example of how your values would look when sent in a single publish step.
1. **Test:** Practice sending and receiving messages to the MQTT to each other. You do not have to use live sensor data, but should send each other messages published over MQTT to confirm that you can publish and subscribe to all assigned topics in the correct format.
1. **Maintain your team's table.** As you continue to program, this table entry is your team's responsibility to maintain. This will be verified during hardware and software verification and/or your team's final demonstration.


Submit the following documents to Canvas by the deadline posted in Canvas.

1. Topic table(pdf)  

