---
layout: post
title:      "Has_Secure_Password"
date:       2020-04-01 16:17:08 +0000
permalink:  has_secure_password
---


This method does several things for us. It gives us validations for our passwords such that they must be present on creation of of accounts and that the password length must be less than or equal to 72 bytes or characters. It also gives us access to password confirmation using a “xxx_confirmation” attribute. In my experience so far I’ve only seen it set as password_confirmation. This allows us to verify that the password we entered is what we what by ensuring that they match.


To put things simply has_secure_password gives us methods to set and authenticate against a 
BCrypt password.

