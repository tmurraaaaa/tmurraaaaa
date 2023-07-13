- 👋 Hi, I’m @tmurraaaaa
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
tmurraaaaa/tmurraaaaa is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
class LicensePlate:
    def __init__(self, plate_number, owner_name):
        self.plate_number = plate_number
        self.owner_name = owner_name


class LicensePlateRegistry:
    def __init__(self):
        self.plates = []

    def register_plate(self, plate_number, owner_name):
        plate = LicensePlate(plate_number, owner_name)
        self.plates.append(plate)
        print("License plate registered successfully!")

    def find_plate_owner(self, plate_number):
        for plate in self.plates:
            if plate.plate_number == plate_number:
                return plate.owner_name
        return "Plate number not found in the registry."


# Example usage
registry = LicensePlateRegistry()

# Registering a license plate
registry.register_plate("ABC123", "John Doe")
registry.register_plate("XYZ789", "Jane Smith")

# Finding the owner of a license plate
plate_number = input("Enter the license plate number: ")
owner_name = registry.find_plate_owner(plate_number)
print("Owner:", owner_name)
