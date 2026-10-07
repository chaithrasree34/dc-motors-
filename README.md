# dc-motors-
# DC Motor Calculator Using Python

print("DC MOTOR CALCULATOR")
print("-------------------")

print("1. Back EMF")
print("2. Mechanical Power")
print("3. Torque")
print("4. Motor Efficiency")

choice = int(input("\nEnter your choice (1-4): "))

if choice == 1:
    V = float(input("Enter supply voltage (V): "))
    Ia = float(input("Enter armature current (A): "))
    Ra = float(input("Enter armature resistance (Ohm): "))

    Eb = V - (Ia * Ra)

    print("\nBack EMF =", round(Eb, 2), "V")

elif choice == 2:
    torque = float(input("Enter torque (N-m): "))
    speed = float(input("Enter speed (RPM): "))

    power = (2 * 3.14159 * speed * torque) / 60

    print("\nMechanical Power =", round(power, 2), "W")
    print("Mechanical Power =", round(power / 1000, 2), "kW")

elif choice == 3:
    power = float(input("Enter mechanical power (W): "))
    speed = float(input("Enter speed (RPM): "))

    torque = (power * 60) / (2 * 3.14159 * speed)

    print("\nTorque =", round(torque, 2), "N-m")

elif choice == 4:
    output_power = float(input("Enter output power (W): "))
    input_power = float(input("Enter input power (W): "))

    efficiency = (output_power / input_power) * 100

    print("\nMotor Efficiency =", round(efficiency, 2), "%")

else:
    print("\nInvalid choice!")