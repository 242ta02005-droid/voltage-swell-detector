# voltage-swell-detector
# Voltage Swell Detector

NORMAL_VOLTAGE = 230
SWELL_LIMIT = 253   # 110% of 230 V

print("==============================")
print("      VOLTAGE SWELL DETECTOR")
print("==============================")

voltage = float(input("Enter measured voltage (V): "))

print("\nMeasured Voltage:", voltage, "V")
print("Normal Voltage:", NORMAL_VOLTAGE, "V")

if voltage > SWELL_LIMIT:
    swell_percentage = ((voltage - NORMAL_VOLTAGE) / NORMAL_VOLTAGE) * 100

    print("\n⚠️ VOLTAGE SWELL DETECTED")
    print("Voltage increase:", round(swell_percentage, 2), "%")
    print("🔴 Power quality is poor")

else:
    print("\n🟢 NO VOLTAGE SWELL")
    print("✅ Voltage is within the normal range")
