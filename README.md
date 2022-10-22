# RPL-IMPAL

from operator import contains


def countFee(computer_amount):

    if (computer_amount == 1 or computer_amount == 2):
        base_fee = 50
        additional_fee = 0

    elif (computer_amount >= 3 and computer_amount <= 10):
        base_fee = 100
        additional_fee = 10

    elif (computer_amount > 10):
        base_fee = 500
        additional_fee = 10

    return base_fee, additional_fee

def business_hour_checker(service_time,business_hour):

    if (not contains(service_time, business_hour)):
        base_fee = base_fee ** 2

    return base_fee

def drop_pick(customer):
    
    if(willDropOff(customer) and willPickUp(customer)):
        base_fee = base_fee - (base_fee*0.5)
    
    return base_fee

