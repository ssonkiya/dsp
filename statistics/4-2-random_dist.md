[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> 

    sample = np.random.random(1000)

    pmf = thinkstats2.Pmf(sample, label = 'PMF')
    width = 0.2
    thinkplot.Pmf(pmf, linewidth=0.2)
    thinkplot.Config(xlabel='random', ylabel='PMF')

    cdf = thinkstats2.Cdf(sample, label='CDF')
    thinkplot.Cdf(cdf)
    thinkplot.Show(xlabel='percentage rank', ylabel='CDF')

The distribution is uniform
