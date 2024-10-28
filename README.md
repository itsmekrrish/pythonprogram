# pythonprogram to devolp 

from datetime import datetime
import pytz

# Define a list of time zones to display
time_zones = [
    "UTC",
    "America/New_York",     # New York, USA
    "Europe/London",        # London, UK
    "Asia/Tokyo",           # Tokyo, Japan
    "Australia/Sydney",     # Sydney, Australia
    "Europe/Berlin",        # Berlin, Germany
    "Asia/Kolkata",         # Kolkata, India
]

print("World Clock".center(40, "-"))
for zone in time_zones:
    # Set the time zone
    timezone = pytz.timezone(zone)
    # Get the current time in that time zone
    current_time = datetime.now(timezone)
    # Display the time in the specified format
    print(f"{zone}: {current_time.strftime('%Y-%m-%d %H:%M:%S')}")
