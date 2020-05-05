---
layout: post
title:      "Chasing the Rabbit"
date:       2020-05-04 12:41:25 -0400
permalink:  chasing_the_rabbit
---


After a long hiatus, I jumped back into building python projects this past month. Once I picked my dataset and started my EDA, the familiar feeling of chasing rabbit holes came back with paralyzing anxiety. Thoughts usually begin with wanting to explore a certain feature or two a certain way, but not knowing how to best present it. This eventually leads to googling everything with a million tabs open. Most of the tabs end up not being relevant in any way to my original question, but are worth cataloging and coming back to. This blog post contains snippets of my catalog that I felt were useful, interesting or subjectively worth noting.

### **OOPs**
I wanted to try and build more functions and explore classes this time on my project. We touched upon object oriented programming in our modules, but its importance eluded me until I started having preferences for certain visualizations and tuning models. 

### **F-Strings**
Somewhere, probably in a Stackoverflow response, I was exposed to F-Strings. Since I didn't understand it at the time, I opted not to use the formatting. I wanted to explore it more when I was listening to an episode of [Talk Python to Me](https://talkpython.fm/episodes/show/211/classic-cs-problems-in-python). Side note, highly recommend this podcast to my fellow students. The concept of 'modern python'  intrigued me when they were talking about it on the show, but this [article](https://realpython.com/python-f-strings/) gives better context for F-Strings in particular. Introduced in Python 3.5 ([PEP 498 documentation](https://www.python.org/dev/peps/pep-0498/)), F-String formatting syntax is an upgrade from %-formatting and str.format().

Our curriculum seems to lean toward the str.format syntax (seen [here](https://github.com/learn-co-students/dsc-3-32-11-xgboost-lab-online-ds-sp-000/tree/solution)):
```
grid_clf = GridSearchCV(clf, param_grid, scoring='accuracy', cv=None, n_jobs=1)
grid_clf.fit(scaled_df, labels)

best_parameters = grid_clf.best_params_

print("Grid Search found the following optimal parameters: ")
for param_name in sorted(best_parameters.keys()):
    print("%s: %r" % (param_name, best_parameters[param_name]))

training_preds = grid_clf.predict(X_train)
val_preds = grid_clf.predict(X_test)
training_accuracy = accuracy_score(y_train, training_preds)
val_accuracy = accuracy_score(y_test, val_preds)

print("")
print("Training Accuracy: {:.4}%".format(training_accuracy * 100))
print("Validation accuracy: {:.4}%".format(val_accuracy * 100))
```

In F-String syntax, we'd have:
```
print(f'Training Accuracy: {training_accuracy:.2%}')
print(f'Validation accuracy: {val_accuracy:.2%}')
```

Intuitely, it's easier to read and understand.

### **Closing Thoughts**
I've really enjoyed learning the coding side of data science. In a multidisciplinary profession of stats, programming, and machine learning, my interest continues to grow in the the programming language itself and the visualization applications.

![](https://i.redd.it/nc5ua4x8lfg31.png)
*[r/learnmachinelearning](https://www.reddit.com/r/learnmachinelearning/comments/cqb7b8/ml_meme_war_this_is_one_of_my_favourite_machine/)*


