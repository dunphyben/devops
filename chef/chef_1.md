1) Create a chef recipe that writes a hash from an attribute into a YAML file.

2) What's the sticky bit?

3) Write me a database query that joins 3 tables: A node table, an
environment table and a organization table, join all 3 and give me all
nodes in the hello organization and the prod and staging environments.

4) Write a ruby script that converts a JSON file into a YAML file

5) Write a few sentences on how nagios works, then write a few more on
why you like it or do not like it.

6) If you had to write a system that did rolling restarts across many
servers and only one service could be down at a time, how would you
accomplish that?

7)Tell me about the worst disaster that you dealt with.

## Chef
#### Handles the configuration of your servers in Ruby code

a. Keeps things DRY
b. Save time
c. Less likely to make mistakes
d. New servers have same policy
e.

    AGILE MOVEMENT
    * Manages aspects of your servers or computers by using code. Does nto mean using a bunch of text files! Uses a Ruby domain specific language, or DSL.
        * This abstracts away implementation on how to configure your servers.
        * In chef, resources and providers are the magical abstration layer.
            **Resource**: Says wahat actions should be taken.
                If want to install a pkg, use the package resource.
                Also use the resource to manage services.
            **Providers**: How to perform the actions.
                Provider corresponding to the resource will perform the action.
        Idempotency: If something is idempotent, you should be able to run chef repeatedly without changing the outcome.
            Strongly encouraged by Chef.
    Why use Chef?
        A. SETUP
            1. Base operating system like Ubuntu or Redhat
            2. Packages and dependencies
            3. Database like Postgres
            4. Web Server like inginx or apache
            5. App Server like Unicorn or Passenger
            6. Load Balancer like H-A Proxy or Varnish
            This is only for a simple app! If you have multiple servers and are doing things like replication, configuring everything by hand gets very tedious.
        B. ABSTRACTION
            1. User doesn't need to know how actions are performed.
            2. Write same code for all different systems. Extensibility to infinity
            3. Anyone can cook (code).
            4. The days of a single-point of failure (i.e. 1 person knows how the system works) are over!




