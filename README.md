# Student_grades_Analysis
grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]

def print_grades(grades):
    for grade in grades:
        print grade

def grades_sum(grades):
    total = 0
    for grade in grades: 
        total += grade
    return total
    
def grades_average(grades):
    sum_of_grades = grades_sum(grades)
    average = sum_of_grades / float(len(grades))
    return average

def grades_variance(scores):
    average= grades_average(scores)
    variance = 0
    for score in scores:
        variance = variance+(average-score)**2
    return variance/len(scores)
grades_variance(grades)
def grades_std_deviation(variance):
    return variance**0.5
variance=grades_variance(grades)
print grades_std_deviation(variance)

print "all of the grades", print_grades(grades)
print "sum of grades", grades_sum(grades)
print "average grade", grades_average(grades)
print "variance", grades_variance(grades)
print "Standard deviation", grades_std_deviation(variance)
