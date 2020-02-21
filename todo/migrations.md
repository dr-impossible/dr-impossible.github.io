# Database Migrations

* why migrations are important
    * they will save your sanity
    * they are tracked
    * they help you share schema changes
        * do you really want to spend time calculating schema changes by hand?
* seed scripts
    * useful test data. you may not want to or be able to work with production data
    * clean room approach to working with data, double-edged sword
    * if thought out carefully, will help you understand your data
    * it's ok to use models here
    * for a test or dev database, you'll need to re-create your schema somehow
        * ActiveRecord generates a schema snapshot after running migrations and uses this to re-create the schema
        * Sequelize.sync() will dynamically sync the database to match your models
        * MongoDB doesn't have schemas
* don't load models in migrations
    * you may be tempted to do this for data migrations
    * models likely to be ahead of the migration and will fail to load
    * model validations and type checking may interfere with the changes you're making
    * your ORM's native query interface is more helpful here
* models are safe to use in seeds, and probably preferred
    * it's assumed that you'll run seeds on a fully updated schema
* down/reverse migrations
    * helpful when working with others or switching between branches
        * is there a way to determine which migrations to roll back before switching branches? using git-diff?
    * may help for rollback of risky changes
* logging
    * log the record id before performing the operation, in case of failure
    * log pass/fail
* error handling
    * are partial failures acceptable?
* separate schema migrations from data migrations
    * or just always use the native query interface

## Out of scope
* stored procedures
    * I've never used this in a real application, when are they useful, how do you deal?