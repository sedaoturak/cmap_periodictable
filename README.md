# Color Map Plotter on Periodic Table
This Python script (`ptable_trends.py`) can be used to plot a heat map over an image of the periodic table of elements for easy and automated visualization of trends.

Usage
-----
A minimal example is as follows (and can be access through [this notebook](https://github.com/sedaoturak/cmap_periodictable/blob/master/example.ipynb)):
```python
from ptable_trends import ptable_plotter
ptable_plotter("ionization_energies.csv")
```
![plot1](example_images/plot1.png)

The only required argument to `ptable_plotter()` is a single positional argument for the full filepath/name (with extension) of the data file containing your trend data. The data file must be in a comma-separated value (`.csv`) format with the first entry in each row being the atom symbol and the second entry being the value you wish to plot. An example `.csv` file is included in this repository for testing purposes under the name `ionization_energies.csv`. After the `ptable_trends.py` script is run, it will show the plot in your web browser. To save the image, simply click the save icon that appears in the web browser figure.

There are numerous optional arguments, which can be used to modify the appearance of the figure. The full argument list can be found under the [definition](https://github.com/arosen93/ptable_trends/blob/0dd4171ececfc5524dea858c562953952295612f/ptable_trends.py#L28-L95) of `ptable_plotter()` function in the `ptable_trends.py` script:

A couple of examples using various optional keyword arguments are as follows:
```python
from ptable_trends import ptable_plotter
ptable_plotter("ionization_energies.csv", log_scale=True)
```
![plot2](example_images/plot2.png)

```python
from ptable_trends import ptable_plotter
ptable_plotter("ionization_energies.csv", cmap="viridis", alpha=0.7, extended=False, periods_remove=[1])
```
![plot3](example_images/plot3.png)

Dependencies
-----

The script requires the following dependencies:
* [Bokeh](http://bokeh.pydata.org/en/latest/)
* [pandas](http://pandas.pydata.org/)
* [matplotlib](http://matplotlib.org/)
* [colorcet](https://colorcet.holoviz.org/)

These packages can be installed using [pip](https://pip.pypa.io/en/stable/) via `pip install -r requirements.txt` in the `ptable_trends` base directory.
