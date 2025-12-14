# **MATH MODULE**
import math

math.ceil(1.03)

math.ceil(-1.03)

math.sqrt(81.0)

math.exp(2.0)

math.fabs(2.0)

math.fabs(-2.0)

math.floor(3.04)

math.floor(-3.04)

math.log(1.0)

math.log(1024, 2)

math.log10(1.0)

math.pow(3.0, 2.0)

value = 1.0

math.sin(value)

math.cos(value)

math.tan(value)

math.degrees(3.14)

math.radians(179.91)

math.pi

math.e

# Extra math functions
math.factorial(5)

math.gcd(24, 36)

math.lcm(8, 14)

math.copysign(3.5, -1)

math.isfinite(math.inf)

math.isinf(math.inf)

math.isnan(float("nan"))

math.hypot(3, 4)

math.comb(5, 2)

math.perm(5, 2)

math.trunc(3.99)

math.modf(3.1415)

math.acos(1)

math.asin(1)

math.atan(1)

math.atan2(1, 1)

import random

random.seed(10)          # reproducible results

random.random()

random.uniform(1, 10)

random.randint(1, 100)

random.randrange(45)

random.randrange(11, 45)

random.randrange(23, 45, 4)

random.choice([1, 2, 3])

random.choices([1, 2, 3], k=5)

random.sample([1, 2, 3, 4, 5], 3)

my_list = [1, 2, 3, 4, 5]

random.shuffle(my_list)

random.betavariate(1, 3)

random.expovariate(1)

random.gauss(0, 1)

random.triangular(0, 10)

# import statistics

seq = [5, 6, 2, 5, 3, 4, 2, 5, 6, 6, 9, 2]

statistics.mean(seq)

statistics.median(seq)

statistics.mode(seq)

# Extra statistics
statistics.pstdev(seq)

statistics.pvariance(seq)

statistics.stdev(seq)

statistics.variance(seq)

statistics.median_low(seq)

statistics.median_high(seq)

statistics.median_grouped(seq)

statistics.fmean(seq)

statistics.harmonic_mean(seq)

statistics.geometric_mean(seq)

data = [1, 1, 2, 3, 3, 3, 4]
statistics.multimode(data)
