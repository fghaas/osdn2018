## Instance auto-expiry

Note:
This is admittedly fairly advanced, but if you have a need for
something like this, it’s a very neat trick.


### Mistral
<https://docs.openstack.org/mistral/>

Note:
Mistral is a workflow execution engine. It comes as part of the
OpenStack codebase, but your public cloud service provider (or private
cloud deployment engine) may or may not make it available to you.


### Some assembly required
(actually, rather lots of it)

Note:
Mistral support in private cloud deployments is not great, indeed
Puppet is probably the only way that you can deploy Mistral in an
automated fashion. (All credit to CERN for that support.)

There is a [Juju charm for
Mistral](https://github.com/openstack/charm-mistral), but
unfortunately it hasn’t seen much love in 2 years.


### Clever use of instance properties


```
task(retrieve_all_projects)
  .result
  .select(dict(id => $.id,
               name => $.name,
               enabled => $.enabled,
               type => $.get('type','none'),
               expire => $.get('expire','off')))
  .where($.type='personal')
  .where($.enabled)
  .where($.expire='on')
```
[YAQL](https://yaql.readthedocs.io/en/latest/)


<https://goo.gl/p3YzTT>

OpenStack in Production (CERN)
