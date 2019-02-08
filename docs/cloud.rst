.. _deployments:

Pangeo Cloud Federation
=======================


{% for cloud in cloud_deployments %}

.. raw:: html

    <img height="80px" class="pull-right" src="_static/{{ cloud.image }}">

{{ cloud.name }}
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

{% for hub in cloud.hubs %}

.. rst-class:: jhub

{{ hub.name }}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. raw:: html

    <div class="row">
      <div class="col-sm-3">
        <a class="btn btn-primary btn-round-lg" href="{{ hub.link }}" role="button">Launch <img src="_static/jupyter-logo.svg"></a>
      </div>
      <div class="col-sm-9">
        {{ hub.description }}
      </div>
    </div>

{% endfor %}

{% endfor %}
