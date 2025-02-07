# Smartphone-Class


class Smartphone:
   
    def __init__(self, brand, model, price, storage, battery_life):
        
        self.brand = brand
        self.model = model
        self.price = price
        self.storage = storage
        self.battery_life = battery_life

   
    def make_call(self, number):
        
        return f"Calling {number}..."

    def send_message(self, number, message):
        return f"Sending message to {number}: {message}"

    def get_info(self):
        return f"Brand: {self.brand}, Model: {self.model}, Price: {self.price}, Storage: {self.storage}GB, Battery life: {self.battery_life} hours"



class SmartphoneWithCamera(Smartphone):
   
    def __init__(self, brand, model, price, storage, battery_life, camera_megapixels):
        super().__init__(brand, model, price, storage, battery_life)
        self.camera_megapixels = camera_megapixels

    def take_photo(self):
        return f"Taking a photo with {self.camera_megapixels}MP camera..."

    def record_video(self, duration):
        return f"Recording video for {duration} minutes with {self.camera_megapixels}MP camera..."

    def get_info(self):
        base_info = super().get_info()
        return f"{base_info}, Camera: {self.camera_megapixels}MP"



# Create a basic smartphone instance

basic_phone = Smartphone("GenericBrand", "ModelX", 299, 64, 24)

print(basic_phone.get_info())

print(basic_phone.make_call("123-456-7890"))

print(basic_phone.send_message("123-456-7890", "Hello!"))


# Create a smartphone with camera instance


camera_phone = SmartphoneWithCamera("CamBrand", "ModelY", 499, 128, 30, 48)

print(camera_phone.get_info())

print(camera_phone.take_photo())

print(camera_phone.record_video(10))

