# btc2022
#include <stdio.h>

int main() {
    double prices[365]; // 比特币 2022 年的每日价格
    double sum = 0;
    double mean;
    double variance = 0;
    double standard_deviation;

    // 使用循环读入比特币 2022 年的每日价格
    for (int i = 0; i < 365; i++) {
        scanf("%lf", &prices[i]);
        sum += prices[i];
    }

    // 计算平均价格
    mean = sum / 365;

    // 计算方差
    for (int i = 0; i < 365; i++) {
        variance += (prices[i] - mean) * (prices[i] - mean);
    }
    variance = variance / 365;

    // 计算标准差
    standard_deviation = sqrt(variance);

    printf("The standard deviation of Bitcoin prices in 2022 is: %lf\n", standard_deviation);
    return 0;
}
