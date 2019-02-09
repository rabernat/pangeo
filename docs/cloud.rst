.. _deployments:

Pangeo Cloud Federation
=======================

Pangeo provides cloud computing services to the geoscience community.
The Jupyter Hubs listed here are generally open to all scientists working in
specific disciplines, and they come loaded with the latest Pangeo software.

If none of these meets your needs, it's easy to deploy your own Pangeo in
the cloud provider of your choice.

{% for cloud in cloud_deployments %}

.. rst-class:: cloud

{{ cloud.name }}
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. raw:: html

    <img height="80px" class="pull-right" src="_static/{{ cloud.image }}">

    <div class="clearfix"></div>


{% for hub in cloud.hubs %}

.. rst-class:: jhub

{{ hub.name }}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. raw:: html

    <div class="row">
      <div class="col-sm-3">
        <a class="btn btn-primary" href="{{ hub.link }}" role="button">launch &nbsp; <img src="_static/jupyter-logo.svg"></a>
      </div>
      <div class="col-sm-9">
        {{ hub.description }}
      </div>
    </div>

{% endfor %}

{% endfor %}
