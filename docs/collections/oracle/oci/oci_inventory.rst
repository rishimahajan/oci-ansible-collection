.. Document meta

:orphan:

.. Anchors

.. _ansible_collections.oracle.oci.oci_inventory:

.. Anchors: short name for ansible.builtin

.. Anchors: aliases



.. Title

oracle.oci.oci -- Oracle Cloud Infrastructure (OCI) inventory plugin
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. Collection note

.. note::
    This plugin is part of the `oracle.oci collection <https://galaxy.ansible.com/oracle/oci>`_ (version 2.12.0).

    To install it use: :code:`ansible-galaxy collection install oracle.oci`.

    To use it in a playbook, specify: :code:`oracle.oci.oci`.

.. version_added


.. contents::
   :local:
   :depth: 1

.. Deprecated


Synopsis
--------

.. Description

- Get inventory hosts from oci.
- Uses a <name>.oci.yaml (or <name>.oci.yml) YAML configuration file.


.. Aliases


.. Requirements


.. Options

Parameters
----------

.. raw:: html

    <table  border=0 cellpadding=0 class="documentation-table">
        <tr>
            <th colspan="2">Parameter</th>
            <th>Choices/<font color="blue">Defaults</font></th>
                            <th>Configuration</th>
                        <th width="100%">Comments</th>
        </tr>
                    <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-api_user_key_file"></div>
                    <b>api_user_key_file</b>
                    <a class="ansibleOptionLink" href="#parameter-api_user_key_file" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                            <div>
                                env:OCI_USER_KEY_FILE
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>Full path and filename of the private key (in PEM format). If the key is encrypted with a pass-phrase, the pass_phrase option must also be provided. Preference order is .oci.yml &gt; OCI_USER_KEY_FILE environment variable &gt; settings from config file This option is required if the private key is not specified through a configuration file (See config_file)</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-api_user_key_pass_phrase"></div>
                    <b>api_user_key_pass_phrase</b>
                    <a class="ansibleOptionLink" href="#parameter-api_user_key_pass_phrase" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                            <div>
                                env:OCI_USER_KEY_PASS_PHRASE
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>Passphrase used by the key referenced in api_user_key_file, if it is encrypted. Preference order is .oci.yml &gt; OCI_USER_KEY_PASS_PHRASE environment variable &gt; settings from config file This option is required if the passphrase is not specified through a configuration file (See config_file)</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-cache"></div>
                    <b>cache</b>
                    <a class="ansibleOptionLink" href="#parameter-cache" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">boolean</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                                                                                    <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li><div style="color: blue"><b>no</b>&nbsp;&larr;</div></li>
                                                                                                                                                                                                <li>yes</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                    <div> ini entries:
                                                                    <p>
                                        [inventory]<br>cache = no
                                                                                                                    </p>
                                                            </div>
                                                                            <div>
                                env:ANSIBLE_INVENTORY_CACHE
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>Toggle to enable/disable the caching of the inventory&#x27;s source data, requires a cache plugin setup to work.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-cache_connection"></div>
                    <b>cache_connection</b>
                    <a class="ansibleOptionLink" href="#parameter-cache_connection" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                    <div> ini entries:
                                                                    <p>
                                        [defaults]<br>fact_caching_connection = None
                                                                                                                    </p>
                                                                    <p>
                                        [inventory]<br>cache_connection = None
                                                                                                                    </p>
                                                            </div>
                                                                            <div>
                                env:ANSIBLE_CACHE_PLUGIN_CONNECTION
                                                                                            </div>
                                                    <div>
                                env:ANSIBLE_INVENTORY_CACHE_CONNECTION
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>Cache connection data or path, read cache plugin documentation for specifics.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-cache_plugin"></div>
                    <b>cache_plugin</b>
                    <a class="ansibleOptionLink" href="#parameter-cache_plugin" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                                    <b>Default:</b><br/><div style="color: blue">"memory"</div>
                                    </td>
                                                    <td>
                                                    <div> ini entries:
                                                                    <p>
                                        [defaults]<br>fact_caching = memory
                                                                                                                    </p>
                                                                    <p>
                                        [inventory]<br>cache_plugin = memory
                                                                                                                    </p>
                                                            </div>
                                                                            <div>
                                env:ANSIBLE_CACHE_PLUGIN
                                                                                            </div>
                                                    <div>
                                env:ANSIBLE_INVENTORY_CACHE_PLUGIN
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>Cache plugin to use for the inventory&#x27;s source data.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-cache_prefix"></div>
                    <b>cache_prefix</b>
                    <a class="ansibleOptionLink" href="#parameter-cache_prefix" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                                    <b>Default:</b><br/><div style="color: blue">"ansible_inventory_"</div>
                                    </td>
                                                    <td>
                                                    <div> ini entries:
                                                                    <p>
                                        [default]<br>fact_caching_prefix = ansible_inventory_
                                                                                                                    </p>
                                                                    <p>
                                        [inventory]<br>cache_prefix = ansible_inventory_
                                                                                                                    </p>
                                                            </div>
                                                                            <div>
                                env:ANSIBLE_CACHE_PLUGIN_PREFIX
                                                                                            </div>
                                                    <div>
                                env:ANSIBLE_INVENTORY_CACHE_PLUGIN_PREFIX
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>Prefix to use for cache plugin files/tables</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-cache_timeout"></div>
                    <b>cache_timeout</b>
                    <a class="ansibleOptionLink" href="#parameter-cache_timeout" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">integer</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                                    <b>Default:</b><br/><div style="color: blue">3600</div>
                                    </td>
                                                    <td>
                                                    <div> ini entries:
                                                                    <p>
                                        [defaults]<br>fact_caching_timeout = 3600
                                                                                                                    </p>
                                                                    <p>
                                        [inventory]<br>cache_timeout = 3600
                                                                                                                    </p>
                                                            </div>
                                                                            <div>
                                env:ANSIBLE_CACHE_PLUGIN_TIMEOUT
                                                                                            </div>
                                                    <div>
                                env:ANSIBLE_INVENTORY_CACHE_TIMEOUT
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>Cache duration in seconds</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-compartments"></div>
                    <b>compartments</b>
                    <a class="ansibleOptionLink" href="#parameter-compartments" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                         / <span style="color: purple">elements=string</span>                                            </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>A dictionary of compartment identifier to obtain list of hosts. This config parameter is optional. If compartment is not specified, the plugin fetches all compartments from the tenancy</div>
                                                        </td>
            </tr>
                                        <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-compartments/compartment_name"></div>
                    <b>compartment_name</b>
                    <a class="ansibleOptionLink" href="#parameter-compartments/compartment_name" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Name of the compartment. If None and `compartment_ocid` is not set, all the compartments including the root compartment are returned.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-compartments/compartment_ocid"></div>
                    <b>compartment_ocid</b>
                    <a class="ansibleOptionLink" href="#parameter-compartments/compartment_ocid" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>OCID of the compartment. If None, root compartment is assumed to be the default value.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-compartments/fetch_hosts_from_subcompartments"></div>
                    <b>fetch_hosts_from_subcompartments</b>
                    <a class="ansibleOptionLink" href="#parameter-compartments/fetch_hosts_from_subcompartments" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">boolean</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                                        <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li>no</li>
                                                                                                                                                                                                <li>yes</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Flag used to fetch hosts from subcompartments. Default value is set to True</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-compartments/parent_compartment_ocid"></div>
                    <b>parent_compartment_ocid</b>
                    <a class="ansibleOptionLink" href="#parameter-compartments/parent_compartment_ocid" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>This option is not needed when the compartment_ocid option is used, it is needed when compartment_name is used. OCID of the parent compartment. If None, root compartment is assumed to be parent.</div>
                                                        </td>
            </tr>
                    
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-compose"></div>
                    <b>compose</b>
                    <a class="ansibleOptionLink" href="#parameter-compose" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">dictionary</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                                    <b>Default:</b><br/><div style="color: blue">{}</div>
                                    </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Create vars from jinja2 expressions.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-config_file"></div>
                    <b>config_file</b>
                    <a class="ansibleOptionLink" href="#parameter-config_file" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                            <div>
                                env:OCI_CONFIG_FILE
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>The oci config path.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-config_profile"></div>
                    <b>config_profile</b>
                    <a class="ansibleOptionLink" href="#parameter-config_profile" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                            <div>
                                env:OCI_CONFIG_PROFILE
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>The config profile to use.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-debug"></div>
                    <b>debug</b>
                    <a class="ansibleOptionLink" href="#parameter-debug" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">boolean</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                                        <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li>no</li>
                                                                                                                                                                                                <li>yes</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Parameter to enable logs while running the inventory plugin. Default value is set to False</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-enable_parallel_processing"></div>
                    <b>enable_parallel_processing</b>
                    <a class="ansibleOptionLink" href="#parameter-enable_parallel_processing" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Use multiple threads to speedup lookup. Default is set to True</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-fetch_db_hosts"></div>
                    <b>fetch_db_hosts</b>
                    <a class="ansibleOptionLink" href="#parameter-fetch_db_hosts" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>When set, the db nodes are also fetched.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-filters"></div>
                    <b>filters</b>
                    <a class="ansibleOptionLink" href="#parameter-filters" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>A dictionary of filter value pairs. Available filters  are display_name, lifecycle_state, availability_domain, defined_tags, freeform_tags.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-groups"></div>
                    <b>groups</b>
                    <a class="ansibleOptionLink" href="#parameter-groups" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">dictionary</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                                    <b>Default:</b><br/><div style="color: blue">{}</div>
                                    </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Add hosts to group based on Jinja2 conditionals.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-hostname_format"></div>
                    <b>hostname_format</b>
                    <a class="ansibleOptionLink" href="#parameter-hostname_format" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                            <div>
                                env:OCI_HOSTNAME_FORMAT
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>Host naming format to use. Use &#x27;fqdn&#x27; to list hosts using the instance&#x27;s Fully Qualified Domain Name (FQDN). These FQDNs are resolvable within the VCN using the VCN resolver specified through the subnet&#x27;s DHCP options. Please see https://docs.us-phoenix-1.oraclecloud.com/Content/Network/Concepts/dns.htm for more details. Use &#x27;public_ip&#x27; to list hosts using public IP address. Use &#x27;private_ip&#x27; to list hosts using private IP address. By default, hosts are listed using public IP address.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-hostnames"></div>
                    <b>hostnames</b>
                    <a class="ansibleOptionLink" href="#parameter-hostnames" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>A list of hostnames to search for.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-instance_principal_authentication"></div>
                    <b>instance_principal_authentication</b>
                    <a class="ansibleOptionLink" href="#parameter-instance_principal_authentication" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                            <div>
                                env:OCI_ANSIBLE_AUTH_TYPE
                                                                                            </div>
                                                                    </td>
                                                <td>
                                            <div>Use instance principal based authentication. If not set, the API key in your config will be used.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-keyed_groups"></div>
                    <b>keyed_groups</b>
                    <a class="ansibleOptionLink" href="#parameter-keyed_groups" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                         / <span style="color: purple">elements=string</span>                                            </div>
                                                        </td>
                                <td>
                                                                                                                                                                    <b>Default:</b><br/><div style="color: blue">[]</div>
                                    </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Add hosts to group based on the values of a variable.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-plugin"></div>
                    <b>plugin</b>
                    <a class="ansibleOptionLink" href="#parameter-plugin" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                 / <span style="color: red">required</span>                    </div>
                                                        </td>
                                <td>
                                                                                                                            <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li>oracle.oci.oci</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>token that ensures this is a source file for the &#x27;oci&#x27; plugin.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-regions"></div>
                    <b>regions</b>
                    <a class="ansibleOptionLink" href="#parameter-regions" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>A list of regions to search. If not specified, the region is read from config file. Use &#x27;all&#x27; to generate inventory from all subscribed regions.</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-strict"></div>
                    <b>strict</b>
                    <a class="ansibleOptionLink" href="#parameter-strict" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">boolean</span>
                                                                    </div>
                                                        </td>
                                <td>
                                                                                                                                                                                                                    <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li><div style="color: blue"><b>no</b>&nbsp;&larr;</div></li>
                                                                                                                                                                                                <li>yes</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>If <code>yes</code> make invalid entries a fatal error, otherwise skip and continue.</div>
                                            <div>Since it is possible to use facts in the expressions they might not always be available and we ignore those errors by default.</div>
                                                        </td>
            </tr>
                        </table>
    <br/>

