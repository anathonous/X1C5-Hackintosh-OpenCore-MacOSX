#!/bin/bash

echo "Restarting bluetooth service..."
blueutil -p 0 && sleep 1 && blueutil -p 1

echo "Waiting bluetooth service to be restored..."
until blueutil -p | grep "1" >/dev/null; do sleep 1; done

echo "Searching for devices not connected..."
devices=($(blueutil --paired | grep "not connected" | awk -F '[ ,]' '{print $2}'))
echo "Found ${#devices[@]} recently paired devices not connected"

for device in ${devices[@]}; do
    for retry in {1..5}; do	
    	echo "Trying to connect to ${device} ..."
        if blueutil --connect ${device}; then break; fi
        echo "Failed to connect to ${device}"
        sleep 1
    done
done
