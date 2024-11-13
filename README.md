class Thesequenceofpowersofthenumber2:
    def __init__(self, max_power):
        self.max_power = max_power
        self.current_power = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.current_power > self.max_power:
            raise StopIteration
        result = 2 ** self.current_power
        self.current_power +=1
        return result

power_iterator = Thesequenceofpowersofthenumber2(20)
for power in power_iterator:
    print(power)
