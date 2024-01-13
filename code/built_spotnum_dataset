#制作情感分析的箱线图
#输入判定为积极情感或消极情感的概率

import pandas as pd
import numpy as np

from pyecharts import options as opts
from pyecharts.charts import Boxplot
from pyecharts.faker import Faker

timedict = pd.DataFrame(columns=['time','max','min'])  # 创建一个空的DataFrame对象，并将其列定义为两列数
def add_data(file_name):
    data = pd.read_csv(file_name,index_col=0,usecols=["热度"])
    data = np.array(data.index)
    timedict.loc[len(timedict.index)] = 	[file_name[-23:-4],data.max(),data.min()] # 将最大最小值
    print(file_name[-23:-4],"stored successfully")
    return timedict

import os

path = 'E:\python当学会\\课程作业\\homework_04_finale\\1900016931_冯嘉隆_大作业\\data_storage\\raw_data'
file_list = []
for file_name in os.listdir(path):
    file_list.append("data_storage\\raw_data\\"+str(file_name))
  # 将文件名列表加进列表中。

for file_path in file_list:
    add_data(file_path)


print(timedict.head)

timedict.to_csv('data_storage\\cleansed_data\\timed_data.csv') # 将数据存储到文件中。记得将文件名称加





