#!/bin/bash

username=${1:-"test"}
password=${2:-"test"}

code=`curl -k -s -o /dev/null -w "%{http_code}" \
    -X POST \
    -H "Content-Type: application/x-www-form-urlencoded" \
    -d "erase-cookie=false&password=$password&popup=false&username=$username" \
    "https://login.aut.ac.ir/login"`

if [ $code == '302' ]; then
	echo "Login was successful."
else
	echo "Login was failed."
fi
