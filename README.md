# -Research-Assistant---Crypto
Solution to Application questions for role advertised.

1. FINANCE

a. The stock-to-flow model is a market model that measures value of a commodity relative to it's current and new supply. The BTC SF model states that value of bitcoin is and will be defined by it's scarcity and regulated/fixed supply. Unlike consumer goods and normal commodities that are easily reproduced after consumption and are as such not a good store of value BTC will according to the model be highly valuable as a store of value because it is a scarce resource. It compares it's model to similar models of scarce commodities such as Gold and Silver relative to the USD. SF is calculated by dividing the current stock of the commodity by new annual supply/production. The current SF for Gold, Silver and Bitcoin are 62, 22 and 25 and market cap of $8.5T, $300B and $118B USD respectively. However it further suggests that unlike Gold and Silver which have an almost fixed supply, the SF and market value of bitcoin will continue to double after every "halving".

Halving is an event in the Crypto's lifecycle whereby the reward for mining is halved. Mining is a process in which miners verify transactions in the block chain by solving complex cryptographical hashes and patterns. The current reward for mining after the May 2020 halving is 6.25 new bitcoins from a previous 12.5. The halving cycle is after every 210,000 blocks and with every verification happening roughly every 10 minutes it's estimated to happen every 4 years. It is derived from the BTC SF model that the market value of BTC will double after every halving and the reward for mining will tend to 0, quantity of bitcoin tends to its maximum supply value which is 21 million, causing the price of BTC to tend skyrocket and make it the most expensive asset and medium of exhange above Gold and Silver. Past halvings have followed the trend and it is estimated that in the second half of 2021, after the 2020 halving, the price of a bitcoin will rise to approximately $55,000 pounds and the total market value, at $1 trillion USD.

The BTC SF model, plots a graph of data with the stock-to-flow in log values on the X-axis and Total market value of the Y-axis, to prove accuracy of this model, a linear regression is then run on the data. An R2 value of 95% is derived. R2(R-squared) is a measure of goodness of fit. In other words it measures the variance of the explained variable relative to the variable explaining it. A p-Value of slope 2.3E-17 to prove that the likelihood that the relationship between the BTC stock-to-flow and its market cap is caused by chance is almost 0. It was then derived that the relationship between the Total market cap and the SF value is significant, and as such confirms the accuracy of the SF model that predicts BTC overtaking Gold and Silver as the most valuable monetary good in existence with an SF higher than gold and market cap of about $1 trillion USD. 

However this model is flawed in certain aspects and in as much as the forecast looks promising, the BTC SF model has it's shortcomings.

Firstly, judging by the regression analysis performed on the model, as more halvings occur and new supply of BTC tends to 0 the total market value of the cryptocurrency tends to infinity which is very unlikely, and points to the strong possibilty of the regression being a spurious one. 

Secondly, With BTC having an SF value of 25, and Silver having an SF of 22, BTC is supposed to be worth more in total market value than Silver currently as it has a higher SF value but reverse is the case as Silver ($300B) is worth more than BTC ($118B). 

Lastly, the model is based on the assumption the SF is strictly responsible for the value of gold, however research has shown that value of Gold is sometimes unrelated to the SF value. The model also fails to take into account the impact of occurences of devaluation of the US dollar and it's contribution to the value of gold.



