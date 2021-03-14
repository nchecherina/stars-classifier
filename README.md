# stars-classifier
%matplotlib inline
import pandas as pd

plt.style.use('seaborn')

x = [1.1, 0.907, 0.144, 0.125, 0.09, 0.46, 2.063, 0.06, 0.102, 0.1, 0.17, 0.136, 0.82, 0.486, 0.168, 0.7, 0.63, 1.499, 0.602, 0.334]
y = [1.519, 0.5002, 0.0004, 0.00005, 0.00002, 0.0055, 25, 0.056, 0.00006, 0.00004, 0.0038, 0.0018, 0.34, 0.0367, 0.00362, 0.153, 0.085, 6.93, 0.00049, 0.039]

plt.title('Luminousity in comparison to mass of stars closest to the Sun')
plt.xlabel('Mass (in terms of Sun)')
plt.ylabel('Luminousity (in terms of Sun)')

colors = [1.29, 0.78, 0.1, 0.27, 0.1, 0.44, 1.63, 0.1, 0.1, 0.1, 0.27, 0.1, 0.78, 0.44, 0.27, 0.61, 0.61, 1.63, 0.1, 0.27]
sizes= [500, 450, 100, 227, 100, 315, 600, 100, 100, 100, 227, 100, 400, 450, 315, 227, 350, 600, 100, 227]
plt.scatter(x, y, s=sizes, c=colors, cmap='Greens', edgecolor='black', linewidth=1, alpha=0.75)

cbar = plt.colorbar()
cbar.set_ticks([0.1, 0.27, 0.44, 0.61, 0.78, 0.95, 1.12, 1.29, 1.46, 1.63])
cbar.set_ticklabels([0.1, 0.27, 0.44, 0.61, 0.78, 0.95, 1.12, 1.29, 1.46, 1.63])
cbar.set_label('Radius (x Sun)')

plt.show()
