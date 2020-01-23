---
layout: post
title:      "Growing and Learning Experiences"
date:       2020-01-23 20:42:34 +0000
permalink:  growing_and_learning_experiences
---


This Sinatra Project was a lot of fun for me. Parts of it were easy while others were challenging.  Here's hoping my post will remind or help some of you to not to make the same mistakes I’ve made. My biggest mistakes involved coding while exhausted and forgetting about conventions relating to the plurality of class names when It comes to certain relationships. 

My biggest and worst coding errors where caused my grammatical errors. Making a class name plural instead of singular to help prevent where applicable. I often made them all plural when models for example needed to be singular to prevent issues. I even started leaving off the end tags “>” when writing ruby in some of my ERB files. Other times I would put in one too many quotation marks or other characters which caused all manner of “undefined methods name errors”.

Although some of my issues were caused from a lack of understanding a good 6/10 were caused from exhaustion. Spelling errors, copies of code, redundant code, you can make a plethora of mistakes while tired. So please make sure you’re getting adequate rest. If not at least take a quick 10-minute nap if you can. It can only help.

A word of advice before I go. If you find yourself writing redundant code refactor it and put in a helper method to speed things up some. For example, in my project I added various validations it got to be too much. 

```
  def require_login
    unless logged_in?
      redirect '/login'
    end
  end
```

My helper method which was called “require_login” checked to see if a user was logged into the site before they could check out the other sections. If someone wasn’t logged in it would always redirect them to the sign-up page. Using helper methods can and will save you tons of time if you can find a way to utilize them.


