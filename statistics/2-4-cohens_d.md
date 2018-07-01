[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>>
    import math

    preg = nsfg.ReadFemPreg()
    live = preg[preg.outcome == 1]

    firsts = live[live.birthord == 1]
    others = live[live.birthord != 1]

    def CohenEffectSize(group1, group2):
        diff = group1.mean() - group2.mean()

        var1 = group1.var()
        var2 = group2.var()
        n1, n2 = len(group1), len(group2)

        pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
        d = diff / math.sqrt(pooled_var)
        return d


    print ('Cohen',CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb))
    print('first', firsts.totalwgt_lb.mean())
    print('other', others.totalwgt_lb.mean())


Mean for the first born weights: 7.201094430437772 \n
Mean for the others: 7.325855614973262
Conden's d: -0.0886729

Generally, first borns are slightly lighter than others.
Conden's d is smaller than the difference in pregnancy length, meaning the difference in means is even smaller.