b. 
Stock price (P<sub>o</sub>) = $40, Strike price (X) = $45, Time (t) 4 months, (0.3 year), Volatility (σ)= 0.4, Risk free (Krf) = 0.03. N (normal distribution for d<sub>1</sub> and d<sub>2</sub>, V<sub>c</sub> (call price)

V<sub>c</sub> = P<sub>o</sub> Nd<sub>1</sub> - ( X / e<sup>Krf * t</sup> )Nd<sub>2</sub>

d<sub>1</sub> = [ln(P<sub>o</sub>/X)] + (Krf + 0.5(σ)<sup>2</sup>)(t) / σ√t 

d<sub>2</sub> = d<sub>1</sub> - σ√t 

d<sub>1</sub> = ln(40/45) + [0.03 + 0.5(0.4)<sup>2</sup>] (0.3) / (0.4)(0.577)

d<sub>1</sub> = -0.118 + [0.03 + 0.08] (0.3) / (0.4)(0.577)

d<sub>1</sub> = -0.118 + [0.11] (0.3) / (0.2308)

d<sub>1</sub> = -0.118 + 0.03663 / (0.2308) = -0.08137 / 0.2308 

d<sub>1</sub> = -0.35

d<sub>2</sub> = -0.353 - 0.2308 

d<sub>2</sub> = -0.58

N<sub>d1</sub> = 0.36317, N<sub>d2</sub> = 0.28096

V<sub>c</sub> = (40)(0.36317) - [(45)/e<sup>(0.03 * 0.33)</sup>] (0.28096) 

V<sub>c</sub> = 14.527 - (45/1.01)(0.281)

V<sub>c</sub> = 14.527 - (44.56)(0.281)

V<sub>c</sub> = 14.527 - 12.5214 

V<sub>c</sub> = $2. 



2. COMPUTER SCIENCE

a. A recursion operates by keeping a copy of it's previous calls in memory to enable it access them in future calls. This is called a recursive tree. For smaller values of n in the recursion it runs optimally. However as n becomes larger, the recursion tree becomes larger thereby causing high usage of system memory which in turn slows down the process. 

b. (Javascript)

<code>
  const isProthNumber = function(num) {


    const isPowerOfTwo = function(num) {
            return Math.log2(num) % 1 === 0;
        }


        // subtract 1 from num
        --num

    //initialise k
    let k = 1



    while (k < (num / k)) {


        if (num % k === 0) {

            if (isPowerOfTwo(num / k))
                //if k × 2<sup>n</sup> + 1
                return true;
        }

        k = k + 2;

    }

    return false;

    }

    console.log(isProthNumber(3))
</code>


3. MATHS 

 y = sqrt((x+6)<sup>2</sup> + 25) + sqrt((x-6)<sup>2</sup> + 121)
 
 y = sqrt((x+6)(x+6) + 25) + sqrt((x-6)(x-6) + 121)
 
 y = sqrt(x<sup>2</sup> + 6x + 6x + 36 + 25) + sqrt(x<sup>2</sup> - 6x - 6x + 36 + 121)
 
 y = sqrt(x<sup>2</sup> + 12x + 61) + sqrt(x<sup>2</sup> - 12x + 157)
 
 y = (x<sup>2</sup> + 12x + 61)<sup>1/2</sup> + (x<sup>2</sup> - 12x + 157)<sup>1/2</sup>
 
 Differentiate using composite rule
 
 y = 1/2(x<sup>2</sup> + 12x + 61)<sup>-1/2</sup> (2x + 12) + (x<sup>2</sup> - 12x + 157)<sup>-1/2</sup> (2x - 12)
 
 y = (2x + 12) / 2 (sqrt(x<sup>2</sup> + 12x + 61)) + (2x - 12) / 2 (sqrt(x<sup>2</sup> - 12x + 157)) 
 
 0 = (x + 6) / (sqrt(x<sup>2</sup> + 12x + 61)) + (x - 6) / (sqrt(x<sup>2</sup> - 12x + 157))
 
 (x + 6) / (sqrt(x<sup>2</sup> + 12x + 61)) = (6-x) / (sqrt(x<sup>2</sup> - 12x + 157))
 
 Square both sides
 
 (x + 6)<sup>2</sup> / (x<sup>2</sup> + 12x + 61) = (6-x)<sup>2</sup> / (x<sup>2</sup> - 12x + 157)
 
 Cross multiply
 
 (x + 6)<sup>2</sup> (x<sup>2</sup> - 12x + 157) = (6-x)<sup>2</sup> (x<sup>2</sup> + 12x + 61)
 
 (x+6)(x+6) (x<sup>2</sup> - 12x + 157) = (x-6)(x-6) (x<sup>2</sup> + 12x + 61)
 
 (x<sup>2</sup> + 6x + 6x + 36) (x<sup>2</sup> - 12x + 157) = (x<sup>2</sup> - 6x - 6x + 36) (x<sup>2</sup> + 12x + 61)

 (x<sup>2</sup> + 12x + 36) (x<sup>2</sup> - 12x + 157) = (x<sup>2</sup> - 12x + 36) (x<sup>2</sup> + 12x + 61)

 x<sup>4</sup> - 12<sup>3</sup> + 157x<sup>2</sup> + 12x<sup>3</sup> - 144x<sup>2</sup> + 1884x + 36x<sup>2</sup> - 432x + 5652 = x<sup>4</sup> + 12x<sup>3</sup> + 61x<sup>2</sup> - 12x<sup>3</sup> - 144x<sup>2</sup> - 732x + 36<sup>2</sup> + 432x + 2196

 x<sup>4</sup> + 49<sup>2</sup> + 1452x + 5652 = x<sup>4</sup> - 47<sup>2</sup> -300x + 2196

 x<sup>4</sup> - <sup>4</sup> + 49<sup>2</sup> + 47x<sup>2</sup> + 1452x + 300x + 5652 - 2196 = 0 

 96<sup>2</sup> + 1752x + 3456 = 0 

 solved this equation as a quadratic on a scientific calculator

 x = -2.25 and x = -16
 
 solving for first value of y

 y = sqrt((x+6)<sup>2</sup> + 25) + sqrt((x-6)<sup>2</sup> + 121)
 
 y = sqrt((-2.25+6)<sup>2</sup> + 25) + sqrt((-2.25-6)<sup>2</sup> + 121)
 
 y = sqrt((3.75)<sup>2</sup> + 25) + sqrt((-8.25)<sup>2</sup> + 121)
 
 y = sqrt(14.0625 + 25) + sqrt(68.0625 + 121)
 
 y = sqrt(39.0625) + sqrt(189.0625)
 
 y = 6.25 + 13.75 
 
 y = 20
 
 solving for second value of y
 
 y = sqrt((-16+6)<sup>2</sup> + 25) + sqrt((-16-6)<sup>2</sup> + 121)
 
 y = sqrt((10)<sup>2</sup> + 25) + sqrt((-22)<sup>2</sup> + 121)
 
 y = sqrt(100 + 25) + sqrt(484 + 121)
 
 y = sqrt(125) + sqrt(605)
 
 y = 11.18 + 24.6
 
 y = 35.78
 
 Both values of y are real numbers
 
 The minimum value of y is 20, when x = -2.25 

