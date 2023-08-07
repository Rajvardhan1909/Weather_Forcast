import pyowm
from datetime import datetime
API_Key = pyowm.OWM('11a73aec8f5f023e8c992ba55c448444')
print("Please enter your city :") city =input()
print("\n********************************************************************\n")
print(' WEATHER FORECAST OF ' , city)
print("\n********************************************************************\n")
mng = API_Key.weather_manager() location =
mng.weather_at_place(city) weather =
location.weather
temp = weather.temperature(unit = 'celsius') status =
weather.detailed_status avg_temp_data =
int(temp['temp'])
humidity = weather.humidity
pressure = weather.pressure
win = weather.wind()
dew_point = int(temp['temp_min'])
sunrise = weather.sunrise_time('iso')
sunset = weather.sunset_time('iso')
print('\nTEMPERATURE DETAILS\n')
print("The temperature today in ", city ,"is", avg_temp_data ,'degree celsius')
if (avg_temp_data <= 0):
print('Freezing Weather!!')
elif (avg_temp_data <= 10):
print('Very Cold Temperature!!')
elif (avg_temp_data <= 20):
print('cold Temperature!!')
elif (avg_temp_data <= 30):
print('Normal temperature!!')
elif (avg_temp_data <= 40):
print('Hot in temperature!!')
elif (avg_temp_data <= 50):
print('Extremely hot in temperature!!')
print("The maximum temperature today in ", city ,"is",temp['temp_max'] , 'degree celsius')
print("The minimum temperature today in ", city ,"is",temp['temp_min'] , 'degree celsius')
print("The feels like temperature today in ", city ,"is",temp['feels_like'] , 'degree celsius')
print('\nOTHER DETAILS\n')
print("Current date and time in",city)
now = datetime.now()
dt_string = now.strftime("%d/%m/%Y %H:%M:%S")
print("date and time =", dt_string)
print('Sun Rise time is',sunrise)
print('Sun Set time is',sunset)
print('Today we will be having ' , status , 'in ' , city)
if 'rain' in status or 'thunderstorm' in status or 'drizzle' in status or 'snow' in status:
print("It's raining outside,so umbrella is required")
elif 'broken clouds' in status or 'clouds' in status:
print('Rain is expected')
elif 'clear' in status :
print('Its clear outside')
print('Percentage of Humidity =' ,humidity)
print('Pressure =' , pressure['press'],'mbar')
print('Sea Level =' ,pressure['sea_level'],'m')
print('Wind speed =',win['speed'])
print('Wind direction is ')
if (win['deg'] == 0 or win['deg'] == 360):
print('north wind (N)')
elif (win['deg'] == 22.5):
print('north-northeast wind (NNE)')
elif (win['deg'] == 45):
print('northeast wind (NE)')
elif (win['deg'] == 67.5):
print('east-northeast wind (ENE)')
elif (win['deg'] == 90):
print ('east wind (E)')
elif (win['deg'] == 112.5):
print('east-southeast wind (ESE)')
elif (win['deg'] == 135):
print('southeast wind (SE)')
elif (win['deg'] == 157.5):
print('south-southeast wind (SSE)')
elif (win['deg'] == 180):
print('south wind (S)')
elif (win['deg'] == 202.5):
print('south-southwest wind (SSW)')
elif (win['deg'] == 225):
print('southwest wind (SW)')
elif (win['deg'] == 247.5):
print('west-southwest wind (WSW)')
elif (win['deg'] == 270):
print('west wind (W)')
elif (win['deg'] == 292.5):
print('west-northwest wind (WNW)')
elif (win['deg'] == 315):
print('northwest wind (NW)')
elif (win['deg'] == 337.5):
print('north-northwest wind (NNW)')
print('Dew point = ',dew_point,'degree celsius')
