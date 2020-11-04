.. _clusterdetails:

------------------------
HPoC Cluster Details
------------------------

Cluster Hardware Details
++++++++++++++++++++++++


**Für den Hosted PoC wurde ein System mit 4 Nodes in 2 Höheneinheiten reserviert:**

.. figure:: images/cluster3060g5a.png

.. note::
  Bedenken Sie bitte, dass diese Testumgebung zum nicht zwangsläufig  auf der neuesten Hardware basiert und das zum anderen auf Grund der Entfernung zum Lab-Datacenter entsprechende Latenzen auftreten können. Nichtsdestotrotz lassen sich mit dieser Umgebung die typischen Routineaufgaben bzgl. einer Nutanix-Cluster-Plattform mit einer ausgezeichneten User-Experience testen.

Infrastruktur IPs
+++++++++++++++++

.. list-table::
   :widths: 10 10 10 10
   :header-rows: 1

   * - Nodes
     - CVMs
     - Hypervisors
     - IPMI
   * - **Position A**
     - 10.42.29.29
     - 10.42.29.25
     - 10.42.29.33
   * - **Position B**
     - 10.42.29.30
     - 10.42.29.26
     - 10.42.29.34
   * - **Position C**
     - 10.42.29.31
     - 10.42.29.27
     - 10.42.29.35
   * - **Position D**
     - 10.42.29.32
     - 10.42.29.28
     - 10.42.29.36


.. list-table::
  :widths: 20 20
  :header-rows: 1

  * - Services
    - IP-Adressen
  * - **Cluster virtual IP**
    - 10.42.29.37
  * - **iSCSI Data Services IP**
    - 10.42.29.38
  * - **Prism Central**
    - 10.42.29.39
  * - **Active Directory**
    - 10.42.29.41


Zugangsdaten
++++++++++++

Die folgende Tabelle führt die standardmäßig hinterlegten Zugangsdaten für die Umgebung auf (falls andere zum Einsatz kommen sollten wird dies gesondert aufgeführt):

.. list-table::
  :widths: 20 20 10
  :header-rows: 1

  * - Name
    - Benutzername
    - Passwort
  * - **IPMI**
    - ADMIN
    - ADMIN
  * - **Prism Element Web**
    - admin
    - nx2Tech342!
  * - **Prism Element SSH**
    - nutanix
    - nx2Tech342!
  * - **Prism Central Web**
    - admin
    - nx2Tech342!
  * - **Prism Central SSH**
    - nutanix
    - nutanix/4u
  * - **NTNXLAB Domain**
    - NTNXLAB\\Administrator
    - nutanix/4u
  * - **CentOS VM Image**
    - root
    - nutanix/4u


Frame-VDI
++++++++++++


Die folgende Tabelle führt die Zugangsdaten zur Frame-VDI Umgebung auf:

Melden Sie sich auf folgende Website mit Ihren Zugangsdaten an: https://frame.nutanix.com/x/labs

.. list-table::
  :widths: 20 20
  :header-rows: 1

  * - Benutzername
    - Passwort
  * - PHX-POC029-User01 ... PHX-POC029-User20
    - nx2Tech342!

NTNXLAB.local Active-Directory-Services
++++++++++++

Darüber hinaus besitzt der Cluster eine dedizierte Domain-Controller-VM, welche die Active-Directory-Services für die **NTNXLAB.local** Domain bereitstellt. Die Domain wurde mit den folgenden Nutzern und Gruppen vorkonfiguriert:

.. list-table::
  :widths: 20 20 10
  :header-rows: 1

  * - Gruppe
    - Benutzername(n)
    - Passwort
  * - **Administrators / Domain Admins**
    - Administrator
    - nutanix/4u
  * - **Bootcamp Users**
    - User01-User25
    - nutanix/4u
  * - **SSP Admins**
    - Adminuser01-Adminuser25
    - nutanix/4u
  * - **SSP Operators**
    - Operator01-Operator25
    - nutanix/4u
  * - **SSP Developers**
    - Devuser01-Devuser25
    - nutanix/4u
  * - **SSP Consumers**
    - Consumer01-Consumer25
    - nutanix/4u
  * - **SSP Custom**
    - Custom01-Custom25
    - nutanix/4u

Netzwerk
++++++++

Die folgenden virtuellen Netzwerke wurden wie folgt vorkonfiguriert:

.. list-table::
   :widths: 33 33 33
   :header-rows: 1

   * -
     - **Primäres** Netzwerk
     - **Sekundäres** Netzwerk
   * - **VLAN**
     - 0
     - 2063
   * - **Netzwerk IP Adresse**
     - 10.42.29.0
     - 10.42.29.128
   * - **Netzmaske**
     - 255.255.255.128 (/25)
     - 255.255.255.128 (/25)
   * - **Default Gateway**
     - 10.42.29.1
     - 10.42.29.129
   * - **IP Address Management (IPAM)**
     - Aktiviert
     - Aktiviert
   * - **DHCP Pool**
     - 10.42.29.50  - 125
     - 10.42.29.132 - 253
   * - **Domain**
     - NTNXLAB.local
     - NTNXLAB.local
   * - **DNS**
     - 10.42.29.41 (DC VM)
     - 10.42.29.41 (DC VM)
