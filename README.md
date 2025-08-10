# water-leakage-detection-dataset
Water supply network leakage detection dataset (including three types of data: normal, small leakage category and large leakage category)
json format
{
  "SampleData": datalist,
  "DeviceID": "*",
   "SampleTime": "*"
}
you can use this function to read the data：

****************************************************************
import json
def getData(path):
    '''
    :param path:type->str: json file path
    :return:->type:list :[SampleData,DeviceID,SampleTime]
    '''
    with open(path, 'r') as f:
        d = json.load(f)
        DeviceID = d['DeviceID']
        SampleTime = d['SampleTime']
        SampleData = d['SampleData']
        return [SampleData, DeviceID, SampleTime]
  ****************************************************************

