# Weather API Client

This C++ project fetches current weather data from the National Weather Service API based on provided latitude and longitude coordinates. It updates the weather information every 5 seconds.

## Features

- Fetches current weather data including temperature, conditions, and wind speed
- Retrieves daily forecast with minimum and maximum temperatures
- Updates weather information automatically every 5 seconds
- Thread-safe implementation

## Prerequisites

- C++11 or later
- libcurl
- pugixml

## Installation

### Linux (Ubuntu/Debian)

1. Install dependencies:

```

   sudo apt-get update
   sudo apt-get install build-essential libcurl4-openssl-dev

```

2. Install pugixml:

```

   sudo apt-get install libpugixml-dev

```

### macOS

1. Install Homebrew if not already installed:

```

   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```

2. Install dependencies:

```

   brew install curl pugixml

```

### Windows

1. Install MSYS2 from https://www.msys2.org/

2. Open MSYS2 MinGW 64-bit terminal and run:

```

   pacman -Syu
   pacman -S mingw-w64-x86_64-gcc mingw-w64-x86_64-curl mingw-w64-x86_64-pugixml

```

## Building the Project

1. Clone the repository:

```

   git clone https://github.com/yourusername/weather-api-client.git
   cd weather-api-client

```

2. Compile the project:

```

   g++ -std=c++11 main.cpp Weather.cpp -o weather_client -lcurl -lpugixml -pthread

```

## Usage

1. Edit the `nws_url_` in `Weather.h` to set your desired latitude and longitude.

2. Run the compiled executable:

```

   ./weather_client

```

The program will start fetching and displaying weather data, updating every 5 seconds for 30 seconds.

## Customization

- To change the update interval, modify the `update_interval_seconds_` variable in `Weather.h`.
- To adjust the runtime, change the `sleep(30)` value in `main.cpp`.

## License

This project is open-source and available under the MIT License.

## Contributing

Contributions, issues, and feature requests are welcome. Feel free to check issues page if you want to contribute.

## Author

[Prayush Adhikari]
