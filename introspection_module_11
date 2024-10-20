from pprint import pprint


def introspection_info(obj):
    # тип
    obj_type = type(obj)

    # атрибуты
    attributes = dir(obj)

    # методы
    methods = [attr for attr in attributes if callable(getattr(obj, attr))]

    # принадлежить модуля
    module = obj_type.__module__

    # другие свойства
    properties = {}
    if hasattr(obj, '__dict__'):
        properties['__dict__'] = obj.__dict__
    if hasattr(obj, '__name__'):
        properties['__name__'] = obj.__name__
    if hasattr(obj, '__doc__'):
        properties['__doc__'] = obj.__doc__

    info = {'type': obj_type.__name__, 'attributes': attributes, 'methods': methods, 'module': module,
            'properties': properties}

    return info


str_info = introspection_info('привет')
pprint(str_info)
