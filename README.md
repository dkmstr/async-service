Async Service
=============

This is a simple example on how to use a Windows Service to run an asyncio task in the background. The service is installed using the command line and it is uninstalled using the command line as well.

The project contains a Sample service to run the async task, and a .spec file to use with pyinstaller to create the executable.

The unused import "win32timezone" is needed by pywin32, it also can be included on "hiddens" list of pyinstaller, but i prefer to leave it on the code. :)

## Usage

Simply download the project and run the following commands:

```bash
pip install -r requirements.txt

pyinstaller async_service.spec

# Install the service

cd dist\async_service
async_service.exe install

# Start the service, you can also start it from the services.msc console
async_service.exe start

# Stop the service, you can also stop it from the services.msc console
async_service.exe stop

# Uninstall the service
async_service.exe remove

# Run as a "normal" program
async_service.exe run
```

Hope someone find this useful. :)

## License

MIT License

