def calculate_duration(age, unit):
    units_in_a_year = {
        "months": 12,
        "weeks": 52,
        "days": 365,
        "hours": 365 * 24,
        "minutes": 365 * 24 * 60,
        "seconds": 365 * 24 * 60 * 60
    }
    
    unit = unit.lower()
    if unit.startswith('m'):
        unit = 'months'
    elif unit.startswith('w'):
        unit = 'weeks'
    elif unit.startswith('d'):
        unit = 'days'
    elif unit.startswith('h'):
        unit = 'hours'
    elif unit.startswith('min'):
        unit = 'minutes'
    elif unit.startswith('s'):
        unit = 'seconds'
    
    if unit not in units_in_a_year:
        return "Invalid time unit."
    
    duration = age * units_in_a_year[unit]
    return f"You lived for {duration} {unit.capitalize()}."

def main():
    age = int(input("What's your age? "))
    unit = input("Please choose time unit: Months, Weeks, Days, Hours, Minutes, Seconds. \nNote: You can write the first letter or the full name of the time unit. ")
    
    result = calculate_duration(age, unit)
    print(result)

if __name__ == "__main__":
    main()

]
