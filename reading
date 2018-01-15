import matplotlib.pyplot as plt
import csv

#empty values
a = []
x = []
y = []
z = []


#function that reads the locations file
def reading_data_locations():
    with open('MokumAirwaysCities.txt','r') as csvfile:
        plots = csv.reader(csvfile, delimiter=',')
        for row in plots:
            a.append(int(row[0]))
            x.append(int(row[1]))
            y.append(int(row[2]))
            z.append(str(row[3]))
        return (a, x, y, z)

#functions that reads the distances between the locations(not finished)      
def reading_data_distances():
    matrix = np.loadtxt('MokumAirwaysDistances.txt')
    print (matrix)

#functions that reads the number of passengers per locations(not finished)
def reading_data_transport():
    matrix = np.loadtxt('MokumAirwaysPassengers.txt')
    print (matrix)

#function that plots the data of the locations file      
def plot_data():
    reading_data_locations()
    plt.scatter(x,y, label='Map of destinations')
    plt.xlabel('x')
    plt.ylabel('y')
    for i, txt in enumerate(z):
        plt.annotate(txt, (x[i],y[i]))
    plt.show()

reading_data()

