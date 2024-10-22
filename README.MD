# Netmode

`netmode` is a simple Bash script that allows you to switch your network interface between different modes such as managed, monitor, IBSS, mesh, and WDS. It automates enabling/disabling monitor mode and other network modes for quick network configuration.

This script uses the power of `iw` as one of its backend commands to manage wireless interfaces efficiently.

## Features
- **Switch between multiple modes**: 
  - Managed
  - Monitor
  - IBSS (Ad-Hoc)
  - Mesh
  - WDS (Wireless Distribution System)
- **Auto detect wireless network interface**: The script automatically detects the available wireless interface on your system.
- **Simple command**: One-liner to change the mode of your network interface.

## Usefulness

The `netmode` script is particularly useful for:

- **Network Administrators**: Quickly switch between different network interface modes to troubleshoot connectivity issues or optimize wireless performance without needing to remember complex commands.

- **Penetration Testers**: Customize your machine to effortlessly change your wireless interface mode during assessments, enabling you to quickly switch to monitor mode for capturing packets or to managed mode for normal operation, all in one streamlined command.

- **Network Engineers**: Simplify the process of configuring network interfaces for various setups, whether it’s for deploying ad-hoc networks, mesh networking, or maintaining WDS connections.

## Requirements

Before using the script, ensure you have the following tools and packages installed:

- **`iw`**: A command-line tool for managing wireless devices.
- **`gawk`**: A programming language used for pattern scanning and processing.
- **`iproute2`**: A collection of utilities for controlling networking in Linux.

You can install these tools using your system package manager.

## Installation

1. Clone the repository:
	```bash
	git clone https://github.com/imortio/netmode.git
	```

2. Move the script to `/usr/local/bin/` and make executable to ensure it available system-wide:
	```bash
	sudo mv netmode /usr/local/bin/
	sudo chmod +x /usr/local/bin/netmode
	```

## Usage

To switch your network interface mode, use the following syntax:
```bash
sudo netmode <mode>
```

## Example

Enable monitor mode on `wlan0`:
```bash
sudo netmode mon
```

Switch back to managed/normal mode:
```bash
sudo netmode man
```

## Help

For help or usage information:
```bash
netmode -h
```

## Error Handling

The script includes basic error handling to ensure:

- You are using a valid network interface.
- The selected mode is supported.

## Contributing

Since this script is purposed to help on a simple task which may be oftenly performed by someone who specifically deals with networks, so contributions are welcome! Here’s how you can help:

1. **Fork the Repository**: Click on the "Fork" button at the top right corner of the page to create your own copy of the repository.

2. **Make Changes**: Clone your forked repository to your local machine and make your changes:
	```bash
	git clone https://github.com/imortio/netmode.git
	cd netmode
	```

3. **Create a Pull Request**: Once you’ve made your changes, push them to your forked repository and create a pull request:

- Go to the "Pull Requests" tab in the original repository.
- Click on "New Pull Request".
- Choose your branch and submit the pull request.

4. Report Issues: If you find any bugs or have feature requests, feel free to open an issue in the [issue tracker](https://github.com/imortio/netmode/issues).

## License

This project is licensed under the [Unlicense](https://unlicense.org/). See the [LICENSE](LICENSE) file for more details.
