## Release Notes

- 6.0.0:
    - django support for 2.2-4.1
    - python support for 3.7-3.9
- 5.1.1:
    - Fix logic holes related to the active flag when generating entity group cache
- 5.1.0:
    - Add decorator to suppress entity syncing
- 5.0.2:
    - Only fetch new entities on a sync_all
- 5.0.1:
    - Fix bug where an entity created or deleted during a sync would cause errors
- 5.0.0:
    - Django 3.0, Django 3.1
    - Drop Django 2.0, 2.1 support
- 4.2.0:
    - Python 3.7, Django 2.2
- 4.1.1:
    - When calling the activation events, ignore entities that are initially inactive
- 4.1.0:
    - Add support for properly calling activation events when entities change
- 4.0.9:
    - Bump manager utils.
    - Update upserts and syncs to be non native to save wasting auto incrementing ids
- 4.0.8:
    - BAD RELEASE DO NOT USE
- 4.0.7:
    - When using the defer entity syncing decorator, do not call sync if the buffer is empty
- 4.0.6:
    - Relax entity update lock to be less aggressive by using `FOR NO KEY UPDATE` lock instead the `FOR UPDATE`. This will allow the updates to not block on other parts of the system that are foreign keyed to entity
- 4.0.5:
    - Add retry logic, and select for update calls during entity syncing
- 4.0.4:
    - Update logging to be debug instead of info
- 4.0.3:
    - Add locking during sync method
    - Add support for deferring entity syncing using a decorator
- 4.0.2:
    - Fix a bug where the is_active flag for entity kinds was being updated during syncing
- 4.0.1:
    - Upgrade manager utils for faster syncs
- 4.0.0:
    - Optimize entity syncing and change syncing interface
- 3.1.2:
    - Fix hole in deletion where a model could be added during syncing
- 3.1.1:
    - Remove 1.10 from setup file
- 3.1.0:
    - Add jsonfield encoder (drop support for 1.10)
- 3.0.0:
    - Add tox to support more versions
    - Switch to django's JSONField
- 2.0.2:
    - Removed celery requirement
- 2.0.1:
    - Return only active entities by default in membership cache method
- 2.0.0:
    - Remove python 2.7 support
    - Remove python 3.4 support
    - Remove Django 1.9 support
    - Remove Django 1.10 support
    - Add Django 2.0 support
- 1.18.1:
    - Reduce number of queries and data selected
- 1.18.0:
    - Optimize entity group queries by providing cache building functions
- 1.17.0:
    - Drop Django 1.8 support
    - Add Django 1.10 support
    - Add Django 1.11 support
    - Add python 3.6 support
- 1.15.0:
    - Remove SyncEntitiesTask, this task should live within the main application that entities is installed within
- 1.11.0:
    - Added support for arbitrary groups of entities.
- 1.10.0:
    - Added Django 1.8 support.
- 1.9.0:
    - Updated Entity Kinds to be activatable models.
- 1.8.2:
    - Added sorting support for Entity Models in Python 3
- 1.8.0:
    - Added support for Django 1.7 and also backwards-compatible support for Django 1.6.
- 1.7.1:
    - Changed the ``is_entity_active`` function in the entity configuration to be named ``get_is_active`` for consistency with other functions.
- 1.6.0:
    - Made entities ``activatable``, i.e. they inherit the properties defined in [Django Activatable Model](https://github.com/ambitioninc/django-activatable-model)
- 1.5.0:
    - Added entity kinds to replace inadequacies of filtering by entity content types.
    - Removed is_any_type and is_not_any_type and replaced those methods with is_any_kind and is_not_any_kind in the model manager.
    - Removed chainable entity filters. All entity filtering calls are now in the model manager.
