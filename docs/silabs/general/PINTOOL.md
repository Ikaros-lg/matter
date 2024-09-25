# Using Simplicity Studio's Pintool and Project Configuration with Matter

At some point during product development you may need to move your project over to your custom hardware. In this case,
you will likely need to change the pinout and hardware configuration in the example project to reflect your own custom project. You can do this
with Simplicity Studio's Pintool starting from a blank C++ project.

## 1. Locate the board support files in the Matter repo

The pin and peripheral configuration for your example application is stored
within the Silicon Labs Matter support directory. For all the examples used in
the matter repository, the peripheral and pin configurations are stored at

When creating a configuration for a custom board do the following:

1. Create a Custom C++ project within Simplicity Studio.
2. Include your desired peripherals in the project.
3. Copy the generated output config files into a custom board support directory
   within the Matter repository.
