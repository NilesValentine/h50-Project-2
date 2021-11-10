ReadMe2.md

# Change Log

# 11/02/2021
    created simple sms app
    created sms library
        Conventions Used:
            IN arguments = argIn_...
            string variables = str_...
        existing variables should not be changed
            will break the app
        published locally
            in h50-p2/library
        need to install API package
            uipath.twilio

# 11/3/2021
    packages and API's in use:
        googlemaps.activities
        openweathermap.activities
        sendsms
            -library by aaron
        uipath.excel.activities
        uipath.mail.activities
        uipath.system.activities
        uipath.twilio.activites
        uipath.uiautomation.activities
        uipath.webapi.activities
        weatherreport.activities
        yahooweather

# 11/4/2021
    created new process 'Weather'
        packages in use:
            OpenWeatherMap.Activities
            UiPath.WebAPI.Activities
    found that weather output is incompatible with JSON dictionary object
    can pull current, min, and max temps from current weather report
        used 'substring' to pull out temperature data from weather output
        converted reported temps from kelvin to fahrenheit
    can pull current conditions from current weather report
        used split and replace to pull conditions from weather report

# 11/5/2021
    rebuilt GetWeatherConditions as library
        input: zip code
        output: current conditions
    rebuilt GetCurrentTemp as library
        input: zip code
        output: current temp, high temp, low temp
    moved SendSMS to proper library folder for push

# 11/5/2021
    combined get temp and get conditions adding get wind
        full features in one library
        takes input of zip code
        gives output of:
            current temp
            day's low temp
            day's high temp
            current weather conditions
            current wind conditions
                speed and direction in degrees
        uses API package OpenWeatherMap.Activities
    can screen scrape weather.com 10 day forcast using supplied zip code
    




    