# removed test logging_test.py file

from loguru import logger

# DEBUG
# INFO
# WARNING
# ERROR
# CRITICAL


# logger.add('info.log' , level="INFO")
# logger.add('critical.log' , level="CRITICAL")
# logger.add('warning.log' , level="WARNING")
# logger.add('debug.log',level="DEBUG")

# logger.add('app.log' , rotation='1 MB', compression='zip', retention='1 MINUTE')
# logger.add('app.log' , rotation='13:15')
# logger.add('app.log' , rotation='1 week')

logger.add("app.log", diagnose=False, backtrace=False)
# @logger.catch


def divide_by(a, b):
    # logger.info("calculating..")
    # logger.debug(f"calculating.. a={a}, b={b}")
    # logger.warning(f"b shouldnd be zero")

    return a / b


try:
    res = divide_by(2, 0)
    print(res)
except:
    # logger.critical("division by 0 !!")
    logger.error("division by 0 !!")
