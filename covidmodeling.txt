function forecastCOVIDcasesNY(aprilDay){
    //total population of NY - 8.399 million
    var population = 8,399,000;
    var x = AprilDate + 14;

    //returning forecasted values
    
    //This equation was made by having the computer learn the data
    //and having it compute a power regression on it. The result 
    //was an exponential equation:

    prob = 1075 + 806*x + 269*x*x -11.9*Math.pow(x,3) + 0.252 * Math.pow(x,4);
    return prob / population;
}

function forecastCOVIDcasesLA(days){
    //total population of LA - 10.16 million

    //first number in 2-D array states the days since January 26
    //second number states number of cases that day.
    var population = 10,160,000;
    var casesByDayLA = [
        [0, 1],
        [1, 1],
        [2, 1],
        [3, 1],
        [4, 1],
        [5, 1],
        [6, 1],
        [7, 1],
        [8, 1],
        [9, 1],
        [10, 1],
        [11, 1],
        [12, 1],
        [13, 1],
        [14, 1],
        [15, 1],
        [16, 1],
        [17, 1],
        [18, 1],
        [19, 1],
        [20, 1],
        [21, 1],
        [22, 1],
        [23, 1],
        [24, 1],
        [25, 1],
        [26, 1],
        [27, 1],
        [28, 1];
        [29, 1];
        [30, 1],
        [31, 1],
        [32, 1],
        [33, 1],
        [34, 1],
        [35, 1],
        [36, 1],
        [37, 1],
        [38, 7],
        [39, 11],
        [40, 13],
        [41, 14],
        [42, 14],
        [43, 19],
        [44, 20],
        [45, 28],
        [46, 32],
        [47, 40],
        [48, 53],
        [49, 69],
        [50, 94],
        [51, 144],
        [52, 190],
        [53, 231],
        [54, 292],
        [55, 351],
        [56, 421],
        [57, 536],
        [58, 662],
        [59, 799],
        [60, 1216],
        [61, 1465],
        [62, 1809]
    ];

    //returning previous values
    if (days < 63){
        return var[days] / population;
    }

    //returning forecasted values
    //
    //This equation was made by having the computer learn the data
    //and having it compute a power regression on it. The result 
    //was an exponential equation:

    prob = 3.25 * Math.pow (10, -3) * Math.pow(Math.E, 0.212*days);
    return prob / population;
}