.. Notes


.. Seealso


.. Examples

Examples
--------

.. code-block:: yaml+jinja

    
    # Fetch all hosts
    plugin: oci

    # Optional fields:
    config_file: ~/.oci/config
    config_profile: DEFAULT

    # Example select regions
    regions:
      - us-ashburn-1
      - us-phoenix-1

    # Enable threads to speedup lookup
    enable_parallel_processing: yes

    # Select compartment by ocid or name
    compartments:
      - compartment_ocid: ocid1.compartment.oc1..xxxxxx
        fetch_hosts_from_subcompartments: false

      - compartment_name: "test_compartment"
        parent_compartment_ocid: ocid1.tenancy.oc1..xxxxxx

    # Example filtering using hostname IP
    hostnames:
      - "11.145.214.11"

    # Example filtering using hostname_format
    hostname_format: "private_ip"

    # Example group results by key
    keyed_groups:
      - key: availability_domain

    # Example using filters
    filters:
      - availability_domain: "IwGV:US-ASHBURN-AD-3"
      - display_name: "instance20190506231645"
      - lifecycle_state: "RUNNING"
      - defined_tags: {
         "ansible_tag_2": {
           "ansibletag448": "test_value"
          }
        }
      - freeform_tags: {
         "oci:compute:instanceconfiguration": "ocid1.instanceconfiguration.oc1.phx.xxxx",
         "oci:compute:instancepool": "ocid1.instancepool.oc1.phx.xxxx"
        }

    # Example flag to turn on debug mode
    debug: true

    # Enable Cache
    cache: yes
    cache_plugin: jsonfile
    cache_timeout: 7200
    cache_connection: /tmp/oci-cache
    cache_prefix: oci_

    # DB Hosts
    fetch_db_hosts: True




.. Facts


.. Return values


..  Status (Presently only deprecated)


.. Authors



.. Parsing errors

