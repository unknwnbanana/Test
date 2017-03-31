CTL Zenoss Incident Response Recipes
====================================

-   [**Important Client
    Notes**](#CTLZenossIncidentResponseRecipes-Import)

-   [**CTL Queue Workflow **](#CTLZenossIncidentResponseRecipes-CTLQue)

-   [**Training**](#CTLZenossIncidentResponseRecipes-Traini)

-   **[Checklist for Escalated
    Support](#CTLZenossIncidentResponseRecipes-Checkl) **

    -   [**Postman
        Collection**](#CTLZenossIncidentResponseRecipes-Postma)

-   [**IP Address Blocks, Control URL and VPN for Each
    Datacenter**](#CTLZenossIncidentResponseRecipes-IPAddr)

-   **[Important IPs and
    Links](#CTLZenossIncidentResponseRecipes-Import) **

    -   [**Z-controller**](#CTLZenossIncidentResponseRecipes-Z-cont)

    -   [**Z-Console**](#CTLZenossIncidentResponseRecipes-Z-Cons)

    -   [**Provisioner**](#CTLZenossIncidentResponseRecipes-Provis)

    -   [**Kibana**](#CTLZenossIncidentResponseRecipes-Kibana)

    -   [**Sync Gateway**](#CTLZenossIncidentResponseRecipes-SyncGa)

-   [**Terms**](#CTLZenossIncidentResponseRecipes-Terms)

-   [**Concepts and FYIs**](#CTLZenossIncidentResponseRecipes-Concep)

-   [**CTL Alert
    Procedures **](#CTLZenossIncidentResponseRecipes-CTLAle)

-   **[Checking Kibana graphs (CTL Zenoss
    Dashboard)](#CTLZenossIncidentResponseRecipes-Checki) **

    -   [**Process**](#CTLZenossIncidentResponseRecipes-Proces)

    -   **[Tier 1: Watching the
        data](#CTLZenossIncidentResponseRecipes-Tier1:) **

        -   [**TOTAL MESSAGE
            THROUGHPUT**](#CTLZenossIncidentResponseRecipes-TOTALM)

    -   [**TIER 2: INITIAL INCIDENT INVESTIGATION /
        RESPONSE**](#CTLZenossIncidentResponseRecipes-TIER2:)

    -   **[TIER 2: KIBANA INCIDENT RESPONSE
        RECIPES](#CTLZenossIncidentResponseRecipes-TIER2:) **

        -   [**Symptoms of overloaded Z-Node observed in Z-Console
            dashboard**](#CTLZenossIncidentResponseRecipes-Sympto)

        -   [**Symptoms of overloaded Z-Node observed in Kibana
            dashboard**](#CTLZenossIncidentResponseRecipes-Sympto)

        -   [**Site-wide outage / Uniform drop in volume across
            datacenters**](#CTLZenossIncidentResponseRecipes-Site-w)

        -   [**Kibana 4 auto-post in Slack's \#cascade-operations room
            fails with a Red
            status**](#CTLZenossIncidentResponseRecipes-Kibana)

        -   [**CTL Kibana 4 Multiple Failures to
            Login**](#CTLZenossIncidentResponseRecipes-CTLKib)

-   **[Deadman's Snitch (DMS)
    alerts](#CTLZenossIncidentResponseRecipes-Deadma) **

    -   **[TIER 1: SPOT
        CHECKS](#CTLZenossIncidentResponseRecipes-TIER1:) **

        -   [**Examples of
            alerts**](#CTLZenossIncidentResponseRecipes-Exampl)

        -   [**SPOT CHECK: Datacenter message volume hasn’t checked
            in**](#CTLZenossIncidentResponseRecipes-SPOTCH)

        -   [**SPOT CHECK: Global message volume hasn’t checked
            in**](#CTLZenossIncidentResponseRecipes-SPOTCH)

        <!-- -->

        -   **[Z-group/Zenoss Node Spot
            Check](#CTLZenossIncidentResponseRecipes-Z-grou) **

            -   [**Examples of
                alerts**](#CTLZenossIncidentResponseRecipes-Exampl)

            -   [**Spot check
                overview**](#CTLZenossIncidentResponseRecipes-Spotch)

            -   [**Spot check
                example**](#CTLZenossIncidentResponseRecipes-Spotch)

            -   [**Thresholds for
                noc@cascadeo.com**](#CTLZenossIncidentResponseRecipes-Thresh)

-   **[TIER 1 INCIDENT
    RECIPES](#CTLZenossIncidentResponseRecipes-TIER1I) **

    -   [**Problem: Maximum threshold for unhealthy count. Removing node
        &lt;SOME NODE&gt; from service. Health: Error creating failure
        event.**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[CTL PROD\] &lt;SOME DEVICE&gt; Evaluation failed
        due to ... &lt;some message about a missing
        expression&gt;**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[CTL PROD\] LB1-\*\*\*\* Alerts. Or any alerts from
        LB1 or network
        10.247.7.X**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[CTL PROD\] Device xxx is unmodeled/ Device xxx has
        not been modelled for xxx
        hours**](#CTLZenossIncidentResponseRecipes-Proble)

-   **[TIER 2 INCIDENT
    RECIPES](#CTLZenossIncidentResponseRecipes-TIER2I) **

    -   [**Problem: Unable to use ssh\_node to access a node in Chef
        Workstation.**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[CTL PROD\] \$HOST\_NAME: Command ModelDeviceAPI
        failed**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**&lt;XXPROVISIONER&gt;Unable to replace un-SEEDED znode. Set
        force to true to force
        replacement**](#CTLZenossIncidentResponseRecipes-<XXPRO)

    -   [**HOWTO: Verify CTL/Platform API
        Issue**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**Problem: Provisioner XXXXPROVISIONER: Manual bootstrap
        returned with non-zero
        code.**](#CTLZenossIncidentResponseRecipes-Proble)

    -   -   [**Problem: \[CTL PROD\] \$HOST\_NAME: no \$GROUP
        directory.\$DIR does not exist.Run bin/rancid-cvs \$GROUP to
        make all of the needed
        directories**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[CTL PROD\] \$HOST\_NAME: \$GROUP/router.db
        file.\$DIR/router.db does not
        exist**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[CTL PROD\] rancid-cvs has failed on
        %s **](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[CTL PROD\] The following routers have not been
        successfully contacted for: \$msgtxt" \$HOST\_NAME: config
        fetcher problems -
        \$GROUP**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Z-GROUP Safe
        Mode**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Horizontal Scaling of Worker Z-Nodes or
        Z-Trap**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[GLOBAL Z-CONSOLE\] localhost localhost
        zenperfdataforwarder heartbeat
        failure**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[MISSING\] GLOBAL R8 Z-cosystem Inventory and
        Config Backup**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**HOWTO : Launch / Restore
        Z-Console**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**HOWTO :  Get Zenoss zProperties using
        zendmd**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**HOWTO : Reduce the workload on a running Z-Node by
        rebalancing **](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**PROBLEM: \[MISSING\] Global R8 OOM KILLER INVOCATIONS hasn't
        checked in**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**  HOWTO: Modify the Memory of a CTL Z-group
        Provisioner/node/master**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**Problem: Global R8 OOM Killer Invocations Snitch Missing Due
        To Provisioner OOM**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**HOWTO : Disable / Enable Chaos
        Monkey**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**HOWTO : Add vCenters for
        monitoring**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   -   [**Problem: Z-node appears to be stuck in SEEDING
        state**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: (HOW TO RE-SEED) SEEDING\_STATE\_TIMEOUT Error
        during seeding**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Forcing Zseed of
        Znode/Zmaster/Ztrap**](#CTLZenossIncidentResponseRecipes-Proble)

    -   **[Problem: Forcing Z-Node
        Replacement](#CTLZenossIncidentResponseRecipes-Proble) **

        -   [**Option 1: Using
            z-api**](#CTLZenossIncidentResponseRecipes-Option)

        -   [**Option 2:
            Manual**](#CTLZenossIncidentResponseRecipes-Option)

    -   [**Problem: ZMaster Seeding is stuck in "SEEDING\_QUEUED"
        state**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: ZMaster Seeding is stuck for a long (time &gt;9
        hours) and also receiving an unexpected:
        SoftTimeLimitExceeded()**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Updating Syslog/SNMP Trap Load Balancer
        Config**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: zseed: Adding / Updating / Removing Devices from
        Inventory**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Rebalancing Polling Workload across Worker
        Z-Nodes**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Provisioner/Z-Comms Heartbeat;
        PROVISIONER\_HEALTH\_NOK**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Provisioner &lt;Provisioner&gt; heartbeat is older
        than 600 seconds. Last heartbeat received was xxxxxxx.xx with
        status OK.**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Provisioning
        failures**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Znode &lt;ZNODE&gt;: Acquire on closed
        pool**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Error: Znode: No JSON object could be
        decoded**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: In &lt;ZNODE&gt;: 'findposkeyerror -v10' command
        returned with exit
        status 1.**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Duplicate zcomms.messaging consumers causing zseed
        failure**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem:
        XXXPROVISIONER HTTPConnectionPool(host='10.128.131.201',
        port=5984): Read timed out. (read
        timeout=5). **](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Restart Zenoss in
        ZNodes/ZConsole**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Reinstating Z-Node into Provisioner's State DB
        (Split-Brain
        Scenario)**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Component: /opt/zenoss/perf threshold of Greater
        than 90 percent used not
        met**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Error Code: Maximum provisioning retries
        reached**](#CTLZenossIncidentResponseRecipes-ErrorC)

    -   [**Problem:  \[GLOBAL Z-CONSOLE\] &lt;ZNODE NAME&gt; &lt;ZNODE
        IP&gt; is DOWN!**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[MISSING\] &lt;Datacenter&gt; Message Volume hasn't
        checked in**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Zenoss down alerts for
        x.x.x.200**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem : \[MISSING\] &lt;Datacenter&gt; Z-MASTER / ZNode
        hasn't checked in**](#CTLZenossIncidentResponseRecipes-Proble)

    -   **[Problem : \[MISSING\] &lt;Datacenter&gt; STATE
        Z-TRAPLOGXX hasn't checked
        in](#CTLZenossIncidentResponseRecipes-Proble) **

        -   [**Possible cause: How to spot the nature of the
            storm**](#CTLZenossIncidentResponseRecipes-Possib)

        -   [**Possible cause: Unable to resolve DMS endpoint domain or
            local resolver
            issue**](#CTLZenossIncidentResponseRecipes-Possib)

    -   [**Problem:  \[MISSING\] &lt;Datacenter&gt; RABBITMQ hasn't
        checked in**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[GLOBAL Z-CONSOLE\] HTTP CRITICAL: HTTP/1.1 500
        Internal Server
        Error **](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Threshold of Free Swap Not
        Met**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[MISSING\] &lt;SOME INDIVIDUAL DEVICE&gt; hasn't
        checked in**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[MISSING\] &lt;Datacenter&gt; \*-vsphere Message
        Volume hasn't checked
        in**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[MISSING\] &lt;Datacenter&gt; \*-event Message
        Volume hasn't checked
        in**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[MISSING\] ESMsgVolume &lt;Datacenter&gt; hasn't
        checked in**](#CTLZenossIncidentResponseRecipes-Proble)

    -   -   [**Problem: This operation is restricted by the
        administrator - 'vpxd.stats.maxQueryMetrics'. Contact your
        system
        administrator**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[MISSING\] ESMsgVol Exemption List hasn't checked
        in**](#CTLZenossIncidentResponseRecipes-Proble)

    -   -   [**Problem:\[GLOBAL Z-CONSOLE\] &lt;COUCHDB\_SERVER&gt;
        threshold of Greater than 40 percent used not met: current value
        XXXX on /home/couchdb
        mountpoint**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[GLOBAL Z-CONSOLE\] VA1ZGPPROXY01/02 Connection
        Refused**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[GLOBAL Z-CONSOLE\] XXXX HTTP WARNING: HTTP/1.1 404
        Not Found**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[GLOBAL Z-CONSOLE\] VA1ZGPWEB0X/0Y threshold of
        API\_Proxy not met: current value
        -2000.000000**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Found orphaned node &lt;hostname&gt; (&lt;ip&gt;) in
        &lt;DC&gt;**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Found IP address (&lt;ip&gt;) in &lt;DC&gt; with
        unknown hostname. **](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**HOWTO: Identifying a CTL Event
        Storm**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**HOWTO: Get to a znode monitoring a certain
        device**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**HOWTO: Enabling -ops (one packet scheduling) on the ZGP load
        balancer (ipvsadm)**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [** COUCHDB-related connection refused (aborted)
        errors**](#CTLZenossIncidentResponseRecipes-COUCHD)

    -   [** Symptom: Most connection refused errors from Z-Console are
        due to CouchDB being out of service. The following assets or
        systems use
        CouchDB:**](#CTLZenossIncidentResponseRecipes-Sympto)

    -   [**\[GLOBAL Z-CONSOLE\] 10.128.131.27 (or .19) threshold of
        Greater than xx percent used not met: current value
        xx**](#CTLZenossIncidentResponseRecipes-[GLOBA)

    -   [**INFORMATION: COUCHDB, proxy related alerts (those are from
        IPs 10.128.131.12, .13, .19,
        .27)**](#CTLZenossIncidentResponseRecipes-INFORM)

    -   [**INFORMATION: 'Update: Ticket
        bucket'**](#CTLZenossIncidentResponseRecipes-INFORM)

    -   [**INFORMATION: Disregard DMS alerts coming from
        CA2R8D0xx**](#CTLZenossIncidentResponseRecipes-INFORM)

    -   [**INFORMATION: CTL Z-Console:  Anything with a count greater
        than 100**](#CTLZenossIncidentResponseRecipes-INFORM)

    -   [**HOWTO: Diagnosing a Z-Node DMS Health
        Issue**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**Problem: Provisioner &lt;provisioner&gt;: Unable to reset IP
        of &lt;Z-Master/Z-Node&gt; in zconsole OR IP address conflicts
        between nodes in
        Z-Console**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: Could not connect to Redis at 127.0.0.1:6379:
        Connection refused**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: ZENRABBIT PROVISIONING\_TIMEOUT
        reached.**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: \[MISSING\] &lt;DATACENTER&gt; ZGPZENRABBIT hasn't
        checked in**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: 10.128.131.202: Datasource HttpMonitor/HttpMonitor
        command timed out**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**HOWTO: Testing the Kafka
        Brokers**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**PROBLEM: How to manually replace IPVS with Samplicator to
        load balance UDP \[syslogs, snmp traps\] (Whenever a ZTRAP is
        replaced in NY1)**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**HOWTO: Smoketest
        https://zen.mon.ctl.io/**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   -   [**PROBLEM: Missing DMS &lt;VA1ZDMZ | ZGP&gt; "Chef Data Bag
        to Couchbase Sync" or "Couchbase to Chef Data Bag
        Sync"**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   **[PROBLEM: Rogue/Stale Workers Causing Celery Worker Heartbeat
        Queue (celeryev) to Back
        Up](#CTLZenossIncidentResponseRecipes-PROBLE) **

        -   [**ISSUE: RABBITMQ DATABASE MNESIA IS CONSUMING A LOT OF
            DISK**](#CTLZenossIncidentResponseRecipes-ISSUE:)

        -   [**ISSUE: BACKING UP OF SOME
            QUEUES **](#CTLZenossIncidentResponseRecipes-ISSUE:)

    -   [**PROBLEM: SNMP agent down (for CTL monitored devices only, not
        for zNodes or Cascadeo managed
        resources)**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: host\_table =
        (rabbit\_details\['internal\_ipaddr'\], rabbit) KeyError:
        'internal\_ipaddr'**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: Juniper NetConf
        Alerts**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: Devices were not found while running zb\_commit
        script to update backup version (CONFIG PUSH
        RELATED)**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: ZenRancid Backup
        alerts**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: TypeError: expected integer key when browsing
        Infrastructure tab, Zenpython shutting
        down**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: \[Errno 113\] No route to host from AMQP transport
        (Z-group RabbitMQ)**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   **[PROBLEM: getSecrets(): raise HTTPError(http\_error\_msg,
        response=self) requests.exceptions.HTTPError: 404 Client Error:
        Not Found](#CTLZenossIncidentResponseRecipes-PROBLE) **

        -   [**Cause: pouchcouch (node.js app on port 3000) is
            down.**](#CTLZenossIncidentResponseRecipes-Cause:)

        -   [**Cause: Sync Gateway is
            down**](#CTLZenossIncidentResponseRecipes-Cause:)

        -   [**Cause: Sync Gateway is
            slow**](#CTLZenossIncidentResponseRecipes-Cause:)

    -   [**PROVISIONER:
        PROVISIONER\_SEEDING\_ZNODE\_FAILURE**](#CTLZenossIncidentResponseRecipes-PROVIS)

    -   [**PROBLEM: BadStatusLine
        in validate\_zcontroller()**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: Provisioner: Can't retry
        zcomms.provisioner.provisioner.poll\_modeling\_status**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**Problem: celery@heartbeat.xxxxxxxxxxxxxx.DC worker tasks
        are backing up.**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**Problem: No new ZenBackup image in
        ZController**](#CTLZenossIncidentResponseRecipes-Proble)

    -   **[PROBLEM: ConnectionError: ('Connection aborted.',
        BadStatusLine('',)) in
        provisioners](#CTLZenossIncidentResponseRecipes-PROBLE) **

        -   [**Case: The CLC (Centurylink Cloud) API call is
            failing**](#CTLZenossIncidentResponseRecipes-Case:T)

        -   [**Case: The manifest (inventory) fetch is
            failing**](#CTLZenossIncidentResponseRecipes-Case:T)

    -   [**PROBLEM: \[GLOBAL Z-CONSOLE\] VA1ZGPAPI05 Datasource
        HttpMonitor/HttpMonitor Swagger API Functionality command timed
        out**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: Provisioner \[DC\]R82ZGPPROVISIONER: maximum
        recursion depth exceeded while calling a Python
        object**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: &lt;SOME DC&gt;PROVISIONER: "Response code 408”
        exception in provisioner.cleanup\_zgroup()
        call**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**RECIPE: BULK UPDATE DATACENTER
        MANIFEST**](#CTLZenossIncidentResponseRecipes-RECIPE)

    -   [**Resource: VA1ZGPSYNCGW{02,03,04 or more} Component: / Event
        Class: /Perf/Filesystem Status: New Message: threshold of
        Greater than &lt;SOME PERCENTAGE THRESHOLD&gt; percent used not
        met: current value &lt;SOME
        VALUE&gt;**](#CTLZenossIncidentResponseRecipes-Resour)

    -   [**PROBLEM: SEEDING IS STILL NOT TRIGGERED EVEN AFTER INCREMENT
        OF MANIFEST VERSION**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: Disk space issue for
        /var/lib/mysql**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: \[DC\]PROVISIONER: Cannot replace ztrap at the
        moment. Check overall ztrap
        health.**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: Task configLoader configure
        failed**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: &lt;urlopen error  \[Errno 111\] Connection
        refused&gt;**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: \[zenoss\] &lt;device name&gt; vSphere Connection /
        authentication
        failed**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: &lt;SOME DATACENTER&gt; PROVISIONER hasn't checked
        in**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**Re: \[Sentry\] \[Cascadeo Internal\] &lt;SOME EXCEPTION
        MESSAGE&gt;**](#CTLZenossIncidentResponseRecipes-Re:[Se)

    -   [**How to modify the IP address of a device if requested by CTL
        teams**](#CTLZenossIncidentResponseRecipes-Howtom)

    -   **[How to re-mediate Z-console slow
        down](#CTLZenossIncidentResponseRecipes-Howtor) **

        -   [**Re-index via
            zendmd**](#CTLZenossIncidentResponseRecipes-Re-ind)

        -   [**Clean mysql data dir and restore
            zenbackup**](#CTLZenossIncidentResponseRecipes-Cleanm)

    -   [**PROBLEM: Unable to update ZNODE details in Z-Console - needs
        manual update**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: Unable to set state of &lt;ZNODE&gt; to production
        in z-console. Reset state manually in
        z-console**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: Error running parser
        error**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: ReadConflictError in NODE\_NAME, device
        DEVICE\_NAME" &lt; --- title message = "DEVICE\_NAME modeling
        encountered 'ReadConflictError: database read conflict
        error**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: \[zenoss\] global z-console from
        &lt;DC&gt;z-console-zenoss-http-check Datasource HttpMonitor -
        ZENOSS/ZENOSS command timed
        out**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**PROBLEM: HTTPmonitor connection timed out from &lt;DC&gt; to
        va1**](#CTLZenossIncidentResponseRecipes-PROBLE)

    -   [**Problem: XXXR82ZGPPROVISIONER \[Errno 32\] Broken
        pipe**](#CTLZenossIncidentResponseRecipes-Proble)

    -   [**requires operator intervention as it will almost certainly
        not clear itself.**](#CTLZenossIncidentResponseRecipes-requir)

    -   [**HOWTO: find a rogue z-node sending alerts for devices already
        set to maintenance mode
        (prodstate=300)**](#CTLZenossIncidentResponseRecipes-HOWTO:)

    -   [**PROBLEM: Get devices does not return device after adding
        device in
        zen.mon.ctl.io**](#CTLZenossIncidentResponseRecipes-PROBLE)

### **Important Client Notes**

1.  If there are events that need to wait (e.g. node replacements) at
    least acknowledge them so that the next person knows they are not a
    new problem. In other words I think the Z-Console should be either
    clear or 100% but never left in a state where there are
    unacknowledged alarms.

2.  If you see Z-Console alarms about CPU, swapping, or free memory,
    just acknowledge them on the Z-Console dashboard and leave them. 
    They will trigger automated workload rebalancing and should
    clear after a while.  It may take several hours for them to clear.
     If they become stuck forever, I need to study them and determine
    why workload rebalancing didn't solve the problem. The geeky
    details:  If thresholds around CPU/swap/freemem are breached,
    trigger -&gt; notify -&gt; drain.l The idea is that over time, this
    should automatically/gradually distribute the workload fairly
    across the Z-Nodes in the Z-Group. If you want to monitor the
    workload migration activity, tail -f /opt/zenoss/log/zenactiond.log
    on the Z-Console.  You'll see drain running there periodically as
    those triggering conditions are met.

3.  Specifically, any time there is a Zenoss node that is swapping
    (threshold of Free Swap not met on Z-Console) that node must be
    replaced using the standard node replacement recipe. Do not allow
    nodes that are swapping to persist, as they are degraded.

4.  Any nodes that are swapping or suffering from disk full need to be
    replaced via the swagger API at <https://zen.mon.ctl.io/docs>

5.  Can also add more Z-Nodes via horizontal scaling
    https://zen.mon.ctl.io/docs/\#!/Node/create to address load issues.

6.  Any CTL Monitoring tickets that cannot be handled by T2 have owner
    set to "Monitoring/Jared Reimer". Anything not set to
    "Monitoring/Jared Reimer" as owner (or assigned to another named CTL
    team member) will be considered T2 territory and untouched.  Note
    the 24 hour SLA please.

7.  Watch the Z-Console events dashboard. Those events with high count
    should clear automatically as those nodes get replaced. If any of
    them persist, please have someone look into it. 

### **CTL Queue Workflow **

![C:\\05d401c2a2625cc04a9b85318219b8a7](media/image1.tmp){width="4.875in"
height="1.1458333333333333in"}

**Source: <https://drive.google.com/open?id=0B27_NGn3dF0KUEF2em5OaldjQTg>**

### **Training**

1.  See
    checklist: [ChecklistforEscalatedSupport](#CTLZenossIncidentResponseRecipes-Checkl)

2.  [CTL Cloud guides](https://www.ctl.io/guides/) (***BIG NOTE***:
    ***DO NOT*** attach or use a public IP in any server instance)

    1.  Dev environment: JRMT (locate only in CA2, create your own
        server group, delete what you don't need)

    2.  Servers (compute instances)

    3.  Using the API

    4.  Connect to the internal work using VPN
        (<https://www.ctl.io/vpn/#Resources>)

        1.  Note the [OpenVPN UDP fragmentation
            issue](https://cascadeo.atlassian.net/wiki/display/CLCDEV/OpenVPN+UDP+fragmentation+issue),
            you might be affected

3.  **[Zenoss training
    guides](https://cascadeo.atlassian.net/wiki/display/ZL1S/9.+Documentation+and+References)
    (from our Zenoss L1 support team)**

    1.  [Zenoss bootstrapping
        guide](file:///C:\wiki\display\CLCDEV\Zenoss+bootstrapping+guide)

    2.  Quick read Zenoss Core Administration 4.2.5 (download
        in <https://www.zenoss.com/services-support/documentation/archive>)

4.  Chef training guides **(NOTE: Choose RHEL or CentOS 7 for the
    walkthrough, keep in mind CTL uses RHEL/CentOS 6)**

    1.  Sign up for a trial account in linuxacademy and take the course
        - <https://linuxacademy.com/devops/training/course/name/certified-chef-developer-basic-chef-fluency-badge>

        1.  Take a screenshot of the course progress bar as proof for
            doing the course.

        2.  Do the chef practice project.
            - <https://docs.google.com/document/d/195aK6W7Pers8ShO956GsgBjkQdeDVczNzz2wpbU_J3o>

    2.  Additional Guides and Resources

        1.  Learn the Basics -
            <https://learn.chef.io/tutorials/learn-the-basics/>

        2.  Manage a Node -
            <https://learn.chef.io/tutorials/manage-a-node/>

        3.  Chef Documentation - <https://docs.chef.io/> 

        4.  Chef Resource Reference -
            <https://docs.chef.io/resources.html>

    3.  [Sample Web App for Chef Server and Chef
        Solo.](https://github.com/joshuajorel/chefbootstrap) **(NOTE:
        Practice by doing the additional work.)**

    4.  Best Practices 

        1.  Internal wiki -
            <https://cascadeo.atlassian.net/wiki/display/syseng/Chef+Best+Practices>

        2.  FB git -
            <https://github.com/facebook/chef-utils/blob/master/Philosophy.md>

    5.  Further Learning

        1.  Community Cookbooks - <https://github.com/chef-cookbooks>

        2.  Chef Supermarket - <https://supermarket.chef.io>

        3.  Skills Library - <https://learn.chef.io/skills/>

        4.  Style guide -
            <https://github.com/pulseenergy/chef-style-guide>

        5.  AWS Opsworks - <https://aws.amazon.com/opsworks/>

    6.  TODO: CTL Zenoss Automation

5.  **Training from 8/11/15 - [WebEx
    Format](file:///C:\wiki\download\attachments\43909190\CTL%20Tier%202%20Training-20150811%200401-1.arf%3fversion=1&modificationDate=1439336766897&cacheVersion=1&api=v2) | [MP4](file:///C:\wiki\download\attachments\43909190\CTL%20Tier%202%20Training-20150811%200401-1.mp4%3fversion=1&modificationDate=1439336297914&cacheVersion=1&api=v2)**

6.  **2/19/16 Tutorial on Horizontal Scaling - [WebEx
    Format](file:///C:\wiki\download\attachments\43909190\CTL%20Walk-through%20of%20Horizontal%20Scaling%20of%20Worker%20Z-Nodes-20160219%200600-2.arf%3fversion=1&modificationDate=1455885505789&cacheVersion=1&api=v2)**

7.  [**7/04/16 CTL Kibana
    4 walk-through**](file:///C:\wiki\download\attachments\43909190\CTL%20K4%20walk-through-gzWkyT7nJ0o.mp4%3fversion=1&modificationDate=1467754149631&cacheVersion=1&api=v2)

8.  **7/9/16 [CTL Walk-through - hacking panels and sub-aggregations in
    Kibana4](file:///C:\wiki\download\attachments\43909190\CTL%20Walk-through%20-%20hacking%20panels%20and%20sub-aggregations%20in%20Kibana4-XuVmeqpdGAI.mp4%3fversion=1&modificationDate=1468113634714&cacheVersion=1&api=v2)**

9.  7/18/16 [CTL Walk-through: Chef workstation and knife
    ssh](https://www.youtube.com/watch?v=iaFLIcqOozo) (cascadeo.com
    account only)

10. [How to use Kibana to explore data and create
    visualization](https://support.ctl.io/hc/en-us/articles/211669403-How-to-use-Kibana-to-explore-data-and-create-visualization)
    (CTL Zendesk KB)

11. 7/28/16 CTL Couchbase Sync Gateway Walk-through for
    T2's [(segment1)](https://www.youtube.com/watch?v=TH9Nnrm92SQ)[(segment2)](https://www.youtube.com/watch?v=oonlcmiC3fw)[(segment3)](https://www.youtube.com/watch?v=D857qLmCA3Q) ([slides
    /
    outline](https://docs.google.com/a/cascadeo.com/presentation/d/1JjyovfWh-3CrbxURIzPgk0ySEKkvnVPxH6OY1hnhEAw/edit?usp=sharing))

    1.  [Find the z-node assigned to monitor a device using the
        manifest](https://docs.google.com/presentation/d/1JjyovfWh-3CrbxURIzPgk0ySEKkvnVPxH6OY1hnhEAw/edit?pli=1#slide=id.g1a8ba7d27b_0_0)

12. (DevOps) ['ELK as a Service'
    Onboarding](https://x.ctl.io/teams/0e0dff97f710efa3/wikis/0f10a5d9b1108a81) \[use
    ctl.io credentials\]

13. (DevOps) <http://wiki.zenoss.org/ZenPack_Development_Guide>

14. [CTL Automated Kibana / Elasticsearch
    monitoring](file:///C:\wiki\pages\viewpage.action%3fpageId=91848729)

15. (DevOps) [Q&A on metric timestamps in
    zenperfdataforwarder](file:///C:\wiki\pages\viewpage.action%3fpageId=91848749)

16. zcomms task queue workers
    ([slides](https://docs.google.com/presentation/d/1K14AWihQlKofbrT0miSEtvYQ9EHzjDsaIpX5O-ydPTc/edit#slide=id.p)
    / [session](https://www.youtube.com/watch?v=J2F-xhX8Sjo))

17. (November 30, 2016) [Z-API
    walk-through](https://www.youtube.com/watch?v=1_X9xTeJsx4)

18. (December 1, 2016) [Jenkins and Sentry
    walk-through](https://youtu.be/EnjV7tNKaD4)
    (slides: [ctl\_jenkins\_sentry.pdf](file:///C:\wiki\download\attachments\43909190\ctl_jenkins_sentry.pdf%3fversion=1&modificationDate=1480593773966&cacheVersion=1&api=v2))

19. (December 5, 2016) [CTL Zenoss Alerting Config
    Walkthrough](https://youtu.be/AFXBjORdoPA) (slides: [CTL Zenoss
    Alerting Config
    Walkthrough.pptx](https://docs.google.com/presentation/d/1QurrpiiCq6lM45y9cNeDSatn0rfXRaNhSjjWGumzh84/edit))

20. CTL walk-through: UDP load balancer for syslogs and snmp traps
    ([recording](https://youtu.be/LlE1kgwM5vc) /
    [slides](file:///C:\wiki\download\attachments\43909190\ctl_udp_lb.pdf%3fversion=1&modificationDate=1481351023854&cacheVersion=1&api=v2))

21. [Z-WebUi and Z-API
    Development](https://docs.google.com/document/d/1CrBdAcD7ZlKLCaO8EzIAecldj5gK1sMFhNOnEgN0_wk/edit)
    (c/o Jerome and Waldemar)

### **Checklist for Escalated Support**

1.  Slack rooms: \#cascadeo-operations, \#internal-ctl

2.  Intro key people: 

    1.  Jared (Lead)

    2.  Prem / Jerome (zcomms and others)

    3.  Leo / Abigail (Zenoss automation, ops and others)

    4.  Peter / Gabriel (ZenPacks and others)

3.  Subscribe to this page ([CTL Zenoss Incident Response
    Recipes](file:///C:\wiki\display\CLCDEV\CTL+Zenoss+Incident+Response+Recipes))

4.  LastPass folder: Shared-Cascadeo-NOC-Tier 2\\CTL (c/o Chris Ellis) 

    1.  Shared-Centurylink (for CTL Devops)

5.  Guidelines on asking help from <help@ctl.io>

    1.  CTL is *OUR* customer

    2.  Ask help from our NOC or CTL Devops first

    3.  Always include your [Support PIN in your
        request](https://www.ctl.io/knowledge-base/support/pin-authentication-for-support-requests/)

    4.  Some recipes mention sending an email to <help@ctl.io> to route
        a question to certain CTL Team (e.g. CTL Analytics Team)

        1.  Be clear which team the request should be routed and who the
            team leader is

        2.  Make it clear we are from Cascadeo working under the Zenoss
            Monitoring Group

        3.  The team leader from our side is Jared Reimer
            (jared@cascadeo.com)

        4.  CC ctl-dev@cascadeo.com

6.  Access the [Production CTL Control
    Dashboard](https://control.ctl.io/Organization/user/userprofile)
    (Account Alias: ZGP, not JRMT!) to [find your personal support
    PIN](https://www.ctl.io/knowledge-base/support/pin-authentication-for-support-requests/).
    You will need this to email [help@ctl.io](mailto:noc@tier3.com) (CTL
    NOC). Always carbon-copy (CC) ctl-dev@cascadeo.com
    and <noc@cascadeo.com> so they can receive updates.

7.  Control Dashboard accounts and where to get the VPN profile:

    1.  LB1 (pre-prod): <https://control.dev.ctl.io/network/vpn>

    2.  JRMT (dev): <https://control.ctl.io/network/vpn> (NOTE: servers
        have to reside in CA2)

    3.  ZGP (this is **production**!): <https://control.ctl.io> (NOTE:
        You can login only one account at a time). For the VPN profile,
        see the item below.

8.  **[CTL Production
    VPN](file:///C:\wiki\display\CLCDEV\CTL+Production+VPN) **(required
    for Tier 2) ~~or get the profile
    from <https://control.ctl.io/Network/vpn>~~

    1.  Note the [OpenVPN UDP fragmentation
        issue](file:///C:\wiki\display\CLCDEV\OpenVPN+UDP+fragmentation+issue),
        you might be affected

    2.  Needs OTP (get from RJ)

9.  How to [Obtain the IP
    addresses](file:///C:\wiki\display\CLCDEV\Obtain+the+IP+addresses)

10. Access to the CTL Zenoss Instances (Creds in LP)

11. [CTL Active Directory access for CTL Analytics
    Kibana/ES](file:///C:\wiki\pages\viewpage.action%3fpageId=76414980),
    you need to be added to the kibana-ie-authors AD group (get from RJ)

    1.  After getting your Active Directory account, setup the
        self-service password change
        in <https://kibana-cascadeo.analytics.ctl.io/login?next=%2F>.
        You will need this when your password expires.

    2.  If your credentials suddenly do not work, your password might
        have expired. Reset
        using <https://passwordchange.ctl.io:8443/accounts/Reset>

12. Access to the [Kibana Zenoss
    Dashboard](https://kibana-cascadeo.analytics.ctl.io) (Use AD
    account)

13. Check IP address blocks for each datacenter below

14. Access to [CTL Zendesk Monitoring
    Queue](https://t3n.zendesk.com/agent/) (as ctl-dev@cascadeo.com, in
    LastPass)

    1.  Any updates (internal or external) made in this Zendesk instance
        can be viewed by the client (CTL)

    2.  Queue search filter: *Group:Monitoring Status&lt;Solved*

    3.  There is *no need* to use the Pending status because the
        requester always has a Zendesk account. Assign the ticket to the
        requester and keep it OPEN.

15. [Cascadeo Zendesk](https://cascadeo.zendesk.com/agent/dashboard)
    (c/o Chris Ellis & RJ)

16. Access to Trello board (Zenoss Active Sprint) (individual account)

17. Trello: [Zenoss Active Sprint
    board](https://trello.com/b/Apvxz91w/zenoss-active-sprint) /
    Production System Operations column

18. Search using \`vi\` or
    \`vim\`: <http://staff.washington.edu/rells/R110/#intermed10>

    1.  Tip: in command mode type \$ (goes to the end of the buffer)

    2.  Then ?&lt;text to search&gt;

19. Z-API: <https://zen.mon.ctl.io/swagger>

    1.  ~~[Whitelist your
        IP](https://cascadeo.atlassian.net/wiki/pages/viewpage.action?spaceKey=CLCDEV&title=CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-HOWTO:Smoketesthttps://zen.mon.ctl.io/)
        or~~

    2.  (preferred) [Connect to ZDMZ VPN and hard-code zen.mon.ctl.io
        address](file:///C:\wiki\display\CLCDEV\Connect+to+ZDMZ+VPN+and+hard-code+zen.mon.ctl.io+address)

    3.  Only *svc\_zenoss2* account works for now

20. Subscribe to <https://status.ctl.io/subscription>

21. [Sentry triage
    workflow](https://docs.google.com/a/cascadeo.com/document/d/1v83dubMr_hcmSAH9R6fuk9mGHXsStURuMmPe3KSBl5g/edit?usp=sharing)

#### Postman Collection

-   [Postman
    Collection](https://drive.google.com/open?id=0B73fCgmnslHUR2NGU3RyUENySUk)
    for Couchbase Sync Gateway API requests

### IP Address Blocks, Control URL and VPN for Each Datacenter

  **Address Block**   **Datacenter**   **\*Account**   **Control URL**                 **VPN Config (see LastPass)**
  ------------------- ---------------- --------------- ------------------------------- -------------------------------
  10.160.8.0          AU1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.51.72.0          CA1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.56.153.0         CA2              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.100.107.0        CA3              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.110.119.0        DE1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.60.112.0         GB1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.105.99.0         GB3              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.92.142.0         IL1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.241.7.0          LB1              ZGP             <https://control.dev.ctl.io/>   LB1
  148.156.13.0        NE1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.71.168.0         NY1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.130.73.0         SG1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.121.186.0        UC1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.95.147.0         UT1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.128.131.0        VA1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.166.3.0          VA2              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.81.25.0          WA1              ZGP             <https://control.ctl.io/>       VA1/SG1
  10.241.102.0        LB1              DMZ             <https://control.dev.ctl.io/>   LB1
  10.137.128.0        VA1              ZDMZ            <https://control.ctl.io/>       VA1/SG1

\*Choose account by clicking on the account header after logging in
control. See screenshots.

![C:\\413b6241b57a1dad7e65a0a9aac1c2f2](media/image2.tmp){width="4.364583333333333in"
height="2.0520833333333335in"}![C:\\bc1d5886a14f6041b50e0cbb3df5559b](media/image3.tmp){width="4.541666666666667in"
height="2.28125in"}

### Important IPs and Links

#### Z-controller

va1zgpzcntlxx : 10.128.131.17 (zenoss: <http://10.128.131.17:8080>)

The Z-controller is the source of the zenbackup (zenoss backup)
image. We do all configuration in z-controller, take a snapshot (called
the zenbackup) and ship it to all z-nodes. The shipping is also called
*config push*. It is important to configure Z-controller correctly
because its configuration is propagated to **ALL** z-nodes. It is also a
good idea to write a change log (screenshot, \`diff\`, or notes) when
modifying the Z-controller.

#### Z-Console

va1zgpzconsolxx: 10.128.131.100

#### Provisioner

For each data center, find an instance name &lt;DC&gt;ZGPPROVRXX. For
example, the provisioner in VA1 is VA1ZGPPROVR18

#### Kibana

[kibana-cascadeo.analytics.ctl.io](http://kibana-cascadeo.analytics.ctl.io) -
Kibana instance dedicated to Cascadeo / CTL Zenoss Monitoring Team.

<https://kibana.analytics.ctl.io/availability.html> -  availability
dashboard for the whole Analytics / ELK as a service product. This shows
the overall availability and message latencies along with breakdowns by
pipeline and DC.

#### Sync Gateway

Sync Gateway is the API gateway to the Couchbase Cluster which hosts the
manifest files (monitoring inventory).

LB1 (preprod environment / CTL's dev environment that we need to
monitor): <http://10.241.7.15:4984>

ZGP (prod): <http://10.128.131.220:4984>

### Terms

1.  **Seeding***.* When the z-node is started it is almost empty. It is
    seeded with the zenoss backup image from Z-controller. Seeding tasks
    have time limits: znode seeding timeout is *1 hour*, zmaster seeding
    timeout is *9 hours*. If a node is stuck in seeding for more than
    the time limit, you can execute this recipe to
    re-seed: <https://cascadeo.atlassian.net/wiki/pages/viewpage.action?spaceKey=CLCDEV&title=CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-Problem:(HOWTORE-SEED)SEEDING_STATE_TIMEOUTErrorduringseeding>

2.  **Z-node replacement or reprovisioning**. A z-node instance (VM) is
    terminated and replaced (with the same z-node ID but different VM
    instance ID). *Do *not*
    confuse [Problem:(HOWTORE-SEED)SEEDING\_STATE\_TIMEOUTErrorduringseeding](#CTLZenossIncidentResponseRecipes-Proble) (*force
    re-seeding*) with *reprovisioning*. They are different.*

3.  **CTL Control Dashboard**. <https://control.ctl.io>

4.  **Z-console**. This is a special Zenoss instance that resides in VA1
    that is used to monitor z-nodes and other z-group operations related
    services.

5.  **Rabbits. **They are the RABBITMQ nodes used for queueing. There
    are two rabbitmq nodes in a z-group. One is for z-group's zcomms
    operations (celery's queueing backend) and the other one is for
    queueing performance data messages (to be forwarded to CTL
    Analytics). They are named like the following examples.

    1.  IL1R82ZGPZENRABBIT - for zenoss performance data queueing

    2.  IL1R82ZGPRABBIT - z-group's zcomms celery rabbitmq backend

### Concepts and FYIs

1.  All -event devices are expected to be *not modeled*. You can click
    Graphs to see how many events were collected from vSphere or use
    Kibana to see the forwarded countI

2.  Ignore alerts for LB1 DMZ indefinitely

### CTL Alert Procedures 

1.  **Tier 1** - Every CTL alarm that needs escalated (DMS, Kibana,
    Zenoss) - escalate to Tier 2

2.  **Tier 2** - Evaluate each alarm against the recipes that [have been
    built in the
    wiki](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes).

    1.  If no recipes match - and we expect this to almost always be the
        case early on - ESCALATE to the CTL Team.

    2.  If a recipe matches but there are problems (login issues,
        unexpected inputs/outputs, unclear) - ESCALATE to the CTL Team -
        do not guess or make assumptions, escalate if you are unsure

3.  **CTL Team** - follow these steps

    1.  Stabilize or fix the issue that was alerted. Make sure that it
        is resolved, including ensuring that all alarms have cleared and
        tickets are closed.

    2.  If the task was something thatTier 2 could have fixed or the
        recipe did not work create a \*new\* ticket (CC: cellis) to get
        that fixed. If possible fix the recipe in the wiki right away.

### **Checking Kibana graphs (CTL Zenoss Dashboard)**

#### Process

1.  Tier 1 is to look at the graphs and make a determination if an
    escalation is required to Tier 2

2.  IF an escalation is needed:

    1.  Trigger escalation to the general SysEng group (Tier 1)

    2.  Create a ticket to track the issue (Tier 1) and assign to the
        responding engineer

3.  Tier 2 completes deeper investagion tasks

    1.  Update \#internal-ctl Slack channel at every critical step

    2.  Update Ticket at every critical step (make sure it CC's
        ctl@cascadeo.com)

4.  Close ticket once we confirm there is no issue or it has been
    escalated to the CTL team (Tier 2).

#### Tier 1: Watching the data

Every 30 minutes we need to look at the [Kibana graph for
CTL](https://kibana-cascadeo.analytics.ctl.io/app/kibana#/dashboard/Zenoss-Dashboard).
You will get a screenshot in \#cascadeo-operations or \#internal-ctl
Slack channels. There are **TWO** graphs to monitor on this page.

First and Foremost

First and foremost in the first graph (IE\_ZENOSS: TOTAL MESSAGE
THROUGHPUT BY DC):  **Ignore the right-most and left-most portion of the
graph.**  Why?  The final data point renders incorrectly.

##### **TOTAL MESSAGE THROUGHPUT**

For the **TOTAL MESSAGE THROUGHPUT (MESSAGES PER INTERVAL)** graph we
are looking for **sudden changes in the pattern**.

***NOTE:*** The graphs below are from the **NEW CTL Kibana (v4.5.1)**
Zenoss dashboard.

![C:\\72a950e2a55136957e13682275094118](media/image4.tmp){width="4.875in"
height="1.5729166666666667in"}

What to check in IE\_ZENOSSDEBUG pipeline...

The graph below is a *split chart.* Each column graphs the message
volume (ie\_zenossdebug pipeline only) of a datacenter (e.g. VA1,
GB3..). ****The spikes are normal****. Watch out for visible gaps.

![C:\\3e4c746c73bba935995675b4370c648c](media/image5.tmp){width="4.875in"
height="1.4895833333333333in"}

Any issue triggers an escalation to the Tier 2 team
"[page@tier2. ](mailto:page@tier2.)

#### **TIER 2: INITIAL INCIDENT INVESTIGATION / RESPONSE**

1.  Go to the \#internal-ctl Slack channel and document everything you
    do carefully.  This information will be used for forensics in RFO
    etc. so please leave a good trail of bread-crumbs for your coworkers
    to follow. Use the DNS name of the device instead of the device name
    when writing the report for the CTL team. Example:\
    uc1r8rc2zgpzmaster | 10.121.186.12 | running\
    uc1r8rc2zgpztrap01 | 10.121.186.26 | running

2.  Study the TOTAL MESSAGE THROUGHPUT BY DC (MESSAGES PER SECOND) graph
    in the Kibana Zenoss Dashboard and attempt to isolate the
    datacenter(s) encountering instability.  Larger spikes in the
    derivative graphs imply a sudden change in message volume; sudden
    changes to message volume are a leading indicator of problems.

3.  Establish a ZGP VPN connection. See the [bootstrapping
    checklist](#CTLZenossIncidentResponseRecipes-Bootst) for other
    access needed.

4.  Use [https://control.ctl.io/](http://control.ctl.io/) to identify
    the datacenter and app deployment in question. For example, if there
    is data missing or fluctuating in volume from "SG1" in the TOTAL
    MESSAGE THROUGHPUT graphs above, find the SG1 deployment in Control.

5.  [Obtain the IP
    addresses](file:///C:\wiki\display\CLCDEV\Obtain+the+IP+addresses) of
    the MASTR, ZNODE, and TRAPLOG instances, there may be more than one
    of each.  These nodes each run the Zenoss Core v4.2.5 application
    stack independently.  Record these to \#internal-ctl Slack
    channel as they may change as nodes are replaced automatically.
     Note:  Problems with the other node types will require escalation
    to the CTL on-call engineering team.

6.  For each of the collected IP addresses,
    visit <http://ip.address:8080/> and login as "admin" using the
    shared credential in LastPass.   (Keep all tabs open concurrently.)
      Click on INFRASTRUCTURE at the top.

7.  Look at the MASTR.  It is a warm stand-by that can sub in for a
    ZNODE when a ZNODE is offline.  In normal operations, the inventory
    of devices being monitored by the MASTR should be empty except for
    "localhost."   You can ignore any device that is not set to
    "Production" as this node is not monitoring them at this time.  If
    you see devices other than "localhost" set to "Production" that
    implies that one or more ZNODEs are offline, possibly updating
    themselves or broken.   Record findings \#internal-ctl Slack channel

8.  Look at the ZNODEs.  These do the actual polling / alerting in
    routine operations. For each device set to "Production" inspect the
    device and make sure it is modeled.  Look at the "Model Time" as
    shown in the screenshot below.  If the device is NOT modeled, you
    can invoke it manually using the gear at the bottom-left.  Modeling
    can take a very long time for some devices, or almost no time for
    others.  You will know the modeler is done when it says something
    like this:

> 2015-05-18 18:51:41,303 INFO zen.ZenModeler: Changes in configuration
> applied
>
> 2015-05-18 18:51:41,304 INFO zen.ZenModeler: Scan time: 1.23 seconds
>
> 2015-05-18 18:51:41,306 INFO zen.ZenModeler: Daemon ZenModeler
> shutting down
>
> We are about to improve how to detect failed modeling during deploy /
> zseed stage -
> <https://trello.com/c/TJi0AWSS/1227-zcomms-some-failed-modeling-runs-are-not-detected>
>
> Unmodeled devices are a definite sign of trouble as modeling is
> automated by the system.  If you have found unmodeled devices, please
> make sure to report them to <ctl@cascadeo.com> for bug fixing.

1.  Look at the global ZCONSOLE here:
     <http://10.128.131.47:8080/zport/dmd/itinfrastructure>  and search
    by IP for the instance(s) you are interested in studying.  This
    system collects telemetry on the production zgp instances and
    provides useful graphs etc.  Note any swapping, CPU overload,
    out-of-memory conditions, etc. for nodes under study.

2.  Record modeling status, findings, re-modeling outcomes, etc. as
    observed to \#internal-ctl Slack channel.  Be verbose and feel free
    to use screenshots rather than re-keying / cut-and-paste if that
    helps.

3.  Look at the Zenoss app on the TRAPLOG nodes.  These are also Zenoss
    app instances but they do not poll.  Instead, they listen for syslog
    and SNMP traps coming in from devices.  There is an active-standby
    pair of load balancers in front of these nodes.  The most
    significant failure mode would be a load balancing failure, such
    that incoming messages never make it to the TRAPLOG nodes.  You can
    watch the incoming event stream by clicking EVENT at the top of the
    primary Zenoss application post-login.  If you do not see new events
    coming in (note the counters on the right and the ability to sort by
    "Last Seen" at the upper right) that is definitely cause for
    concern.

4.  Record everything you've done and observed to the \#internal-ctl
    Slack channel **and send it to ctl@cascadeo.com** so that the CTL
    team has visibility in to IR.  Flag anything that requires
    follow-up, e.g. bugs / defects found, devices that were unmodeled
    but set to Production, etc. Use the DNS name of the device instead
    of the device name when writing the report for the CTL team.
    Example:\
    uc1r8rc2zgpzmaster | 10.121.186.12 | running\
    uc1r8rc2zgpztrap01 | 10.121.186.26 | running

5.  If needed, escalate to the on-call CTL engineer via page@ctl
    &lt;message&gt; (you need to do this in \#cascadeo-operations Slack
    channel ) if you are not fully convinced that the system is behaving
    normally.   Normal behavior will show uniform message volumes in
    Kibana.  When in doubt, escalate - this is a mission-critical system
    and outages result in unrecoverable data loss!

6.  If you are not getting a prompt response from the on-call CTL
    engineers, please escalate to Jared Reimer directly at  +1 (206)
    650-7090 *day or night*.   (SMS / iMessage preferred; voice if no
    response or emergency.)\
    \
    **Screenshots for Tier 2 IR follow:**\
    ![C:\\d557aed81c1ee81f78fc31842febdbe7](media/image6.tmp){width="1.3645833333333333in"
    height="2.6041666666666665in"}![C:\\0e6737738debc967276a6b51d3f466ad](media/image7.tmp){width="4.875in"
    height="1.4479166666666667in"}![C:\\b496d96daaea0f9e58f74a0c6fb23548](media/image8.tmp){width="4.416666666666667in"
    height="2.6041666666666665in"}![C:\\1499b58f08bc58e8dbdae64b3febfb42](media/image9.tmp){width="2.5104166666666665in"
    height="2.6041666666666665in"}![C:\\85efcc05e8eea0db6769bb65661e00bf](media/image10.tmp){width="1.4895833333333333in"
    height="2.03125in"}\
    ![C:\\1b18aa4299d5d70b660cc1ab0e9ef677](media/image11.tmp){width="4.875in"
    height="1.0833333333333333in"}

#### TIER 2: KIBANA INCIDENT RESPONSE RECIPES

##### Symptoms of overloaded Z-Node observed in Z-Console dashboard

The events dashboard of the Z-Console shows nodes believed to be
overloaded, as well as other errors.

![C:\\00832850283cd345643dfc38f820752a](media/image12.tmp){width="4.875in"
height="2.1666666666666665in"}

In the example above, there are three distinct problems:

-   One of the HTTP monitors is failing.  In this case, it is failing
    for VA1ZGPPROXYLB01.   Manual human investigation is required.  This
    may be a broken / failed process.  It is probably not related to
    load, but that is a possibility that can not be ruled out based on
    the example above.

-   Many of the nodes have CPU load averages higher than whatever the
    current threshold is set to.  Note the corresponding trigger and
    notification rules.  These events invoke "drain" automatically in
    response to high load.  The drain script will NOT attempt to move
    large devices like vCenter and Juniper SRX.  Placement of larger
    monitoring workloads (-vsphere, -event, -srx etc.)  must be done
    carefully.  See notes in the next section about this.

-   Many nodes have been swapping.  This means they are out of memory.
     The correct solution is to move workload away from them and force
    replacement of the nodes to clear the swap condition.  These alarms
    will persist until the nodes are replaced.

##### Symptoms of overloaded Z-Node observed in Kibana dashboard

The graphs lower in the Kibana dashboard highlight cases where Z-Nodes
are struggling under excessive workload.  Two examples of this condition
follow:

![C:\\55f762e62acae2f19651f6554e19071c](media/image13.tmp){width="4.875in"
height="1.5729166666666667in"}

In this case, NY1R82ZGPZNODE10 was consistently exhibiting a
memory-exhaustion condition.  UC1R82ZGPZNODE06 was, but less
severely/consistently.

![C:\\cd4a3b8d0151ad1aa36b2a00615b6862](media/image14.tmp){width="2.90625in"
height="2.59375in"}

Note the uneven distribution here.  The abnormally tall bars on the left
are the ones we are most interested in resolving.  This same logic also
applies to ZNODES WITH NEW ZENOSS EVENT FORWARDERLAGSEC&gt;900 and other
similar graphs showing relative workload across Z-Nodes.   It definitely
applies to any Z-Node that is swapping (out of memory) as that massively
impairs Zenoss application performance.

There are two options for reducing the workload on a Z-Node that is
showing symptoms of being overloaded:

~~1) Move workload to other Z-Nodes in the Z-Group.  This is almost
always the right thing to do.  The "drain" script (documented elsewhere)
makes it easy to move smaller workload items away from the overloaded
node.  It does not, however, attempt to move the largest work items.
 Those must be moved manually (using the Swagger API) and placed very
carefully.  ~~

~~The placement guideline is this:  **Avoid placing two or more of the
following items on a single Z-Node unless you are certain it is very
lightly loaded.**~~

~~The special case items are devices with these in their names:   ** 
-vsphere     -event    -srx-core    -srx-edge    -cfw-   -efw-**~~

~~Again, please be careful in placement of these large objects.  
Putting too many of them on a single Z-Node will cause collection
problems.  They MUST be spread across Z-Nodes.   ~~

~~*If you cannot find a suitable Z-Node, use the horizontal scale-out
recipe to add a new Z-Node to the Z-Group and place the workload
there.*~~

~~There is a script that you can use to bulk-move devices.  The script
is called \`*mover\`* and it is typically used to populate a
newly-created Z-Node after horizontal scale-out.  To run it, \`perl
/usr/local/bin/mover.l targetznode\` on the Z-Console and paste a list
of devices you want moved to that Z-Node, one per line.   This script
iterates across the list of devices and uses the Swagger API to move
them.~~

2\) Increase capacity for *all Z-Nodes in this Z-Group* to add RAM or CPU
cores.   Generally speaking, this is ONLY done where there is a single
device (usually a core SRX firewall) monitored by a node and it is still
low on memory or swapping.   To do this, use the vertical scaling recipe
published elsewhere in this runbook.  NOTE:  Check with a CTL team
member before making this determination; it should be a last resort, not
a first attempt at fixing the problem.

===

##### Site-wide outage / Uniform drop in volume across datacenters

Tier 2 can report major Analytics outages (eg Kibana is broken, all
Message Volume alarms firing at once, etc.) to
[help@ctl.io](mailto:noc@tier3.com) (cc:ctl@cascadeo.com) and they will
page the on call Analytics team member to respond.

When emailing <help@ctl.io>, it is highly suggested to use the following
format:

**Subject**: CTL Analytics / Kibana problem\
**Message**:\
          The Analytics pipeline is being managed by Ade Miller’s team
(CTL Slack channel **\#analytics**) 

-   State what is wrong e.g. message count drop site-wide from one or
    more or all datacenters 

-   State the time range where you noticed the issue (UTC highly
    recommended) 

-   Give the link of the dashboard, specify that it is only accessible
    by the ie\_team 

-   Attach screenshots, mention in the email that you are attaching
    screenshots 

-   Attach Kafka tests (refer to [HOWTO: Testing the Kafka
    Brokers](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-HOWTO:TestingtheKafkaBrokers))  

-   Attach byline (who is sending the ticket to help@ctl.io) and ZGP
    PIN  \
     \
     If you do not have access to **\#analytics** in CTL Slack, you may
    ask any CTL dev/ops member to post on your behalf.

##### Kibana 4 auto-post in Slack's \#cascade-operations room fails with a Red status

Examples:

![C:\\6338b7c2488eb3c4287b1da65a993b9e](media/image15.tmp){width="4.03125in"
height="2.6041666666666665in"}

Figure: The error log above is:
*plugin:elasticsearch \[security\_exception\] unable to authenticate
user \[kb\_cascadeo\_server\] for REST request
\[/\_cluster/health/.kibana\_cascadeo?timeout=5s\], with:
{"header":{"WWW-Authenticate":"Basic realm=\\"shield\\""}}*

*\
*![C:\\d642c65f4b6072a7c5b8495685d45e36](media/image16.tmp){width="3.2604166666666665in"
height="2.6041666666666665in"}

Figure: The error log above is: *plugin:elasticsearch *Authentication
Exception

**Triage:**

1.  Try logging in manually
    to <https://kibana-cascadeo.analytics.ctl.io/>

2.  If you still see the error, take a screenshot and see the recipe
    below how to escalate to CTL Devops and CTL \#analytics team.

##### CTL Kibana 4 Multiple Failures to Login

If the Kibana autopost in **\#cascadeo-operations** is not working, you
may do the following steps:

1.  Check if you can log in to Kibana 4 using CTL AD credentials. If
    not, proceed to Step 3.

2.  If you can log in to Kibana 4, wait for 2 cycles if the autopost
    recovers. If not, inform (Slack PM) Prem or any ctl-dev (Jerome,
    Leo, Peter, Jared, Abigail) that the account that handles the Kibana
    autopost is broken. Ask them to notify and ask in CTL's \#analytics
    room. (NO NEED TO PAGE)

3.  Email <help@ctl.io> (cc: ctl@cascadeo.com) that the AD login for
    Kibana is not working, and at least two accounts are confirmed. Ask
    Prem to verify the account used for the autopost
    (*svc\_zenoss@ctl.io* as of this writing). Don't forget to ask them
    to route it to Analytics and indicate your ZGP PIN.

Sample Email:

Hello,

Please route this to the Analytics Team c/o Ade Miller.

It appears that our AD login is not working in Kibana 4. Two accounts
are confirmed: svc\_zenoss@ctl.io and katrina.ramos. The error is 401
Unauthorized login.

Please check, thank you.

Another sample email:

Hello,

Please route this to the Analytics Team c/o Ade Miller.

We encountered a RED status with our Kibana instance
(<https://kibana-cascadeo.analytics.ctl.io/>). See attached screenshots.

Please check, thank you.

### Deadman's Snitch (DMS) alerts

We send pings from some components (CTL ELK message volume checks,
Zenoss Event Processing health check, Z-group hosts uptime, etc.) to DMS
to confirm their health script/check has been run.

#### TIER 1: SPOT CHECKS

###### Examples of alerts

-   \[MISSING\] SG1 Message Volume hasn't checked in -  SG1 is a
    datacenter

-   \[MISSING\] GLOBAL R8 ElasticSearch Message Volume hasn't checked in
    - Global R8 covers all datacenters, the alert means the script
    failed to query ElasticSearch for the message volume stats.

If you receive a MISSING email from DMS, *quickly spot check*.

After receiving ***2* SUCCESSIVE EMAILS**** (gap is \~15min between
emails) from DMS, escalate to Tier 2.

****If a bar for the concerned datacenter exists during the spot check,
it means the MESSAGE HAS CHECKED IN. If after 3 HOURS, the DMS alert
still exists but the spot check is OK, create an URGENT (non-emergency)
ticket for an engineer to check why the alert is persisting (most
probably the volume threshold has been reached).****

**SPOT CHECKS**

In this example, the datacenter is SG1:

###### SPOT CHECK: Datacenter message volume hasn’t checked in

\[MISSING\] SG1 Message Volume hasn't checked in

1.  Take note of the timestamp (also noting the TIME ZONE).

2.  Go to [Kibana Zenoss Dashboard for
    CTL](https://kibana-cascadeo.analytics.ctl.io/app/kibana#/dashboard/Zenoss-Dashboard).  [~~https://ctl-kibana.centurylinkcloud.com/\#/dashboard/elasticsearch/Zenoss%20Dashboard~~](https://ctl-kibana.centurylinkcloud.com/#/dashboard/elasticsearch/Zenoss%20Dashboard)

3.  Go to *TOTAL MESSAGE THROUGHPUT BY DC (MESSAGES PER
    INTERVAL ~~SECOND~~)* graph.

![C:\\72a950e2a55136957e13682275094118](media/image4.tmp){width="4.875in"
height="1.5729166666666667in"}![C:\\3e4c746c73bba935995675b4370c648c](media/image5.tmp){width="4.875in"
height="1.4895833333333333in"}

Check the *2nd and 3rd to the last bars* of the concerned datacenter (eg
SG1). Hover on the bar and check for the timestamp (note that equivalent
time in the previous time zone you noted).

****If a bar for the concerned datacenter exists, it means the MESSAGE
HAS CHECKED IN so you can ignore the DMS Alert.****

If the alert is global like:

###### *SPOT CHECK: Global message volume hasn’t checked in*

\[MISSING\] GLOBAL R8 ElasticSearch Message Volume hasn't checked in

It means that all of the message volume stats cannot be fetched. If you
still see the bars from the graph from all of the datacenters, it means
the DMS alert is a FALSE POSITIVE.

##### Z-group/Zenoss Node Spot Check

###### Examples of alerts

\[MISSING\] NE1 STATE Z-MASTER hasn't checked in

\[MISSING\] UC1 ZEP Z-TRAPLOG02 hasn't checked in

\[MISSING\] CA1 Z-MASTER hasn't checked in

\[MISSING\] CA1 Z-NODE03 hasn't checked in

###### Spot check overview

There are three major types of nodes that are being checked in DMS:

-   Z-MASTER

-   Z-NODE

-   Z-TRAP

Their corresponding names in Kibana are: 

-   If Z-MASTER, "&lt;Datacenter&gt;&lt;Release&gt;&lt;CTL Account
    Code&gt;ZMASTER". Example: "WA1R8RC2ZGPZMASTER". The Datacenter is
    WA1, Release is R8RC2, and CTL Account Code is ZGP.

-   If Z-NODE, "&lt;Datacenter&gt;&lt;Release&gt;&lt;CTL Account
    Code&gt;ZNODE&lt;Node Index&gt;". Example: “WA1R8RC2ZGPZNODE01” or
    “WA1R8RC2ZGPZNODE02”.  The Datacenter is WA1, Release is R8RC2, CTL
    Account Code is ZGP, and Node Index is 01 or 02.

-   If Z-TRAP, "&lt;Datacenter&gt;&lt;Release&gt;&lt;CTL Account
    Code&gt;ZTRAP&lt;Node Index&gt;". Example: “WA1R8RC2ZGPZTRAP04” or
    “WA1R8RC2ZGPZTRAP05”.  The Datacenter is WA1, Release is R8RC2, CTL
    Account Code is ZGP, and Node Index is 04 or 05.

###### Spot check example

Go to [CTL Zenoss Spot Check
Dashboard](https://kibana45-cascadeo.analytics.ctl.io/app/kibana#/dashboard/Zenoss-Host-Spot-Check)

~~Go to
<https://ctl-kibana.centurylinkcloud.com/#/dashboard/elasticsearch/Zenoss%20Host%20Spot%20Check>~~

You should see something like this:

![C:\\bd039ea13e41e922a81961538b2aa27e](media/image17.tmp){width="4.875in"
height="2.7395833333333335in"}

Edit the hostname under the search bar.

~~field *must* ~~

~~field: hostname~~

~~query: “&lt;FILL IN THE HOSTNAME HERE, SMALL/LOWERCASE CAPS&gt;”~~

~~(then click Apply)~~

Example:

If the alert is

\[MISSING\] UC1 ZEP Z-TRAPLOG02 hasn't checked in

Your query should be "hostname: uc1r8rc2zgpztrap02". This is the node
name (also known as hostname).

IMPORTANT: DO NOT SAVE THE KIBANA DASHBOARD THAT YOU JUST EDITED.

###### Thresholds for <noc@cascadeo.com>

E*scalate to engineer if there is an alert Report to responding engineer
the result of the spot check. *

~~If you see bars indicating stream of messages, it means the node is OK
(the alert is there because we are still adjusting its sensitivity). DO
NOT escalate.~~

~~If you see *none or zero bars*, it means there is no stream of
messages and it corresponds to the DMS alert, *escalate to an engineer
to check*.~~

~~*If the spot check is OK and you still see the DMS alert persisting
after 3 hours, it is time for an engineer to check why the alert is
persisting.*~~

### **TIER 1 INCIDENT RECIPES**

#### **Problem: Maximum threshold for unhealthy count. Removing node** *&lt;SOME NODE&gt;* **from service. Health: Error creating failure event.**

**Sample ticket:** <https://cascadeo.zendesk.com/agent/tickets/99584>

**Overview:** The self-healing mechanism has kicked in. When the node is
re-provisioned, it should generate DMS alerts such as Missing State /
ZEP.

**Resolution:**

1.  It should recover on its own. Wait for ****45 minutes**** for
    re-provisioning to finish. During re-provisioning, you might receive
    DMS alerts.

2.  Escalate to the CTL Team if DMS alerts related to the re-provisioned
    node do not clear after ****45 minutes****.

3.  Resolve the ticket and update / merge with related DMS Zendesk
    tickets.

#### Problem: \[CTL PROD\] &lt;SOME DEVICE&gt; Evaluation failed due to ... &lt;some message about a missing expression&gt;

Sample ticket: <https://cascadeo.zendesk.com/agent/tickets/92478>

Overview: Rooti cause is either a transform error or the error happens
during the first time modeling of the device (since the datapoints
that's included in the calculation have not values yet). 

Resolution:

1.  NOC to assign to CTL oncall engineer.

#### Problem: \[CTL PROD\] LB1-\*\*\*\* Alerts. Or any alerts from LB1 or network 10.247.7.X

Sample ticket: <https://cascadeo.zendesk.com/agent/tickets/105233>

Overview: LB1 is the CTL Lab Environment but has the same SLA similar to
ZGP (production)

Resolution:

1.  Escalate LB1 alerts as usual.

#### Problem: \[CTL PROD\] Device xxx is unmodeled/ Device xxx has not been modelled for xxx hours

Overview: 

Resolution:

1.  Assign/Merge if there is an existing ticket to Abby.

### **TIER 2 INCIDENT RECIPES**

#### Problem: Unable to use ssh\_node to access a node in Chef Workstation. 

**Validation / Information: **

Unable to access node using ssh\_node in Chef Workstation 

> \[root@VA1ZGPCHEF-W01 \~\]\# ssh\_node CA1R82ZGPZNODE04
>
> ssh-ing to 10.51.72.24...

but node is in SEEDED state.

> \[root@CA1R82ZGPPROVISIONER \~\]\# redis-cli
>
> redis 127.0.0.1:6379&gt; hget CA1R82ZGPPROVISIONER state
>
> (nil)
>
> redis 127.0.0.1:6379&gt; hget CA1R82ZGPZNODE04 state
>
> "SEEDED"

**Solution(s):**

1.Find the correct host in <https://control.ctl.io> by using the dns
information.

![C:\\d8c663b3bbbbf159c01663f5bc2909e5](media/image18.tmp){width="0.3333333333333333in"
height="0.3333333333333333in"}

2\. SSH manually in to the host and run 'chef-client' to register it.

#### Problem: \[CTL PROD\] \$HOST\_NAME: Command ModelDeviceAPI failed

**Validation / Information: ** This event is generated when auto-remodel
trigger fails. The trigger can fail if the API server fails or there is
a bug in the script that calls remodelAsync API. Verify API issue by
browsing <http://10.128.131.39:8080/docs/>. If down or flapping,
escalate the issue to Z-Cosystem API component owner
(jerome@cascadeo.com). If nothing is wrong with the API, see
zenactiond.log of Z-Console and investigate what is causing
ModelDeviceAPI to fail. Escalate to CTL ops if necessary.

**Solution(s):**

1.  **TBD**

#### **&lt;XXPROVISIONER&gt;Unable to replace un-SEEDED znode. Set force to true to force replacement**

Traceback (most recent call last):\
File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 240,
in trace*task\
R = retval = fun(\*args, \*\*kwargs)\
File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 437,
in \_\_protected\_call*\_\
return self.run(\*args, \*\*kwargs)\
File "/home/zenoss/zcomms/provisioner/provisioner.py", line 227, in
replace\_node\
raise Exception('Unable to replace un-SEEDED znode. Set force to true to
force replacement.')\
**Exception: Unable to replace un-SEEDED znode. Set force to true to
force replacement**

**Solution**

**Using sentry**

**Go to: <http://10.128.131.73:9000/sentry/zcomms/> (sample sentry
issue: <http://10.128.131.73:9000/sentry/zcomms/issues/35/>)**

-   look for the EXCEPTION *Unable to replace un-SEEDED znode. Set force
    to true to force replacement*.

-   At the right side you can see EVENTS with counts indicated

-   It will display lists of exception coming from XXPROVISIONER

-   under nodename you will see the affected node\
    \
    ![C:\\30e8c7789910445a1d8b522b86e68389](media/image19.tmp){width="4.666666666666667in"
    height="2.6041666666666665in"}

-   After identifying the affected node [continue replacing
    it](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-Problem:ForcingZ-NodeReplacement) (set
    force to True)

-   Close the Sentry issue so you can receive exceptions related to
    other z-nodes that are still problematic.

#### HOWTO: Verify CTL/Platform API Issue

**Validation / Information: ** CTL API or Platform API is used to
provision nodes in CTL Cloud. It is also used to detect orphan nodes in
zgroups and delete them. Sometimes, however, API fails due to unknown
issue. In which case, verify first if indeed there is an API issue by
following the steps below before escalating it to CTL helpdesk.

**Solution(s):**

1.  SSH in to the provisioner in question.

2.  Enter python shell: \# python

3.  In python shell, execute the code below line by line.

4.  import requests,clc,json

5.  \#Change to whatever DC you are testing

6.  DC = "au1"

7.  \#Retrieve manifest

8.  r=requests.get('http://10.128.131.220:4984/zenoss\_databag/manifest\_%s\_r82\_zgp'
    % DC.lower())

9.  manifest = r.json()

10. group = manifest\['specifications'\]\['znode'\]\['HardwareGroupID'\]

11. template = manifest\['specifications'\]\['znode'\]\['Template'\]

12. network = manifest\['specifications'\]\['znode'\]\['Network'\]

13. account = manifest\['specifications'\]\['znode'\]\['AccountAlias'\]

14. user = manifest\['z\_group'\]\['ctl-mvp'\]\['API\_USER'\]

15. passwd = manifest\['z\_group'\]\['ctl-mvp'\]\['API\_PASSWORD'\]

16. \#If you see error here, stop and check CouchBase first. The issue
    is probably not an API issue. Prem is the contact owner - in case
    you need help with troubleshooting.

17. 18. \#TEST for authentication error

19. \#Authenticate

20. clc.v2.SetCredentials(user, passwd)

21. \#If it errors here, check creds in manifest. We dont usually change
    API creds, but worth looking if there is an auth error.

22. 23. \#TEST for cleanup\_zgroup error

24. \#Get group details. Group here is the group where znodes are
    created.

25. g=clc.v2.Group(group, alias=account)

26. print g.id

27. \#If there is a problem here, cleanup\_zgroup routine will not work

28. \#like below:

29. \#&lt;html&gt;&lt;body&gt;&lt;h1&gt;503 Service
    Unavailable&lt;/h1&gt;\\nNo server is available to handle this
    request.\\n&lt;/body&gt;&lt;/html&gt;

30. \#and more

31. \#Get list of servers in a group

32. servers=g.Servers().Servers()

33. print servers

34. \#If there is a problem here, cleanup\_zgroup routine will not work.

35. \#like below:

36. \#&lt;html&gt;&lt;body&gt;&lt;h1&gt;503 Service
    Unavailable&lt;/h1&gt;\\nNo server is available to handle this
    request.\\n&lt;/body&gt;&lt;/html&gt;

37. \#and more

38. \#TEST server creation

39. \# Create new server and block until complete

40. clc.v2.Server.Create(name="TEST",cpu=1,memory=1,

41. group\_id=g.id,

42. template=template,

43. network\_id=network).WaitUntilComplete()

44. \#Watch queue in Control Portal UI. Be sure to delete the instance
    after the test.

> \#CAUTION: DO NOT run Create or Delete in rapid succession. E.g.
> inside for loop without throttling the requests

1.  If you encounter error after manifest retrieval, it is probably an
    API issue. Escalate the issue to CTL helpdesk. When creating ticket,
    DO NOT include the URLs from celery-provisioning log as they are
    truncated. This is just a logging bug in CLC Python SDK. If you
    include them, tell CTL helpdesk that the URLs are actually correct
    and that it is just a bug in logger.

      5. Perform the validation above if you see the same stack trace
below. If the event is persistent escalate create a ticket to
<help@ctl.io> . 

          u'&lt;html&gt;&lt;body&gt;&lt;h1&gt;503 Service
Unavailable&lt;/h1&gt; No server is available to handle this request.
&lt;/body&gt;&lt;/html&gt; '

   

#### **Problem: Provisioner XXXXPROVISIONER: Manual bootstrap returned with non-zero code.**

**Information:** No manual intervention is required for this alert
unless maximum provisioning retries is reached. This error occurs when
the provisioner was unable to bootstrap a znode successfully. The
provisioner will automatically try to reprovision the znode if this
error occurs. Once the maximum retries is reached (3 retries), the
provisioner will stop retrying and create alert that maximum retries
have been reached which should be addressed as outlined
in [ErrorCode:Maximumprovisioningretriesreached](#CTLZenossIncidentResponseRecipes-ErrorC).

#### 

#### Problem: \[CTL PROD\] \$HOST\_NAME: no \$GROUP directory.\$DIR does not exist.Run bin/rancid-cvs \$GROUP to make all of the needed directories

**Validation / Information: ** Event class is /App/Rancid. The alert is
generated from the Rancid backup
ZenPack. [https://docs.google.com/document/d/1tyWph2IEOMuCBimGERHLNmKVlQ8dSeD0XI73yAWphfw/edit\#](https://docs.google.com/document/d/1tyWph2IEOMuCBimGERHLNmKVlQ8dSeD0XI73yAWphfw/edit)  

**Solution(s):**

**NOTE: Check first if the source of the alert is from an active znode
that's been seeded completely. It's possible that an orphaned znode or a
newly provisioned znode not yet seeded might run rancid (CRON). If
that's the case, you can ignore the alert (if possible remove/terminate
the orphan node).**

1\. SSH in to the z-node. The zenrancid daemon should always generate the
necessary group directory. Check
/opt/zenoss/rancid/var/’directory\_name’ if it exists. If it doesn’t
exist, try to clear the /opt/zenoss/rancid/var directory contents and
run zenrancid. If for some reason it still fails to create the
directory, check the official RANCID site on how to troubleshoot it.

#### Problem: \[CTL PROD\] \$HOST\_NAME: \$GROUP/router.db file.\$DIR/router.db does not exist

 **NOTE: Check first if the source of the alert is from an active znode
that's been seeded completely. It's possible that an orphaned znode or a
newly provisioned znode not yet seeded might run rancid (CRON). If
that's the case, you can ignore the alert (if possible remove/terminate
the orphan node).**

**Validation / Information: ** Event class is /App/Rancid. The alert is
generated from the Rancid backup ZenPack. 
[https://docs.google.com/document/d/1tyWph2IEOMuCBimGERHLNmKVlQ8dSeD0XI73yAWphfw/edit\#](https://docs.google.com/document/d/1tyWph2IEOMuCBimGERHLNmKVlQ8dSeD0XI73yAWphfw/edit)

**Solution(s):**

1\. SSH in to the z-node. Check if
/opt/zenoss/rancid/var/Group\_dir/router.db exists. By default only the
group being handled by the z-node should run the RANCID backup (for that
z-node).

#### Problem: \[CTL PROD\] rancid-cvs has failed on %s 

**NOTE: Check first if the source of the alert is from an active znode
that's been seeded completely. It's possible that an orphaned znode or a
newly provisioned znode not yet seeded might run rancid (CRON). If
that's the case, you can ignore the alert (if possible remove/terminate
the orphan node).**

**Validation / Information: ** Event class is /App/Rancid. The alert is
generated from the Rancid backup ZenPack. 
[https://docs.google.com/document/d/1tyWph2IEOMuCBimGERHLNmKVlQ8dSeD0XI73yAWphfw/edit\#](https://docs.google.com/document/d/1tyWph2IEOMuCBimGERHLNmKVlQ8dSeD0XI73yAWphfw/edit)

**Solution(s):**

1\. SSH in to the z-node. Since we’re using Github for the backup, the
process includes clearing the /opt/zenoss/rancid/var directory and then
preparing / initiating it for the remote Github repository. This is
important to prevent Github sync issues. If there are issues, try to run
zenrancid run -v10 (debug mode) and check /opt/zenoss/log/rancidd.log

#### Problem: \[CTL PROD\] The following routers have not been successfully contacted for: \$msgtxt" \$HOST\_NAME: config fetcher problems - \$GROUP

**NOTE: Check first if the source of the alert is from an active znode
that's been seeded completely. It's possible that an orphaned znode or a
newly provisioned znode not yet seeded might run rancid (CRON). If
that's the case, you can ignore the alert (if possible remove/terminate
the orphan node).**

**Validation / Information: ** Event class is /App/Rancid. The alert is
generated from the Rancid backup ZenPack. 
[https://docs.google.com/document/d/1tyWph2IEOMuCBimGERHLNmKVlQ8dSeD0XI73yAWphfw/edit\#](https://docs.google.com/document/d/1tyWph2IEOMuCBimGERHLNmKVlQ8dSeD0XI73yAWphfw/edit)

**Solution(s):**

1\. This is generated if a router/device included in the backup can’t be
reached or inaccessible by RANCID. These alerts are still under
observation. Please merge to an existing ticket and assign to Leo
Bustamante.

#### **Problem: Z-GROUP Safe Mode**

**Validation / Information: **A very important emergency stabilization
measure.  This recipe disables all non-essential functionality and
zcomms (Command and Control infrastructure).  Each Z-Node is then a
stand-alone Zenoss instance operating autonomously.   This recipe is
ONLY used when you have followed standard recipes and cannot get the
system into a stable state.  It is most likely to be used in response to
nodes not being replaced / seeded, e.g. the Provisioner / zseed / zcomms
functionality is broken, or Provisioner frequently or continuously
replaces multiple z-nodes in a datacenter.

**Solution(s):**

1.Use [control.ctl.io](http://control.ctl.io) to stop (power off) the
RabbitMQ and Provisioner nodes for the Z-Group in question.  This will
freeze the Z-Nodes in their current configuration and prevent
re-provisioning, self-healing, new configurations from propagating, etc.
 

2\. SSH in to Z-Master and stop supervisor to avoid Provisioner timeout
alerts.

> \# service supervisor stop\
> \# chkconfig supervisor off   \#if node is expected to reboot

3. SSH in to all z-nodes and stop supervisor to avoid heartbeat queue
from backing up.

> \# service supervisor stop\
> \# chkconfig supervisor off   \#if node is expected to reboot

4. Operate Zenoss application locally on each Z-Node as you would any
other Zenoss deployment, but be aware that any configuration changes
made locally will be overwritten by the next zseed run.

5. If Z-Nodes are unseeded, manually enable monitoring by setting
devices to Production state. Mapping of devices to z-nodes can be found
at the manifest.'

6. Make sure the component owner is aware that the Z-Group is in an
impaired status.   The system should not be left in this state for a
long period of time.

7. Monitor Z-Group very carefully as there is no redundancy or
self-healing in “Safe Mode.”

> **\
> Verification: **

#### **Problem: Horizontal Scaling of Worker Z-Nodes or Z-Trap**

**Validation / Information: **This covers the steps in increasing the
number of Z-Nodes or increasing node capacity to accommodate higher
workload.   Horizontal scaling is done when a node becomes overwhelmed
or additional capacity is needed for increased workloads coming soon.
  Vertical scaling is done when a node has too little RAM or too few CPU
cores to handle its current workload.  In general, vertical scaling tops
out at 32GB of RAM and rebalancing work across multiple Z-Nodes
(horizontal scale-out) becomes preferable at that point.  If you are
unsure, please contact a CTL team member for guidance.

 **Solution(s):**

1. Login to <https://deadmanssnitch.com/> and create THREE new snitches
for the new nodes you are adding (e.g. CA1 ZEP Z-NODE03, CA1 Z-NODE03,
CA1 STATE Z-NODE03). Copy config, interval and tags from other similar
snitches already configured in the DMS web GUI.  An example is here:
 <https://deadmanssnitch.com/snitches/c127f3d5f3>

2. In the Chef Workstation node (VA1), ensure that the new node/client
name does not exist in Chef Server by deleting it.  You can find the IP
of the Chef Workstation in the VA1 inventory in
[control.ctl.io](http://control.ctl.io).  The root SSH key is the
standard ctlroot.pem

\# knife node delete &lt;nodename e.g. VA1R8D13STG1ZNODE04&gt;\
\# knife client delete &lt;nodename&gt;

3. Still in chef workstation, create client and generate client key.

export EDITOR=vi\
knife client create &lt;newnodename\_from\_step\_1\_above&gt;

  \# knife client create &lt;newnodename\_from\_step\_1\_above&gt;

>  Created client\[VA1R8D13STG1ZNODE04\]\
> -----BEGIN RSA PRIVATE KEY-----\
> MIIEowIBAAKCAQEAtptI82pBKO7smgSF2sJ6YpqUjFSKVKAL7xRfFfrceOqJ3ylZa\
> ........\
> 413jcab4/+cgYf0+UJJJ3lMEDEDXSNEVqU6SWQ0wsiFPmvVAmR4h
>
> -----END RSA PRIVATE KEY-----

4. Copy the key into the provisioner as

/etc/provisioner/keys/&lt;newnodename\_from\_step\_1\_above&gt;.pem 

5\. To learn about Couchbase Sync Gateway, please
read <https://docs.google.com/presentation/d/1JjyovfWh-3CrbxURIzPgk0ySEKkvnVPxH6OY1hnhEAw/edit#slide=id.g15fd513547_1_0>.
You have to install Postman and import postman collection as shown in
Slide 7 of the document. To get and update Couchbase Sync Gateway, read
slides 8 to 10. Authentication will be provided by Prem.

> a\. On the Postman, you have to GET and copy the latest version of the
> manifest for the datacenter. 
>
> b\. Then PUT or paste the latest version of the manifest to add a new
> z-node under the "z\_group\_nodes" and "mapping" section. Fill in the
> snitch IDs from the previous step and populate the mapping with the
> devices to be monitored by the new z-node:
>
> Note: Production z-node naming convention:
> &lt;DC&gt;R82ZGPZNODE&lt;Number&gt;, e.g. GB1R82ZGPZNODE09 /
> corresponding manifest ID:  manifest\_&lt;DC&gt;\_r82\_zgp,
> e.g. manifest\_uc1\_r82\_zgp. For Z-Trap nodes, its mapping entry
> should be empty e.g. "VA1R82ZGPZTRAP03": \[\] 

-   GET
    \# http://10.128.131.220:4984/zenoss\_databag/manifest\_uc1\_r82\_zgp

-   Click SEND and Copy to clipboard.

<!-- -->

-   PUT
    \# http://10.128.131.220:4984/zenoss\_databag/manifest\_uc1\_r82\_zgp

-   Empty the Body and paste the latest version of the manifest and
    update with the new z-node.

  ...example follows…

> "z\_group\_nodes": {\
> ...\
>    "UC1R82ZGPZNODE18": {\
>      "z\_role": "znode",\
>      "z\_group": "ctl-mvp",\
>      "snitch\_id": "CHANGE\_ME",\
>      "zep\_snitch\_id": "CHANGE\_ME",\
>      "state\_snitch\_id": "CHANGE\_ME"\
>    },\
> ...\
> "mapping": {\
> ...\
>  "UC1R82ZGPZNODE18": {\
>  },\
>  "UC1R82ZGPZNODE17": {
>
>          "10.124.11.43": {
>
>                 "attributes": {
>
>                     "collector": "localhost",
>
>                     "groupPaths": \[\],
>
>           ......
>
>  },\
>  … 
>
> c\. Click SEND and confirm the revision has been updated:

{

  "id": "manifest\_uc1\_r82\_zgp",

  "ok": true,

  "rev": "3134-2a533bbff5e4c5aae669c52e229e0849"

}

d\.  Skip this step if you are creating a Z-Trap. On the Z-Controller,
run the zb\_commit script to update the backup version. The http
authorization code can be found in Postman under [Header
tab](https://docs.google.com/presentation/d/1JjyovfWh-3CrbxURIzPgk0ySEKkvnVPxH6OY1hnhEAw/edit#slide=id.g16040e73f9_0_0).

\# cd /home/zenoss/zcomms/messaging && env PYTHONPATH=/home/zenoss
python helpers/zb\_commit.py --zb-commit -a &lt;auth&gt; -r
manifest\_uc1\_r82\_zgp

> d\. Back to the postman, GET a new copy of the latest version of manifest
> with the updated zb\_version.

-   GET
    \# http://10.128.131.220:4984/zenoss\_databag/manifest\_uc1\_r82\_zgp

-   Click SEND and Copy to clipboard.

> e\. PUT or paste the latest version of the manifest and increment the
> mapping version of the manifest (e.g. "version": 2016021800) and
> reupload the manifest. Click SEND and confirm the revision has been
> updated.

6\. Skip this step if you are creating a Z-Node. SSH to the currently
existing Z-Trap nodes in the datacenter and stop the zentrap and
zensyslog daemons. You will need to edit the monit so that the daemons
do not auto start after you stop them manually. 

\# vim /etc/monit.d/zenoss.conf

comment out the configuration for zensyslog and zentrap by adding a '\#'
at the beginning of each line. 

...

\#check process zentrap matching "zentrap"\
\#start program = "/etc/init.d/zendaemonctl.sh start zentrap" with
timeout 90 seconds\
\#stop program = "/etc/init.d/zendaemonctl.sh stop zentrap" with timeout
90 seconds\
\#if does not exist then restart\
\#if totalmem &gt; 33% for 2 cycles then restart\
\#if 3 restarts within 10 cycles then alert

...

 

\#check process zensyslog matching "zensyslog"\
\#start program = "/etc/init.d/zendaemonctl.sh start zensyslog" with
timeout 90 seconds\
\#stop program = "/etc/init.d/zendaemonctl.sh stop zensyslog" with
timeout 90 seconds\
\#if does not exist then restart\
\#if totalmem &gt; 33% for 2 cycles then restart\
\#if 3 restarts within 10 cycles then alert

...

\# /etc/init.d/monit reload

stop the zensyslog and zentrap daemon

\#su zenoss

\#zentrap stop

\#zensyslog stop

7. Skip this step if you are creating a Z-Trap. Run *chef-client -o
'recipe\[z-controller::setup-zseed\]'* in the Provisioner to generate
the dispatcher script for the new node.  You can find the IP of the
Provisioner by inspecting the Z-Group in
[control.ctl.io](http://control.ctl.io) or by looking in the Z-Console. 

8. The provisioner should be able to pick up the change in manifest and
start provisioning the z-node. Wait for the z-node to be seeded and
verify the devices in Zenoss. Monitor the progress on the provisioner:

\# tail -f /var/log/celery/celery-heartbeat.log\
\# tail -f /var/log/celery/celery-provisioning.log

\# tail -n 100 /var/log/celery/celery-seeding.log

9\. Skip this if you are creating a Z-Node. Once the new Z-Trap has been
seeded successfully, uncomment the lines you edited in step 6 in the
/etc/monit.d/zenoss.conf file. And, reload the monit daemon. This should
automatically run all the zenoss daemons.

\# vim /etc/monit.d/zenoss.config

\# /etc/init.d/monit reload

...

check process zentrap matching "zentrap"\
start program = "/etc/init.d/zendaemonctl.sh start zentrap" with timeout
90 seconds\
stop program = "/etc/init.d/zendaemonctl.sh stop zentrap" with timeout
90 seconds\
if does not exist then restart\
if totalmem &gt; 33% for 2 cycles then restart\
if 3 restarts within 10 cycles then alert

...

check process zensyslog matching "zensyslog"\
start program = "/etc/init.d/zendaemonctl.sh start zensyslog" with
timeout 90 seconds\
stop program = "/etc/init.d/zendaemonctl.sh stop zensyslog" with timeout
90 seconds\
if does not exist then restart\
if totalmem &gt; 33% for 2 cycles then restart\
if 3 restarts within 10 cycles then alert

...

verify if all the zenoss daemons should be running

\# su zenoss

\# zenoss status

**Verification: -**

#### **Problem: \[GLOBAL Z-CONSOLE\] localhost localhost zenperfdataforwarder heartbeat failure**

**Validation:** This is a standard zenoss event when a registered zenoss
daemon is not running or not working properly.

**Solution(s):**

1.  SSH in to the Z-Console (10.128.131.100). Check whether
    zenperfdataforwarder is running on z-console. 

    1.  ps -ef | grep zenperfdataforwarder

2.  If not, start zenperfdataforwarder.

    1.  su - zenoss

    2.  zenperfdataforwarder start

3.  If daemon is running, stop the currently running zenperfdataforwader
    daemon and restart it.

    1.  zenperfdataforwarder stop

    2.  make sure no zenperfdataforwarder process is running. use kill
        command if necessary. (hint: kill -9 &lt;pid&gt; if its
        stubborn)

    3.  zenperfdataforwarder start

 

#### Problem: \[MISSING\] GLOBAL R8 Z-cosystem Inventory and Config Backup

**Solution: **

SSH to the ZConsole (10.128.131.100) and check the cron
zenoss-backup-zcontroller

    \[root@VA1ZGPZCONSOL02 cron.d\]\# cat zenoss-backup-zcontroller\
0 **\*/1 \*** \* \* root
m=\`/usr/local/sbin/backup\_zenoss\_prod.sh\` && curl -o /dev/null
--silent -d "m=\$m" <https://nosnch.in/3bba01c30e>

Attempt to run the script and see if there are any issues. 

 

 

#### HOWTO : Launch / Restore Z-Console

 

1.  Launch a new server in VA1 from the latest Zenoss GMBI.

2.  From the workstation, bootstrap the node.

> knife bootstrap --no-host-key-verify -N VA1R82ZGPZCONSOLE02  -r
> "role\[z-console\]" -j '{"CTL\_MANIFEST\_DATABAG": "zenoss",
> "CTL\_MANIFEST\_ITEM": "manifest\_va1\_r8rc2\_zgp"}' &lt; ip\_address
> &gt; 

1.  SSH to the new z-console and disable cron service.

> /etc/init.d/crond stop
>
> chkconfig crond off

1.  Disable Zenoss notifications from UI.

2.  Verify.

3.  Enable cron service and Zenoss notifications.

4.  Cut-over by assigning VIP.

 

#### HOWTO :  Get Zenoss zProperties using zendmd

 

1.  SSH to the Zcontroller (IP address and credentials in
    <https://control.ctl.io/>)

2.  Execute zendmd as zenoss user:

            \# su - zenoss

> \$ zendmd
>
> &gt;&gt;&gt; d = dmd.Devices.findDevice('device\_name')  \#Set this to
> your devices name
>
> &gt;&gt;&gt; for prop\_id in d.zenPropertyIds():\
> ...        value = d.getProperty(prop\_id)\
> ...        print "{0} - {1}".format(prop\_id, value)
>
> Example Output:
>
> zAggregatorCollectionInterval - 300
>
> zCiscoMonIgnoreNotPresent - True
>
> zCiscoMonTemperatureFactor - 0.9
>
> .\
> .\
> .
>
> zVSpherePassword - cedr8wuVacEbrucu6raPHa5w
>
> zVSpherePort - 443
>
> zVSphereTransport - HTTPS
>
> zVSphereUsername - t3n\\svc\_zenoss

*The recipe below has been deprecated.*

#### ~~HOWTO : Reduce the workload on a running Z-Node by rebalancing ~~

1.  ~~Determine which Z-Node you want to move monitoring workload away
    from.  The load will be randomly reassigned to other Z-Nodes in the
    same Z-Group.~~

2.  ~~ssh in to the Z-Console as root ~~

3.  drain GB1R82ZGPZNODE99         &lt;---- put the name of the Z-Node
    here

    1.  ~~observe output and hit CTRL+C to abort if things go sideways~~

    2.  ~~repeat step 3 as needed as some transient API failures are
        common~~

    3.  ~~note that some devices are exempt: -vsphere and -event
        devices, Juniper SRX devices, etc.  This is because it is unsafe
        to move their workload to other nodes randomly; they must be
        placed by humans because of their immense workload.  ~~

    4.  you will know that you are done when no more workload can be
        moved away from the node, e.g. running the drain.l script has no
        real effect.

***~~Alternatively, use the mover script to move specific devices:~~***

1.  ~~Example: ~~\
    ~~Move il1-srx-core in IL1 NODE07 to IL1 NODE06 since NODE06 has the
    fewer number of count message and is not overloaded.~~\
    \
    ~~\[root@VA1ZGPZCONSOL16 \~\]\# perl /usr/local/bin/mover.l
    il1r82zgpznode06~~\
    ~~Paste a list of devices to move to il1r82zgpznode06 in IL1~~\
    ~~il1-srx-core~~

#### **PROBLEM: \[MISSING\] Global R8 OOM KILLER INVOCATIONS hasn't checked in**

 

**Causes:**

1.  This snitch will not be pinged if there is at least one Z-node with
    its Out-Of-Memory (OOM) killer activated

 **Objective:** Pinpoint the issue / process that caused OOM killer to
be activated.

Solution:

1.  See the panel "ZNODES WITH OOM KILLER INVOCATIONS" in
    <https://kibana-cascadeo.analytics.ctl.io/app/kibana#/dashboard/Z-NODE-CANARIES> to
    identify the Z-nodes with its Out-Of-Memory (OOM) killer activated.

> Example: 
>
> ![C:\\9fac228bf72d5da38df95c594dc520ee](media/image20.tmp){width="4.875in"
> height="0.8229166666666666in"}

1.  ~~Identify the process which was killed by the OOM. You can use this
    search as a
    base <https://kibana-cascadeo.analytics.ctl.io/app/kibana#/discover/syslog-search-killed-proc>~~

> ~~Replace the following.~~

1.  ~~time range (1 hour or the range when the OOM killer was
    activated)~~

2.  ~~hostname~~

<!-- -->

1.  ~~The line from syslog can look like the following.~~\
    ~~\
    Example: This line shows it is Zope (Zenoss Web UI) that is
    killed.~~\
    \
    *~~Jul 29 10:37:59 CA1ZGPZNODE585 kernel: Out of memory:
    Kill process 10572 (runzope) score 47 or sacrifice child~~*\
    \
    ~~Example: This line shows that it is some python process that is
    killed. See the next step how to get more hints which specific
    python process.~~\
    *~~\
    May  8 17:12:26 UC1ZGPZNODE656 kernel: Out of memory: Kill process
    13157 (python) score 469 or sacrifice child\
    ~~*

2.  ~~Use this search as the
    base <https://kibana-cascadeo.analytics.ctl.io/app/kibana#/discover/syslog-search-killed-proc2>~~

> ~~Replace the following.~~

1.  ~~time range (Absolute): ~~

    1.  ~~use the header.indexTimestamp of the line with the *Kill
        process (Python)* as the starting point (From:)~~

    2.  ~~as the end point (To:), add 1-2 minutes~~

> ~~\
> ~~Scan the result ~~and look for monit lines that start a process that
> is missing. Example: this hint shows that it was *zensyslog* that was
> killed.~~
>
> *~~Jul 29 03:15:04 WA1ZGPZNODE580 monit\[8879\]: 'zensyslog' start:
> /etc/init.d/zendaemonctl.sh~~*\
> *~~Jul 29 03:15:04 WA1ZGPZNODE580 monit\[8879\]: 'zensyslog' trying to
> restart~~*\
> *~~Jul 29 03:15:04 WA1ZGPZNODE580 monit\[8879\]: 'zensyslog' process
> is not running~~*

1.  ~~Create a Trello card under "Production Ops Issues" column with the
    list of Z-nodes that are out of memory along with which process was
    killed.~~\
    \
    ~~Note: This script is in Z-Console's cron
    zconsole-monitor-oom-killer-invocations. The owner is Prem.~~

2.  ~~T1 can pause this snitch but create a recurring note to have T2
    check every day if there are new Z-nodes added to the panel (T1 can
    remove the note if the snitch is healthy again)~~

3.  The following are the possible actions to clear the event:

-   If you see the z-node or z-master appearing in the graphs
    > consistently (OOM count is 3 or higher), [increase RAM
    > allocation](https://goo.gl/so2ryW) by increments of +4GB in the
    > manifest and Control Dashboard.

-   Please take note that you can increase the znode memory up to 45GB
    > only. Else replace the z-node and create a trello card and
    > assigned to Peter or Jerome to deep dive the devices on the
    > z-node.

-   [~~Horizontal
    > Scaling~~](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-Problem:HorizontalScalingofWorkerZ-NodesorZ-Trap)

-   [~~Move workload to other Z-Nodes in the
    > Z-Group~~](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-HOWTO:ReducetheworkloadonarunningZ-Nodebyrebalancing)

 

####   **HOWTO: Modify the Memory of a CTL Z-group Provisioner/node/master**

Increase specs using [zen.mon.ctl.io](http://zen.mon.ctl.io)

**Step 1**:

This one gets the spec of the z-node/z-master

<https://zen.mon.ctl.io/docs/#!/Node/getSpecification>

![C:\\82e162f11d68b3eb7ffb562b91d46a1f](media/image21.tmp){width="4.875in"
height="0.19791666666666666in"}

example:

<https://zen.mon.ctl.io/api/node/WA1/WA1R82ZGPZMASTER/getSpecification>

{\
"AccountAlias": "ZGP",\
"Alias": "MASTR",\
"Cpu": 4,\
"Description": "zmaster",\
"HardwareGroupID": "3caa6af9b97d4efc9924b1f34f7d0df9",\
"LocationAlias": "WA1",\
"MemoryGB": 22,\
"Network": "6d9d53c3956340bb9c0acd9f8d39fef9",\
"Password": "0eNkXgHyLnN59Y91",\
"PrimaryDns": "192.168.64.19",\
"SecondaryDns": "8.8.8.8",\
"ServerType": 1,\
"ServiceLevel": 2,\
"Template": "WA1ZGPGMBI10"\
}

**Step 2**:

Copy paste it into in the param \`specification\` then set \`dc\`,
\`name\` and 'MemoryGB'

![C:\\1c113c892b924584411e60b29154210f](media/image22.tmp){width="4.875in"
height="0.20833333333333334in"}

![C:\\e10240ed7adfd80c13ebd2a200701a82](media/image23.tmp){width="4.875in"
height="2.375in"}

if successful

{\
"id": "manifest\_wa1\_r82\_zgp",\
"ok": true,\
"rev": "14295-ae0c736f8ae1e141ce9d3899ff886d81"\
}

**Step 3**:

Log-in to Control Portal Dashboard
( [https://control.ctl.io](https://control.ctl.io/) ) and Navigate to
the Z-Node/Z-Master, and notice the percentage circle ( CPU and Memory
).  Point the mouse cursor to the percentage circle of “Memory” and an
“Edit” button will be visible. Click “Edit” to modify the memory of the
provisioner. Then, click ” Apply” and it will automatically reboot the
instance

![C:\\48677303b9318cb1175a6fb10862ae8f](media/image24.tmp){width="4.875in"
height="1.3541666666666667in"}

The Manifest of the Z-Group Provisioner should also be modified via
Postman. In manifest\_uc1\_r8rc2\_zgp:

>    "provisioner": {
>
>      "SecondaryDns": "8.8.8.8",
>
>      "Description": "provisioner",
>
>      "LocationAlias": "UC1",
>
>      "AccountAlias": "ZGP",
>
>      "ServerType": 1,
>
>      "HardwareGroupID": "3bbdea55f31a433baf2622ef102bab89",
>
>      "ServiceLevel": 2,
>
>      "Alias": "PROVR",
>
>      "MemoryGB": 4,
>
>      "PrimaryDns": "10.124.15.19",
>
>      "Template": "CENTOS-6-64-TEMPLATE",
>
>      "Password": "0eNkXgHyLnN59Y91",
>
>      "Cpu": 2,
>
>      "Network": "5b1fc32cb4fc4d149f4367a9b29e285b"
>
>    }

#### Problem: Global R8 OOM Killer Invocations Snitch Missing Due To Provisioner OOM

**Validation**: /var/log/messages in the Provisioner will indicate that
the killed process is celery.

**Solution**:

1.  SSH to Chef Workstation and increase the memory of the provisioner
    in the manifest such that it is equal to VA1 provisioner. For
    example, we will be increasing the memory of CA2 Provisioner.\
    Note: Always update git before modifying anything in the manifest
    and push changes to git afterwards.\
      \
    \[root@VA1ZGPCHEF-W01 \~\]\# cd
    /root/zenoss-cookbooks/data\_bags/zenoss/\
    \[root@VA1ZGPCHEF-W01 zenoss\]\# knife data bag show zenoss
    manifest\_ca2\_r82\_zgp -Fjson &gt; manifest\_ca2\_r82\_zgp.json\
    \[root@VA1ZGPCHEF-W01 zenoss\]\# vi manifest\_ca2\_r82\_zgp.json\
    ...........\
    \[root@VA1ZGPCHEF-W01 zenoss\]\# knife data bag from file zenoss
    manifest\_ca2\_r82\_zgp.json

2.  Log in to the Control Portal Dashboard and perform step 2 of [HOWTO:
    Modify the Memory of a CTL Z-Group
    Provisioner](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-HOWTO:ModifytheMemoryofaCTLZ-groupProvisioner)
    such that it is consistent with the manifest change.

**Verification**: After the changes are applied, the provisioner will
restart on its own and the services will be auto-started. In addition,
the OOM snitch will eventually report back.

 

#### HOWTO : Disable / Enable Chaos Monkey

1.   Go to the API - http://10.128.131.39:8080/docs/

2.  Select Chaos - enable or disable

3.  Send

#### HOWTO : Add vCenters for monitoring

There are 3 devices that needs to be added in order to monitor a
vCenter. Each of which should be added manually and outside the API.
This is because they share the same IP address and some Zenoss daemons
does not permit adding devices with an existing IP address in inventory.
The following manual steps need to be done as a workaround.

1.  Add the following devices on the z-controller: &lt;device&gt;,
    &lt;device&gt;-event, &lt;device&gt;-vsphere. Make sure to set the
    Production State to "Decommissioned" and untick Model Device.\
    e.g.

    -   wa1-vc-m01.t3n.dom under /Server/Microsoft/Windows/vSphere

    -   wa1-vc-m01.t3n.dom-event under /vSphere/APIEvent

    -   wa1-vc-m01.t3n.dom-vsphere under /vSphere

> ![C:\\a0abd4797da1549c4efe27b991d1b136](media/image25.tmp){width="4.875in"
> height="1.3854166666666667in"}

1.   Select each of the device and Reset/Change the IP address. It
    should allow you to assign the same IP address for all 3 devices.
    Also edit the Location on the same window and assign appropriately
    e.g. /WA1.\
    \
    ![C:\\0b5cb8fa55b9e3832de4a5b40d33de6a](media/image26.tmp){width="3.125in"
    height="5.135416666666667in"}

2.  Add the devices to the manifest manually via Postman with the
    following attributes. Check the znode graphs on the z-console to
    select which is the least loaded in the group. They may reside on
    the same znode.

> **Code to insert**
>
> "WA1R82ZGPZNODE05": {
>
> "wa1-vc-m01.t3n.dom": {
>
> "attributes": {
>
> "locationPath": "/Locations/WA1",
>
> "manageIp": "10.88.10.241"
>
> },
>
> "check\_dp\_start": false,
>
> "description": "wa1-vc-m01.t3n.dom",
>
> "device\_class": "/Server/Microsoft/Windows/vSphere",
>
> "name": "wa1-vc-m01.t3n.dom",
>
> "previous\_name": "wa1-vc-m01.t3n.dom",
>
> "productionState": 1000
>
> },
>
> "wa1-vc-m01.t3n.dom-vsphere": {
>
> "attributes": {
>
> "locationPath": "/Locations/WA1",
>
> "manageIp": "10.88.10.241"
>
> },
>
> "check\_dp\_start": false,
>
> "description": "wa1-vc-m01.t3n.dom-vsphere",
>
> "device\_class": "/vSphere",
>
> "name": "wa1-vc-m01.t3n.dom-vsphere",
>
> "previous\_name": "wa1-vc-m01.t3n.dom-vsphere",
>
> "productionState": 1000
>
> },
>
> "wa1-vc-m01.t3n.dom-event": {
>
> "attributes": {
>
> "locationPath": "/Locations/WA1",
>
> "manageIp": "10.88.10.241"
>
> },
>
> "check\_dp\_start": false,
>
> "description": "wa1-vc-m01.t3n.dom-event",
>
> "device\_class": "/vSphere/APIEvent",
>
> "name": "wa1-vc-m01.t3n.dom-event",
>
> "previous\_name": "wa1-vc-m01.t3n.dom-event",
>
> "productionState": 1000
>
> },

1.  Run config push against the z-group. See the runbook.

2.  Spot check the vSphere and Windows graphs.

#### 

#### Problem: Z-node appears to be stuck in SEEDING state

Stuck is defined more than *30 minutes of waiting*.

**How the seeding looks like in
PROVISIONER:/var/log/celery/celery-seeding.log**

*Notice the task ID is *04c0f592-2175-40f7-ad87-bb14c38f5e34*.*

\[2016-10-19 13:08:42,539: INFO/MainProcess\] Received task:
zcomms.provisioner.provisioner.dispatch\_znode\[04c0f592-2175-40f7-ad87-bb14c38f5e34\]

\[2016-10-19 13:08:43,377: WARNING/Worker-1\] Seeding CA2R82ZGPZTRAP02

\[2016-10-19 13:08:43,377: WARNING/Worker-1\] Skipping zmaster in
seeding CA2R82ZGPZTRAP02

\[2016-10-19 13:08:43,377: INFO/Worker-1\]
zcomms.provisioner.provisioner.dispatch\_znode\[04c0f592-2175-40f7-ad87-bb14c38f5e34\]:
In CA2R82ZGPZTRAP02: Running znode\_stop\_monitor.

\[2016-10-19 13:13:19,752: INFO/Worker-1\]
zcomms.provisioner.provisioner.dispatch\_znode\[04c0f592-2175-40f7-ad87-bb14c38f5e34\]:
In CA2R82ZGPZTRAP02: Done znode\_handoff\_monitor.

\[2016-10-19 13:13:19,753: WARNING/Worker-1\] Done seeding
CA2R82ZGPZTRAP02.

\[2016-10-19 13:13:20,283: INFO/MainProcess\] Task
zcomms.provisioner.provisioner.dispatch\_znode\[04c0f592-2175-40f7-ad87-bb14c38f5e34\]
succeeded in 277.742009245s: None

If you are not seeing this flow after 30 minutes of waiting, you can try
to reseed
(<https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-Problem:(HOWTORE-SEED)SEEDING_STATE_TIMEOUTErrorduringseeding>).

#### **Problem: (HOW TO RE-SEED) SEEDING\_STATE\_TIMEOUT Error during seeding**

Keywords: reseed, re-seed, force-reseed, force reseed, force\_reseed

**Validation: ** CTL \#zenoss Slack channel will indicate if there's a
Seeding timeout. Additionally DMS will fire the following alert:
"\[MISSING\] State &lt;znode name&gt; hasn't checked in"

**BIG NOTE**: You ****CANNOT FORCE RESEED**** if the znode is not fully
provisioned. A fully provisioned znode will have many fields in its
state table. If you force it, the entire z-group will be stuck and you
will notice that none of the z-nodes will be SEEDING or proceed to
SEEDING\_QUEUED. See examples below.

> **Example 1:  A z-node that was forced to be re-seeded but it not yet
> really provisioned:**

redis 127.0.0.1:6379&gt; hgetall GB3R82ZGPZNODE14

1\) "state"

2\) "PROVISIONED"

3\) "force\_reseed"

4\) "YES"

> **Example 2: A z-node that is fully provisioned:**

redis 127.0.0.1:6379&gt; hgetall GB3R82ZGPZNODE14

1\) "state"

2\) "PROVISIONED"

3\) "force\_reseed"

4\) "YES"

redis 127.0.0.1:6379&gt; hgetall GB3R82ZGPZTRAP01

1\) "state"

2\) "PROVISIONED"

3\) "state\_time"

4\) "1479232390.737859"

5\) "status"

6\) "active"

7\) "internal\_ipaddr"

8\) "10.105.99.160"

9\) "powerState"

10\) "started"

11\) "description"

12\) "znode"

13\) "id"

14\) "gb3zgpznode1961"

15\) "locationId"

16\) "GB3"

17\) "created\_date"

18\) "1479224663"

19\) "osType"

20\) "CentOS 6 64-bit"

21\) "groupId"

22\) "5bcca394486d44d0abb446ca75940e45"

23\) "name"

24\) "GB3ZGPZNODE1961"

25\) "role"

26\) "znode"

27\) "account\_id"

28\) "zgp"

29\) "server\_id"

30\) "GB3ZGPZNODE1961"

31\) "zboutput\_ver"

32\) "0"

33\) "mem\_free"

34\) "4626558976"

35\) "heartbeat\_time"

36\) "1479232566.606348"

37\) "last\_model\_time"

38\) "{}"

39\) "node\_id"

40\) "GB3R82ZGPZTRAP01"

41\) "health"

42\) "OK"

43\) "cpu"

44\) "8.8000000000000007"

45\) "inventory\_ver"

46\) "2016110800"

**Solution(s):**

1.  **On the provisioner, check the status of the node with the
    issue:**\
    \
    \#redis-cli\
    redis 127.0.0.1:6379&gt; hget VA1R8RC1ZGPZNODE01 state

2.  If the seeding has timed out, the state should be: "SEEDING" or
    "SEEDING\_FAILED"

3.  Check the following log files, to verify if the znode seeding has
    indeed timed out as well as any errors (exceptions) that might
    related to it:\
    \
    /var/log/celery/celery-heartbeat.log\
    /var/log/celery/celery-provisioning.log\
    /var/log/celery/celery-seeding.log\
    \
    In the z-node: /var/log/celery/celery-messaging.log

4.  If it has indeed timed out, reset the seeding process for the
    z-node:

> **BIG NOTE: Check the state of the z-node. If it is SEEDING or
> SEEDING\_FAILED, reset it to PROVISIONED before performing the steps
> below.**\
> \
> \[IN PROVISIONER \~\]\# redis-cli hset &lt;NODE-NAME&gt; state
> PROVISIONED\
> \
> \[IN PROVISIONER \~\]\# redis-cli hset &lt;NODE-NAME&gt; force\_reseed
> YES
>
> *force\_reseed in STATEDB possible values: YES | NO*
>
> Example:\
> \
> \[root@VA1R82ZGPPROVISIONER \~\]\# redis-cli
> hset VA1R8RC1ZGPZNODE01 force\_reseed YES
>
> **We have noticed instances after doing above, the node state
> transitions from PROVISIONED to SEEDING\_QUEUED (making all z-nodes,
> including zmaster in SEEDING\_QUEUED). If you notice this, you can try
> restarting *celery-seeding-znode* celery process in the provisioner,
> then redoing step 4.**
>
> Example:
>
> root@CA3R82ZGPPROVISIONER \~\]\# supervisorctl restart
> celery-seeding-znode\
> celery-seeding-znode: stopped\
> celery-seeding-znode: started

1.  Monitor the log files (particularly
    /var/log/celery/celery-heartbeat.log) if the seeding process will be
    completed. Please note that log errors might appear (particularly on
    /var/log/celery/celery-provisioning.log, /var/log/celery/celery-seeding.log) 
    though the seeding is complete. Just take note of the said error and
    report it to the component owner

2.  If resetting the seeding process doesn't fix the issue, try it again
    (resetting the seeding process). If it still doesn't fix the issue,
    you can try the force z-node replacement

**Verification:** The DMS State alert should clear.

 

#### Problem: Forcing Zseed of Znode/Zmaster/Ztrap

**Validation**: This is done when seeding is stuck or failed and the
recipe for [SEEDING\_STATE\_TIMEOUT Error during
seeding](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-Problem:SEEDING_STATE_TIMEOUTErrorduringseeding)
does not work.

**Steps**:

The steps below are now deprecated.
Use [Problem:(HOWTORE-SEED)SEEDING\_STATE\_TIMEOUTErrorduringseeding](#CTLZenossIncidentResponseRecipes-Proble).

**Verification**: The node should eventually finish seeding. If not, try
force-replacing the node.

1.  ~~ SSH to the Z-Master and stop heartbeat:~~

> ~~\[root@CA2R82ZGPZMASTER \~\]\# supervisorctl stop celery-heartbeat~~
>
> ~~celery-heartbeat: stopped~~

1.  ~~SSH to the provisioner and do the following:~~

> ~~redis-cli hset &lt;znode&gt; state "PROVISIONED"~~
>
> ~~redis-cli hset &lt;znode&gt; zboutput\_ver 0~~
>
> ~~redis-cli hset &lt;znode&gt; inventory\_ver 0~~
>
> ~~redis-cli hget &lt;znode&gt; zboutput\_ver; redis-cli hget
> &lt;znode&gt; inventory\_ver; redis-cli hget &lt;znode&gt; state~~

1.  ~~Repeat the last line until the affected Z-Node changes state from
    PROVISIONED to SEEDING. Once it does, go back to the Z-Master and
    start heartbeat:~~

> ~~\[root@CA2R82ZGPZMASTER \~\]\# supervisorctl start
> celery-heartbeat~~
>
> ~~celery-heartbeat: started~~

#### **Problem: Forcing Z-Node Replacement**

*(This is also called **Z-node re-provisioning / reprovisioning**.
**Reprovisioning** transitions through these states:
PROVISIONING\_REQUESTED → INSTANCE\_CREATE → BOOTSTRAPPING
→ COPYING\_KEYS → CHEF\_CLIENT\_RUNNING → PROVISIONED → SEEDING\_QUEUED
→ SEEDING → SEEDED → MODELING). The most current set of states is
declared
<https://github.com/Tier3/zcomms/blob/master/heartbeat/heartbeat.py#L34-L44> )*

**Validation: ** This is usually done if the z-node is unreachable (also
verify connectivity through SSH), resetting the seeding process doesn't
fix the issue or the Zenoss service/application is broken (GUI not
reachable or Zenoss daemons can't be run). Additionally, the DMS alert
"**\[MISSING\] &lt;Znode name&gt; hasn't checked in**" is received

**Pro Tip :**

You can execute a replacement by logging into the z-console and
executing:

perl /usr/local/bin/replace.l IL1R82ZGPZMASTER

This will replace IL1 Z-Master

**\
Solution(s):**

##### **Option 1: Using z-api**

![C:\\c54069263c430188351fecfab4157393](media/image27.tmp){width="4.635416666666667in"
height="2.6041666666666665in"}

**Figure: Making the node replace request**

A successful response should look like the following.

![C:\\a63e00fb981a4bd1afc6915906eab864](media/image28.tmp){width="4.354166666666667in"
height="2.6041666666666665in"}

**Figure: Response**

##### **Option 2: Manual**

1.On the provisioner, add the z-node to delete\_queue via redis-cli.
This will trigger the provisioning process of the z-node. Note that at
this point, the old z-node is still active and monitoring the devices so
there will be no gaps in monitoring.

\# redis-cli

redis 127.0.0.1:6379&gt; lpush delete\_queue VA1R8RC1ZGPZNODE01

Note : lpush will not work when node is not SEEDED and healthy. In these
cases, use "del". Example:

\# redis-cli

redis 127.0.0.1:6379&gt; del VA1R8RC1ZGPZNODE01

To find out the state of the instance, use : &gt;hget &lt;Znode name&gt;
state. Example :

redis 127.0.0.1:6379&gt; hget VA1R8RC2ZGPZMASTER state

"SEEDING\_QUEUED"

** **2. Wait for the z-node to be seeded and verify the devices in
Zenoss. Monitor the progress on the provisioner.

\# tail -f /var/log/celery/celery-heartbeat.log\
\# tail -f /var/log/celery/celery-provisioning.log

3. After the new z-node is seeded. The provisioner will automatically
stop the old z-node.

4\. Check the Global Z-Console (currently
at [http://10.128.131.81:8080)](http://10.128.131.81:8080)) and ~~delete
the old z-node device with the old IP address (since it's been
replaced)~~ update the IP address like below.

![C:\\c7e2b60a0f6c06e333782eff05fb0b4c](media/image29.tmp){width="4.875in"
height="2.34375in"}

**NOTE:** There is a bug where the old entry of the node that is
replaced is not removed from the z-console automatically. Just delete
the old entry if this happens.

**Verification:** Check if the DMS alert for the particular znode has
cleared

#### **Problem: ZMaster Seeding is stuck in "SEEDING\_QUEUED" state**

**Validation:  **ZMaster is stuck in "SEEDING\_QUEUED" state for a long
time. Check the provisioner for the state of all the z-nodes. A z-node
can be in SEEDING\_QUEUED state if another z-node is still SEEDING. If
another z-node is still SEEDING, be patient until you think it is stuck
(greater than 30 minutes) in SEEDING state. Use the recipe on stuck
SEEDING state.

**Solution(s):**

1.  Go to http://&lt;PROVISIONER IP&gt;:5555/workers

2.  Click the worker with the queue: seeding-zmaster

3.  Find one active task that appears to be stuck which has been in the
    queue for some time\
    causing celery-seeding.log to not move

4.  Revoke by clicking the uuid of the queued tasks under Reserved so it
    won't keep reseeding.

![C:\\b3826745313633d18b96ed72a4691f0c](media/image30.tmp){width="4.875in"
height="2.125in"}

#### **Problem: ZMaster Seeding is stuck for a long (time &gt;9 hours) and also receiving an unexpected: SoftTimeLimitExceeded()**

**Validation:  **ZMaster is stuck in "seeding" state for a long time. 

A similar event below may also be raised :

\[2016-05-05 20:40:20,818: ERROR/MainProcess\] Task
zcomms.provisioner.provisioner.dispatch\_master\[968d46af-550a-4571-8024-62dd10f451b7\]
raised unexpected: SoftTimeLimitExceeded()\
Traceback (most recent call last):\
File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 240,
in trace\_task\
R = retval = fun(*args, \*\*kwargs)\
File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 437,
inprotected\_call\
return self.run(*args, \*\*kwargs)\
File "/home/zenoss/zcomms/provisioner/provisioner.py", line 561, in
dispatch\_master\
time.sleep(60)\
File "/usr/lib64/python2.6/site-packages/billiard/pool.py", line 231, in
soft\_timeout\_sighandler\
raise SoftTimeLimitExceeded()\
SoftTimeLimitExceeded: SoftTimeLimitExceeded()

You may also issue the following command from the chef instance to check
if the instance is in "seeding" status

\[root@VA1ZGPCHEF-W01 \~\]\# DC=all; REL=R8RC2;
/root/zenoss-cookbooks/scripts/knife\_ssh.sh \$DC provisioner 'for i in
\$(redis-cli keys "\*" | grep -E "ZMASTER|ZNODE|TRAP"); do echo -n \$i"
" && redis-cli hget \$i state; done' \$REL | grep -v SEEDED

**\
Solution(s):**

1.Force Z-Node replacement on the Z-Master using "del". (see Forcing
Z-Node Replacement)

 

> \# redis-cli\
> redis 127.0.0.1:6379&gt; del ZMASTER\_INSTANCE\_NAME

**\
Verification: **Check if the DMS alert for the particular znode has
cleared. Also check from the chef instance for instance status.

#### **Problem: Updating Syslog/SNMP Trap Load Balancer Config**

**Validation / Information: ** 

In every datacenter, there is a load balancer.\
For example:\
  
 <https://control.ctl.io/manage#/ca3/group/843451f1bc104992af8996b03cde70c1>

![C:\\4c912903802a6141dd93953ba8fd8559](media/image31.tmp){width="4.875in"
height="2.21875in"}\
\
If you login to the primary,say:
<https://control.ctl.io/manage#/ca3/server/ca3zgpsyslbp01>, you can see
this:\
    \[root@CA3ZGPSYSLBP01 \~\]\# ifconfig\
        eth0     Link encap:Ethernet HWaddr 00:0C:29:F5:8C:CA\
                inet addr:10.100.107.17 Bcast:10.100.107.255
Mask:255.255.255.0\
                inet6 addr: fe80::20c:29ff:fef5:8cca/64 Scope:Link\
                UP BROADCAST RUNNING MULTICAST MTU:1500 Metric:1\
                RX packets:41728206 errors:0 dropped:0 overruns:0
frame:0\
                TX packets:47352417 errors:0 dropped:0 overruns:0
carrier:0\
                collisions:0 txqueuelen:1000\
                RX bytes:6034154448 (5.6 GiB) TX bytes:6221347233 (5.7
GiB)\
        eth0:1     Link encap:Ethernet HWaddr 00:0C:29:F5:8C:CA\
                inet addr:10.100.107.200 Bcast:10.255.255.255
Mask:255.0.0.0\
                UP BROADCAST RUNNING MULTICAST MTU:1500 Metric:1\
    \
Notice eth0:1\
It is the Virtual IP address.  

                 \
Meanwhile, the trap nodes are special zenoss nodes that accept only
traps via the load balancer.The **162** port is load balanced to two
nodes, say for example here, we got \[server CA3ZGPZTRAP01 {\] and
\[server CA3ZGPZTRAP02 {\] from the snmp trap channel below:\
virtual SNMP\_Trap     {\
                        active = 1\
                        address = 10.100.107.200 eth0:1\
                        vip\_nmask = 0.0.0.0\
                        port = 162\
                        expect = "1000"\
                        use\_regex = 0\
                        send\_program =
"/usr/local/bin/zenoss\_healthcheck %h"\
                        load\_monitor = none\
                        scheduler = wrr\
                        protocol = udp\
                        timeout = 6\
                        reentry = 15\
                        quiesce\_server = 0\
                    server CA3ZGPZTRAP01     {\
                                                                 address
= 10.100.107.32\
                                                                 active
= 1\
                                                                 weight
= 1\
                                                                 }\
                    server CA3ZGPZTRAP02     {\
                                                                 address
= 10.100.107.25\
                                                                 active
= 1\
                                                                  weight
= 1\
                                                                 }\
                                     }\
\
Also, we are monitoring the VIPs in Z-Console in this device
group: <http://10.128.131.100:8080/zport/dmd/itinfrastructure#devices:.zport.dmd.Devices.Endpoint.Critical_Endpoint>

![C:\\bda33809ec6c3f769692b5ec3584d52c](media/image32.tmp){width="4.875in"
height="2.4791666666666665in"}

The **HttpMonitor** monitoring template attached to this queries port
8080 which gives us visibility that the ztrap backend servers are ok.

![C:\\092c625b9bb9c8fc1723670305697498](media/image33.tmp){width="4.875in"
height="1.3020833333333333in"}

                 

**After any reprovisioning of Z-Group or of syslog z-nodes, the
syslog/SNMP trap load balancers need to be updated to forward logs to
the newly provisioned syslog z-nodes.**

**\
Solution(s):**

1.Get the IP addresses of the newly provisioned syslog z-Nodes (i.e.
knife node show CA1R8RC2ZGPZTRAP01 in Chef workstation to get IP
address).

2\. SSH to the secondary load balancer. SSH to the primary load balancer
from the secondary load balancer. Take note that SSH directly to the
primary load balancer is not possible.

3\. Update /etc/sysconfig/ha/[lsv.cf](http://lsv.cf) of the primary load
balancer with the following changes:

  -------------------------------------------------------------------------------------------------------------------------------------
  **lsv.cf**                                                        **What to change**
  ----------------------------------------------------------------- -------------------------------------------------------------------
  **virtual ZENOSS {**                                              **Change to the appropriate actual IP address on the following:**
                                                                    
  **    active = 1**                                                -   **virtual ZENOSS**
                                                                    
  **    address = 10.100.107.200 eth0:1**                           -   **virtual syslog**
                                                                    
  **    port = 8080**                                               -   **virtual SNMP\_Trap**
                                                                    
  **    expect = "1000"**                                           
                                                                    
  **    use\_regex = 0**                                            
                                                                    
  **    send\_program = "/usr/local/bin/zenoss\_healthcheck %h"**   
                                                                    
  **    load\_monitor = none**                                      
                                                                    
  **    scheduler = rr**                                            
                                                                    
  **    protocol = tcp**                                            
                                                                    
  **    timeout = 6**                                               
                                                                    
  **    reentry = 15**                                              
                                                                    
  **    quiesce\_server = 0**                                       
                                                                    
  **    server CA3ZGPZTRAP01 {**                                    
                                                                    
  **        address = 10.100.107.32**                               
                                                                    
  **        active = 1**                                            
                                                                    
  **        weight = 1**                                            
                                                                    
  **    }**                                                         
                                                                    
  **    server CA3ZGPZTRAP02 {**                                    
                                                                    
  **        address = 10.100.107.25**                               
                                                                    
  **        active = 1**                                            
                                                                    
  **        weight = 1**                                            
                                                                    
  **    }**                                                         
                                                                    
  **}**                                                             
                                                                    
  **========================================================**      
                                                                    
  **virtual syslog {**                                              
                                                                    
  **    active = 1**                                                
                                                                    
  **    address = 10.100.107.200 eth0:1**                           
                                                                    
  **    port = 514**                                                
                                                                    
  **    expect = "1000"**                                           
                                                                    
  **    use\_regex = 0**                                            
                                                                    
  **    send\_program = "/usr/local/bin/zenoss\_healthcheck %h"**   
                                                                    
  **    load\_monitor = none**                                      
                                                                    
  **    scheduler = wrr**                                           
                                                                    
  **    protocol = udp**                                            
                                                                    
  **    timeout = 6**                                               
                                                                    
  **    reentry = 15**                                              
                                                                    
  **    quiesce\_server = 0**                                       
                                                                    
  **    server CA3ZGPZTRAP01 {**                                    
                                                                    
  **        address = 10.100.107.32**                               
                                                                    
  **        active = 1**                                            
                                                                    
  **        weight = 1**                                            
                                                                    
  **    }**                                                         
                                                                    
  **    server CA3ZGPZTRAP02 {**                                    
                                                                    
  **        address = 10.100.107.25**                               
                                                                    
  **        active = 1**                                            
                                                                    
  **        weight = 1**                                            
                                                                    
  **    }**                                                         
                                                                    
  **}**                                                             
                                                                    
  **========================================================**      
                                                                    
  **virtual SNMP\_Trap {**                                          
                                                                    
  **    active = 1**                                                
                                                                    
  **    address = 10.100.107.200 eth0:1**                           
                                                                    
  **    vip\_nmask = 0.0.0.0**                                      
                                                                    
  **    port = 162**                                                
                                                                    
  **    expect = "1000"**                                           
                                                                    
  **    use\_regex = 0**                                            
                                                                    
  **    send\_program = "/usr/local/bin/zenoss\_healthcheck %h"**   
                                                                    
  **    load\_monitor = none**                                      
                                                                    
  **    scheduler = wrr**                                           
                                                                    
  **    protocol = udp**                                            
                                                                    
  **    timeout = 6**                                               
                                                                    
  **    reentry = 15**                                              
                                                                    
  **    quiesce\_server = 0**                                       
                                                                    
  **    server CA3ZGPZTRAP01 {**                                    
                                                                    
  **        address = 10.100.107.32**                               
                                                                    
  **        active = 1**                                            
                                                                    
  **        weight = 1**                                            
                                                                    
  **    }**                                                         
                                                                    
  **    server CA3ZGPZTRAP02 {**                                    
                                                                    
  **        address = 10.100.107.25**                               
                                                                    
  **        active = 1**                                            
                                                                    
  **        weight = 1**                                            
                                                                    
  **    }**                                                         
                                                                    
  **}**                                                             
  -------------------------------------------------------------------------------------------------------------------------------------

4. SCP the updated configuration to the secondary load balancer.

\# scp /etc/sysconfig/ha/[lvs.cf](http://lvs.cf)  &lt;secondary load
balancer&gt;:/etc/sysconfig/ha/[lvs.cf](http://lvs.cf)

5\. Turn on the rsyslog service on the primary and secondary load
balancer.

 

\# service rsyslog start

6. Restart Pulse service in both secondary and primary load balancers.
Start the secondary load balancer first.

\# service pulse restart 

7. Verify secondary load balancer is setup as backup.

> \# tail -f /var/log/messages\
> Apr 24 04:23:41 VA1JRMTSYSLBS01 yum\[23615\]: Installed:
> php-5.3.3-40.el6\_6.x86\_64\
> Apr 24 04:23:41 VA1JRMTSYSLBS01 yum\[23615\]: Installed:
> libnl-1.1.4-2.el6.x86\_64\
> Apr 24 04:23:41 VA1JRMTSYSLBS01 yum\[23615\]: Installed:
> ipvsadm-1.26-4.el6.x86\_64\
> Apr 24 04:23:42 VA1JRMTSYSLBS01 yum\[23615\]: Installed:
> piranha-0.8.6-4.el6\_5.2.x86\_64\
> Apr 24 04:48:35 VA1JRMTSYSLBS01 yum\[23724\]: Installed:
> openssh-clients-5.3p1-104.el6\_6.1.x86\_64\
> Apr 24 04:49:42 VA1JRMTSYSLBS01 pulse\[23754\]: STARTING PULSE AS
> BACKUP\
> Apr 24 04:49:42 VA1JRMTSYSLBS01 kernel: IPVS: Registered protocols
> (TCP, UDP, SCTP, AH, ESP)\
> Apr 24 04:49:42 VA1JRMTSYSLBS01 kernel: IPVS: Connection hash table
> configured (size=4096, memory=64Kbytes)\
> Apr 24 04:49:42 VA1JRMTSYSLBS01 kernel: IPVS: ipvs loaded.\
> Apr 24 04:49:42 VA1JRMTSYSLBS01 kernel: IPVS: sync thread started:
> state = BACKUP, mcast\_ifn = eth0, syncid = 0

8. Verify that the new syslog z-nodes are reachable from the load
balancer.

> \# ipvsadm -L\
> IP Virtual Server version 1.2.1 (size=4096)\
> Prot LocalAddress:Port Scheduler Flags\
>  -&gt; RemoteAddress:Port           Forward Weight ActiveConn
> InActConn\
> TCP  10.126.99.200:webcache rr\
>  -&gt; 10.126.99.79:webcache        Route   1      0          0\
>  -&gt; 10.126.99.80:webcache        Route   1      0          0\
> UDP  10.126.99.200:snmptrap wrr\
>  -&gt; 10.126.99.79:snmptrap        Route   1      0          0\
>  -&gt; 10.126.99.80:snmptrap        Route   1      0          0\
> UDP  10.126.99.200:syslog wrr\
>  -&gt; 10.126.99.79:syslog          Route   1      0          0\
> -&gt; 10.126.99.80:syslog          Route   1      0          0

5\. After you are done debugging the load balancers, turn off the rsyslog
service.

\# service rsyslog stop

**Verification: **

#### **Problem: zseed: Adding / Updating / Removing Devices from Inventory**

**Seeding should only be done around 9AM Mon-Fri with Jared's consent.**

**Validation:\
Solution(s):**

1.Make changes to Z-Controller Zenoss Core Web GUI .  Make sure that the
state you leave it in is perfect: localhost is in production state,
events and jobs are clear, dashboard is good, search fields are
unpopulated, etc.

2\. On the workstation, edit the manifest file (e.g.
manifest\_va1\_r8rc1.json) for the Z-Group. Update the device mapping
for each z-node to distribute the workload and increment the mapping
version:

\# cd \~/ctl-chef/data\_bags/zenoss

\# vi manifest\_va1\_r8rc1.json

  ...\
  "mapping": {\
   "version": 2015060101,\
   ...\
   "VA1R8RC1ZGPZNODE01": \[\
 {\
   "description": "VA1-BE-10G-R4R5-U0",\
   "name": "VA1-BE-10G-R4R5-U0",\
   "device\_class": "/Arista",\
   "check\_dp\_start": false\
 },\
 ...

3\.  Upload the manifest to Chef.

\# knife data bag from file zenoss manifest\_va1\_r8rc1.json

4. On the Z-Controller, run the zb\_commit script to update the backup
version.

\# cd /home/zenoss/zcomms/messaging && env PYTHONPATH=/home/zenoss
python helpers/zb\_commit.py --zb-commit -r manifest\_va1\_r8rc1

5. The provisioner should be able to pick up the changes in manifest
mapping version and backup version. This will trigger the re-seeding
process of the z-nodes to apply the new mapping. Wait for the z-node to
be seeded and verify the devices in Zenoss. Monitor the progress on the
provisioner.

\# tail -f /var/log/celery/celery-heartbeat.log\
\# tail -f /var/log/celery/celery-provisioning.log

**Verification: **

#### **Problem: Rebalancing Polling Workload across Worker Z-Nodes**

**Seeding should only be done around 9AM Mon-Fri with Jared's consent.**

**Validation:\
Solution(s):**

1.On the workstation, edit the manifest file (e.g.
manifest\_va1\_r8rc1.json) for the Z-Group. Update the device mapping
for each z-node to distribute the workload and increment the mapping
version:

\# cd \~/ctl-chef/data\_bags/zenoss\
\# vi manifest\_va1\_r8rc1.json\
  ...\
  "mapping": {\
   "version": 2015060101,\
   ...\
   "VA1R8RC1ZGPZNODE01": \[\
 {\
   "description": "VA1-BE-10G-R4R5-U0",\
   "name": "VA1-BE-10G-R4R5-U0",\
   "device\_class": "/Arista",\
   "check\_dp\_start": false\
 },\
 ...

2. Upload the manifest to Chef.

\# knife data bag from file zenoss manifest\_va1\_r8rc1.json

3. On the Z-Controller, run the zb\_commit script to update the backup
version.

\# cd /home/zenoss/zcomms/messaging && env PYTHONPATH=/home/zenoss
python helpers/zb\_commit.py --zb-commit -r manifest\_va1\_r8rc1

4. The provisioner should be able to pick up the changes in manifest
mapping version and backup version. This will trigger the re-seeding
process of the z-nodes to apply the new mapping. Wait for the z-node to
be seeded and verify the devices in Zenoss. Monitor the progress on the
provisioner.

\# tail -f /var/log/celery/celery-heartbeat.log\
\# tail -f /var/log/celery/celery-provisioning.log

**\
Verification: **

#### **Problem: Provisioner/Z-Comms Heartbeat; PROVISIONER\_HEALTH\_NOK**

**Validation / Information: **The Provisioner periodically produces
heartbeat. The Provisioner heartbeat is then consumed by the Z-Master.
Once the heartbeat is received, the Z-Master stores the health
information in the state table which is stored in a local Redis
database. Meanwhile, the Z-Master also produces heartbeat periodically
every 30 seconds. In this cycle, provisioner and z-nodes health are
read. If Provisioner health is not equal to “OK”, a critical message is
sent to the Slack channel. Note that this alert can be considered
cleared if not repeating.

**Solution(s): **

1.  Verify that celery-heartbeat is running by executing “*ps ax | grep
    zcomms.heartbeat*” in provisioner and zmaster. There should be at
    least three workers/processes running. If not running, start the
    process by executing “*supervisorctl restart celery-heartbeat*”.

2.  If celery-heartbeat is running on both nodes, verify
    that zcomms.heartbeat.heartbeat.consume\_provisioner\_heartbeat is
    executed every minute and successful. To verify, browse to
    http://&lt;provisioner\_ip&gt;:5555/tasks?limit=100&worker=All&type=zcomms.heartbeat.heartbeat.consume\_provisioner\_heartbeat&state=All

3.  If there are successive failures, escalate the incident to ctl-nms.

**Verification: **

#### **Problem: Provisioner &lt;Provisioner&gt; heartbeat is older than 600 seconds. Last heartbeat received was xxxxxxx.xx with status OK.**

**Validation / Information: **The Z-Master detects that the
Provisioner’s last heartbeat is more than the timeout period. This could
be due to Provisioner not able to produce its heartbeat or Z-Master not
able to update state table in Redis.

**Solution(s):**

1.  Check if the Zmaster for the datacenter is in SEEDING\_QUEUED state.
    This alert is triggered when the zmaster is in this state for a long
    time.

> \#login to the provisioner and check the state of the zmaster. On this
> example, its the DE1 datacenter.
>
> \$ redis-cli
>
> &gt; hget DE1R82ZGPZMASTER state

1.  If the zmaster is not in SEEDING\_QUEUED, proceed to step 3.

2.  Verify that celery-heartbeat is running by executing “*ps ax | grep
    zcomms.heartbeat*”. There should be at least three workers/processes
    running. If not running, start the process by executing
    “*supervisorctl restart celery-heartbeat*”.

3.  If the celery-heartbeat is running, look for any exceptions in the
    Provisioner at (*/var/log/celery/celery-heartbeat.log*). 

4.  Report the exception/s to CTL DevOps as an urgent card \[not
    emergency\]. You can escalate as an emergency if it becomes
    persistent (more than three times).

**Verification: **

#### **Problem: Provisioning failures**

**Symptoms: "Provisioner XXX: Timeout Exceeded", etc**

**Validation / Information: **Provisioner is unable to complete
provisioning due to some error.

**Solution(s):**

1.  Identify the root cause. If the error is due to an infrastructure
    problem, wait for the issue to resolve before reprovisioning.

2.  Once the underlying issue is resolve, reprovision the znode manually
    by force-replacing the node.

**Verification: **

#### **Problem: **Znode &lt;ZNODE&gt;: Acquire on closed pool

**Validation / Information: **A known bug in celery which causes rabbit
tcp connection to close
abruptly. <https://github.com/celery/celery/issues/1839>

**Solution(s):**

*There is no action required*. We have already deployed auto-remediation
using a monit rule that checks the logs for this issue and automatically
restarts supervisor. If you still see a persistent (repeats after 5
minutes) exception from the same node, you can use the steps below to
manually restart supervisor and create a Production Ops Issue Trello
card to allow us to deep dive.

1.  If this issue was forwarded to Zendesk ****do not merge**** the
    tickets, close the ticket separately so we can track down supervisor
    restarts and z-node replacements.

2.  Search Zendesk for the most recent ticket related to this issue so
    you know which z-node/s were tackled e.g. search string: "sentry
    Acquire on closed pool order\_by:created sort:desc"

3.  Check this exception in Sentry
    e.g. <http://10.128.131.73:9000/sentry/zcomms/issues/17/>

    1.  Click Related Events tab
        e.g. <http://10.128.131.73:9000/sentry/zcomms/issues/17/events/>

    2.  Check the most recent event and from which Servers the
        exceptions are coming fromSSH in to the Z-Node in question.\
        \
        ![C:\\6a1a42afc7731c867dcfaf694a13c73c](media/image34.tmp){width="4.875in"
        height="2.5in"}\
        Figure: Related events tab, notice which servers the exceptions
        are coming from\
        \
        ![C:\\088d622669e7a29238de9ade526fe4fa](media/image35.tmp){width="4.875in"
        height="2.5104166666666665in"}\
        Figure: (another example)

4.  Restart supervisor in the z-node

    1.  \# service supervisor restart

5.  If the error persists, replace the Z-Node.

6.  After the error is resolved, *resolve the Sentry issue*. Update the
    Zendesk ticket with the z-node/s where you restarted supervisor.

We also found instances when this sequence needs to be executed when
this exception is seen in zmaster celery-messaging logs:

1.  Restart supervisor in zmaster

2.  Restart supervisor in provisioner

3.  If exception still appears, restart again supervisor in zmaster

#### **Problem: Error: Znode: No JSON object could be decoded**

** **

**Symptom**: The traceback looks like the following.

![C:\\2e47137e4264acb00f3cd24483ff7eb1](media/image36.tmp){width="4.6875in"
height="2.6041666666666665in"}

The Related Events tab will show you the z-nodes with the issue and
their corresponding timestamp.

**Resolution:**

1.  *No action is needed* but you can observe auto-remediation
    happening. Search for the string "forced reseeding" in Sentry. It
    will show you the exceptions like the one below. The Related Events
    tab will show you the z-nodes that are auto-force-reseeded. If "No
    JSON object could be decoded" persists for a certain z-node even if
    you can see it was already auto-force-reseeded, create a Prod Ops
    Issue Trello card and assign to Jerome / Leo / Prem.\
    \
    \
    ![C:\\803156b281723d234816cec552a9a54b](media/image37.tmp){width="4.875in"
    height="2.4583333333333335in"}\
    Figure: search for "forced reseeding" exceptions\
    \
    ![C:\\78cd4cbab77632c394062db9acf5abf7](media/image38.tmp){width="4.875in"
    height="2.40625in"}\
    Figure: z-nodes that are auto-force-reseeded

#### **Problem: In &lt;ZNODE&gt;: 'findposkeyerror -v10' command returned with exit status 1.**

**Symptoms:**

Corrupted ZODB. To verify ssh to the znode and tail
/opt/zenoss/log/toolbox/findposkeyerror.log. There are warning
findposkey errors in the log.

**Resolution:**

1.  [Re-seed the
    z-node](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-Problem:(HOWTORE-SEED)SEEDING_STATE_TIMEOUTErrorduringseeding).
    This is temporary until this card is
    done <https://trello.com/c/WcmuMt4w/3856-p0-watch-for-poskeyerrors>

2.  If it persists, create a Prod Ops Issue Trello card and assign to
    Jerome / Leo / Prem.

#### **Problem: Duplicate zcomms.messaging consumers causing zseed failure**

**Symptoms**

zseed fails. It is stuck and you will get SEEDING\_STATE\_TIMEOUT alerts
in Slack/Zendesk.

Example:

  -------------------------------------------------------
  SEEDING\_STATE\_TIMEOUT reached in CA1R8RC2ZGPZNODE12
  -------------------------------------------------------

If you check the celery logs in the Z-node you will notice a failure in
the zenrestore step. The error below is caused by a missing zenbackup
image. The zenbackup image is missing because the step that pulls the
zenbackup image from the Z-controller was not executed in the Z-node. A
rogue consumer (from a decommissioned (even if it is already offline)
Z-node) consumed the task. You will also see below how to spot the rogue
consumer in zcomms.messaging celery flower
(<http://PROVISIONER_OF_THE_ZGROUP:5556/>)

/var/log/celery/celery-messaging.log:

\[2015-09-20 13:46:15,137: WARNING/Worker-6\] Restarting
CA1R8RC2ZGPZNODE12

\[2015-09-20 13:46:15,138: WARNING/Worker-6\] Executing client\_pull
step z\_restore...

You must specify either --file or --dir.

Command returned nonzero at
/home/zenoss/zcomms/messaging/scripts/[client\_pull\_zrestore.pl](http://client_pull_zrestore.pl)
line 14.

\[2015-09-20 13:46:19,340: WARNING/Worker-6\] INFO: Restoring ...

\[2015-09-20 13:46:19,360: WARNING/Worker-6\] Details: Traceback (most
recent call last):

 File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 240,
in trace\_task

   R = retval = fun(\*args, \*\*kwargs)

 File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 437,
in \_\_protected\_call\_\_

   return self.run(\*args, \*\*kwargs)

 File "/home/zenoss/zcomms/messaging/znode\_tasks.py", line 59, in
restart\_routine

   print run\_client\_pull(step)

 File "/home/zenoss/zcomms/messaging/taskhelper.py", line 98, in
run\_client\_pull

   raise Exception("run\_client\_pull %s command returned with exit
status %s." % (step, ret.group(1)))

Exception: run\_client\_pull z\_restore command returned with exit
status 255.

Figure: Duplicate consumers. One of them from a decommissioned Z-node
that might be already offline

**Resolution**

Cancel the rogue consumer:

Go to the Z-group’s zcomms.messaging celery flower
([http://PROVISIONER\_ADDRESS:5556](http://provisioner_address:5556)).

You should see the list of workers. Spot the worker of the Z-node in
question. You should see multiple workers of the same Z-node.

Get the ID of the consumer that is the most current. In the current
Z-node:

\# ps aux | grep messaging

root     19266  0.7  0.0 246788 23576 ?        S    14:19   0:01
/usr/bin/python /usr/bin/celery worker -A zcomms.messaging.celeryapp
--loglevel=INFO -Ofair --concurrency=10 --queues=CA1R8RC2ZGPZNODE12 -n
messaging.20150920141901.%h

...

20150920141901 is the ID. Click the rogue worker/s in celery flower. Go
to its Queues tab. Cancel the consumer.

Attempt to re-seed using [these
steps](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-Problem:(HOWTORE-SEED)SEEDING_STATE_TIMEOUTErrorduringseeding).

 

#### Problem: XXXPROVISIONER HTTPConnectionPool(host='10.128.131.201', port=5984): Read timed out. (read timeout=5). 

**Symptom: **

Traceback (most recent call last):\
 File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 240,
in trace\_task\
   R = retval = fun(\*args, \*\*kwargs)\
 File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 437,
in \_\_protected\_call\_\_\
   return self.run(\*args, \*\*kwargs)\
 File "/home/zenoss/zcomms/heartbeat/heartbeat.py", line 999, in
get\_devices\
   r = requests.get(device\_url, timeout=5)\
 File "/usr/lib/python2.6/site-packages/requests/api.py", line 59, in
get\
   return request('get', url, \*\*kwargs)\
 File "/usr/lib/python2.6/site-packages/requests/api.py", line 48, in
request\
   return session.request(method=method, url=url, \*\*kwargs)\
 File "/usr/lib/python2.6/site-packages/requests/sessions.py", line 451,
in request\
   resp = self.send(prep, \*\*send\_kwargs)\
 File "/usr/lib/python2.6/site-packages/requests/sessions.py", line 557,
in send\
   r = adapter.send(request, \*\*kwargs)\
 File "/usr/lib/python2.6/site-packages/requests/adapters.py", line 422,
in send\
   raise ReadTimeout(e, request=request)\
ReadTimeout: HTTPConnectionPool(host='10.128.131.201', port=5984): Read
timed out. (read timeout=5)

**Resolution:**

This alert can be ignored if it is not repeating. Otherwise, see below.

Each provisioner pass their StateDB table to a couchdb 10.128.131.201. 

To quickly check the connectivity between the provisioner and the
zconsole, perform the following:

1.  SSH into the provisioner.

2.  Perform \`telnet 10.128.131.201 5984\` and see if a connection is
    established

3.  Perform \`curl http://10.128.131.201:5984\` and see if a connection
    is established

4.  Perform \`ping  10.128.131.201\` and see if there is no packet loss.

You can also check if the issue is resolved by looking for lines that
look like:

\[2015-10-04 05:14:28,351: INFO/MainProcess\] Received task:
zcomms.heartbeat.heartbeat.get\_devices\[633d7ea2-3186-4fca-8ee9-96d5c26ca080\]\
\[2015-10-04 05:14:30,032: INFO/MainProcess\] Task
zcomms.heartbeat.heartbeat.get\_devices\[633d7ea2-3186-4fca-8ee9-96d5c26ca080\]
succeeded in 1.67975160852s: None

in the celery-provisioning.log file. Alternatively you can use the
Celery web interface.

1.  Open the Celery web interface by vising http://&lt;ip of
    provisioner&gt;:5555/

2.  Click on the Tasks Tab

3.  Select the heartbeat log for the provisioner on the worker and the
    task type \`zcomms.heartbeat.heartbeat.get\_devices\` then click
    Apply Filters.\
    ![C:\\8652ff7b6900820268291f61024f57d1](media/image39.tmp){width="4.333333333333333in"
    height="2.6041666666666665in"}

4.  Notice that after a failure, you should see subsequent successes
    which indicate the issue has been resolved. 

If the issue is not solved, escalate to CTL team.

 

#### Problem: Restart Zenoss in ZNodes/ZConsole

If there is a need to restart zenoss, particularly in the Zconsole, use
the wrapper script in /etc/init.d/zenoss.sh

\[root@VA1ZGPZCONSOL02 \~\]\# cat /etc/init.d/zenoss.sh\
\#!/bin/bash\
start()\
{\
   /etc/init.d/zenoss start\
   sleep 10 \# seconds\
}\
stop()\
{\
   /etc/init.d/zenoss stop\
   sleep 10 \# seconds\
   ps -U zenoss -u zenoss -o pid= | xargs -r kill -9\
}\
case "\$1" in\
   start)\
       start\
       ;;\
   stop)\
       stop\
       ;;\
   \*)\
       echo \$"Usage: \$0 {start|stop}"\
esac\
exit 0

For ZNodes/Zmaster, stop the monit script first prior to performing a
zenoss restart.

/etc/init.d/monit stop

zenoss stop; zenoss start;

/etc/init.d/monit start

As zenperfdataforwarder takes a while to stop itself.

 

#### **Problem: Reinstating Z-Node into Provisioner's State DB (Split-Brain Scenario)**

**Information**: Z-Node will be replaced by the Provisioner when it
missed z-node's heartbeat or found the z-node unhealthy. However, there
are times when these are caused by lower-level infrastructure failure
such as connectivity issues. In such case, replacing the node will not
resolve the issue. The preferred temporary resolution during this
scenario is to put the z-group into safe-mode (see Problem: Z-GROUP Safe
Mode).\
However, once the underlying issue is resolved (e.g. network issue),
Provisioner's state DB may not reflect the correct/working/healthy
Z-NODE (split-brain scenario). In this case, the state DB should be
inspected.\
**Solution(s)**:

1.  SSH in to the Z-Group's/DC's provisioner.

2.  Make sure provisioner is in safe mode (i.e supervisor/celery
    processes are not running)\
    \# /etc/init.d/supervisor stop\
    \# ps -ef | grep celery

3.  Edit /home/zenoss/zcomms/utils/restore\_state.py. Set username and
    password variables ([control.ctl.io](http://control.ctl.io)
    credentials).

4.  For each z-node including z-master, find the healthy virtual machine
    in <https://control.ctl.io>.

5.  Select one healthy machine for each z-node and get its
    machine/server id. This is usually indicated in the URL for device
    details page. For example, in
    <https://control.ctl.io/manage#/ca3/server/ca3zgpznode101>,
    ca3zgpznode101 is the server id.

6.  To reinstate the machine as the active z-node, run the command below
    in the provisioner.

/home/zenoss/zcomms/utils/restore\_state.py &lt;DC&gt;
&lt;SERVER/MACHINE\_ID&gt; &lt;ROLE-zmaster\_or\_znode&gt;. For
example:\
/home/zenoss/zcomms/utils/restore\_state.py CA3 ca3zgpznode101 znode

1.  The command will automatically identify the node id (e.g.
    CA3R8RC2ZGPZNODE01)

2.  Run restore\_state.py command for all nodes that need to be
    reinstated to the statedb.

#### **Problem: Component: /opt/zenoss/perf threshold of Greater than 90 percent used not met**

**Symptom:**

Component: /opt/zenoss/perf \
Severity: 3 \
Time: 2015/10/09 01:24:04.000 \
Message: \
threshold of Greater than 90 percent used not met: current value
496612.000000 

**Resolution:**

Perform "[Forcing Z-Node
Replacement](file:///C:\wiki\display\CLCDEV\CTL+Zenoss+Incident+Response+Recipes)"
on the affected node.

#### Error Code: Maximum provisioning retries reached

**Symptom:**

Examples:

1.  Traceback (most recent call last):\
     File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line
    240, in trace\_task\
       R = retval = fun(\*args, \*\*kwargs)\
     File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line
    437, in \_\_protected\_call\_\_\
       return self.run(\*args, \*\*kwargs)\
     File "/home/zenoss/zcomms/provisioner/provisioner.py", line 132, in
    create\_instance\
       self.retry()\
     File "/usr/lib/python2.6/site-packages/celery/app/task.py", line
    665, in retry\
       [self.name](http://self.name), [request.id](http://request.id),
    S.args, S.kwargs))\
    MaxRetriesExceededError: Can't retry
    zcomms.provisioner.provisioner.create\_instance\[1fb4eea6-aad2-47de-836a-3a7e9f89430d\]

> ...

1.  Traceback (most recent call last):

> File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 240,
> in trace\_task
>
>   R = retval = fun(\*args, \*\*kwargs)
>
> File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 437,
> in \_\_protected\_call\_\_
>
>   return self.run(\*args, \*\*kwargs)
>
> File "/home/zenoss/zcomms/provisioner/provisioner.py", line 154, in
> get\_server
>
>   self.retry()
>
> File "/usr/lib/python2.6/site-packages/celery/app/task.py", line 665,
> in retry
>
>   [self.name](http://self.name), [request.id](http://request.id),
> S.args, S.kwargs))
>
> MaxRetriesExceededError: Can't retry
> zcomms.provisioner.provisioner.get\_server\[e927419e-3284-454a-9300-f073bc859dec\]
> args:(\[(u'ca3-23457', u'ZGP', {'status': None, 'context\_key':
> 'newserver', 'context\_val':
> u'/v2/servers/ZGP/90d3131d1d9441f89bc368eed9964fa1?uuid=True'})\],
> ('zenoss.zgp\_prod', '\*\*\*\*\*\*\*\*\*\*\*'))
> kwargs:{'api\_endpoint':
> '[*https://api.ctl.io*](https://api.ctl.io/)', 'api\_sslverify': True}

1.  Provisioner CA3R8RC2ZGPPROVISIONER: Maximum provisining retries
    reached..

> Traceback (most recent call last):
>
> File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 240,
> in trace\_task
>
>  R = retval = fun(\*args, \*\*kwargs)
>
> File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 437,
> in \_\_protected\_call\_\_
>
>  return self.run(\*args, \*\*kwargs)
>
> File "/home/zenoss/zcomms/heartbeat/heartbeat.py", line 89, in run
>
>  self.provisioner\_heartbeat()
>
> File "/home/zenoss/zcomms/heartbeat/heartbeat.py", line 132, in
> provisioner\_heartbeat
>
>  self.\_provision\_nodes(manifest)
>
> File "/home/zenoss/zcomms/heartbeat/heartbeat.py", line 639, in
> \_provision\_nodes
>
>  raise Exception("Maximum provisining retries reached..")
>
> Exception: Maximum provisining retries reached..\
> Note: For this traceback there is a wrong spelling, "Exception:
> Maximum provisining retries reached..". When searching for the string
> on the log file, search for "Exception: Maximum provisining retries
> reached" or "Exception: Maximum provisioning retries reached.."

**Description:** The Provisioner will try to reprovision failed nodes if
the nodes are found to be unhealthy or with missed heartbeat. However,
it will recreate the nodes only up to the REBUILD\_THRESHOLD (max 3)
configured in provisionerconfig.py. Once reached, the provisioner will
stop reprovisioning the unhealthy node. This a safety mechanism to
ensure that CTL Cloud is not flooded with instances.

**Resolution:**

> 1\. In the Z-Group’s Provisioner, inspect
> /var/log/celery/celery-provisioning.log. Search for the keyword
> “Exception occurred.. Attempting to recreate server..”. Scroll down
> until traceback is seen.
>
> a\. If the error is caused by API failure such as shown below, create a
> ticket to the Tier3 NOC to fix the issue.
>
> b\. APIFailedResponse: Response code 400.  The request is invalid. POST
> https://api.ctl.ioservers/ZGP
>
> c\. APIFailedResponse: Response code 400.  CPU limit exceeded -&gt;
> available: 0, requested: 4 POST https://api.ctl.io
>
> d\. APIFailedResponse: Response code 400.  Memory limit exceeded -&gt;
> available: 0, requested: 4 POST https://api.ctl.io
>
> e\. APIFailedResponse: Response code 500.  An error has occurred. POST
> https://api.ctl.io/v2/servers/ZGP (FIX: Try manually creating a CentOS 6
> server in the datacenter in question. If it fails, find the blueprint
> and build log in https://control.ctl.io/Queue (filter failed and
> datacenter). Report the build log to help@ctl.io)
>
> f\. For other issues not documented you can use this recipe to triage
> CTL's Control API.
>
> 2\. This error could also be caused by multiple reprovisioning of znodes
> due to heartbeat or health failure. If so, fix znode issue first before
> proceeding to the next step.
>
> a\. Once the root cause is fixed, reprovisioning of nodes can be
> restarted by executing the following in the provisioner node.
>
> i\. \$ redis-cli
>
> ii\. redis 127.0.0.1:6379&gt; del heartbeat\_timeout
> provisioning\_timeout
>
> iii\. redis 127.0.0.1:6379&gt; del &lt;NODENAME&gt;
>
> iv\. redis 127.0.0.1:6379&gt; quit
>
> v\. or: \# redis-cli hgetall heartbeat\_timeout; redis-cli hgetall
> provisioning\_timeout
>
> vi\. \# redis-cli del provisioning\_timeout 
>
> 3\. The provisioner will then try to create the node that was deleted in
> the state table. Inspect /var/log/celery/celery-heartbeat.log for any
> issues.
>
> a\. If you don't see a blueprint / build queued in
> https://control.ctl.io/Queue (filter by pending and datacenter) after
> around 5 minutes, try to restart the supervisor process and retry
> reprovisioning the node in question 
>
> i\. \# supervisorctl stop celery-heartbeat celery-provisioning
>
> ii\. \#redis-cli
>
> iii\. del &lt;znode&gt;
>
> iv\. exit
>
> v\. \# supervisorctl start celery-heartbeat celery-provisioning
>
> 4\. If no error was identified in the celery-provisioning.log, try
> resetting the timeout and then trigger replacement. Then tail
> celery-provisioning log for inspect error.  
>
> 5\. If you still get an error, create a ticket by sending an email to
> <help@ctl.io> CC <ctl@cascadeo.com>. Include the traceback error and
> your Support PIN in the email. The issue will be handled by CTL's NOC.
> Updates will go the requester and <ctl@cascadeo.com>. 

 

#### **Problem: ** \[GLOBAL Z-CONSOLE\] &lt;ZNODE NAME&gt; &lt;ZNODE IP&gt; is DOWN!

**Information: **When a z-node is replaced, the old/unhealthy znode is
powered off which may cause the above alert as well as alerts from DMS.
This is not critical unless there are errors in provisioning.

**Solutions:**

1.  SSH in to the Provisioner node for the DC.

2.  Verify that the node is being replaced.

    1.  Inspect /var/log/celery/celery-provisioning.log. The log should
        show some activity.  If not, verify further by checking celery
        flower (step below).

    2.  Browse http://&lt;provisioner\_ip&gt;:5555/tasks?limit=100

        1.  In Workers drop down menu, select
            celery@provisioner.&lt;timestamp&gt; and then click the
            Apply Filter button.

        2.  You should see tasks in STARTED or RECEIVED state. 

        3.  If there are **no** STARTED or RECEIVED tasks, identify the
            node name by looking at the device name in z-console. Once
            identified, perform  "[Forcing Z-Node
            Replacement](file:///C:\wiki\display\CLCDEV\CTL+Zenoss+Incident+Response+Recipes)"
            for the node. 

3.  Monitor /var/log/celery/celery-provisioning.log until provisioning
    and seeding is completed. A successful provisioning/seeding should
    show something like:

> \[2015-10-10 09:53:06,132: WARNING/Worker-5\] Task:
> a21f59c8-7dc4-45d9-9b3a-034e0d2ef083\
> \[2015-10-10 09:53:06,158: WARNING/Worker-5\] Terminal Task:
> ce93ab87-cbc6-4147-b4e8-32d95d7ac498\
> \[2015-10-10 09:53:31,587: INFO/Worker-5\]
> zcomms.provisioner.provisioner.dispatch\_znode\[3cf46d3c-ce39-43a8-af5c-d6c78762003b\]:
> In WA1R8RC2ZGPZNODE06: Done znode\_handoff\_monitor.\
> \[2015-10-10 09:53:31,587: WARNING/Worker-5\] Done seeding
> WA1R8RC2ZGPZNODE06.\
> \[2015-10-10 09:53:31,588: WARNING/Worker-5\] Details: None\
> \[2015-10-10 09:53:32,006: WARNING/Worker-5\] Slack Response: 200,
> Text: ok\
> \[2015-10-10 09:53:32,009: INFO/MainProcess\] Task
> zcomms.provisioner.provisioner.dispatch\_znode\[3cf46d3c-ce39-43a8-af5c-d6c78762003b\]
> succeeded in 273.756327236s: None

1.  If there are exceptions/errors, a ticket would be auto-generated.
    This should be escalated to CTL dev team if not covered by any
    recipe.

2.  Verify that DMS have cleared. If not, escalate to CTL dev team.** **

#### **Problem: \[MISSING\] &lt;Datacenter&gt; Message Volume hasn't checked in**

**Symptom:**

** **

Hi <dms-ctl@cascadeo.com>,

FYI "DE1 Message Volume" doesn't seem to be working.

Last healthy check-in: 30 minutes ago (14 Oct 01:30 UTC)

You might want to check it out:

<https://deadmanssnitch.com/snitches/8cf6be21ad>

Would you like to pause your snitch?

<https://deadmanssnitch.com/snitches/8cf6be21ad/pause>

** **

Tags: \
- Production
&lt;<https://deadmanssnitch.com/snitches?tags=Production>&gt; \
- DE1 &lt;<https://deadmanssnitch.com/snitches?tags=DE1>&gt; \
- ElasticSearchVolume \
&lt;<https://deadmanssnitch.com/snitches?tags=ElasticSearchVolume>&gt;

Kind regards,

Dead Man's Snitch

**Description:** There is a script in the z-console that pings the DMS
endpoint only when a certain threshold for the datacenter is met.

**Solution: Assign this as a high-priority item (needs acknowledgement;
no need to page) to the on-call CTL Dev.**

The recipe that deploys the script is
in <https://github.com/Tier3/zenoss-cookbooks/blob/master/cookbooks/z-console/recipes/cron-scripts.rb>

\['bin', 'conf', 'cron'\].each do |dir|

bash "update\_creds\_cron\_\#{dir}" do

code &lt;&lt;-EOF

sed -i
's/\\\#{default\_zenoss\_password}/\#{s\["z\_admin\_password"\]}/g'
/opt/zconsole/zconsole-cron/\#{dir}/\*

sed -i 's/\\\#{cascadeo\_kibana\_pass}/\#{s\["kibana\_password"\]}/g'
/opt/zconsole/zconsole-cron/\#{dir}/\*

EOF

end

end

1.  ~~Adjust the threshold of the datacenter in
    the monitor\_elasticsearch\_volume.l script~~

    1.  ~~Create a backup copy of the script in GitHub before making any
        changes. The script is located
        [here](https://github.com/cascadeo/ops/blob/master/ctl/scripts/monitor_elasticsearch_volume.l). ~~

    2.  ~~Update the threshold value for the affected datacenter.~~

        1.  ~~Go to the [CTL Kibana
            Dashboard](https://ctl-kibana.centurylinkcloud.com/#/dashboard/elasticsearch/Zenoss%20Dashboard)
            and click on the datacenter that is affected under TOTAL
            MESSAGE VOLUME BY DC. Change the time filter to "last 5
            minutes".~~\
            ![C:\\90280f2ed7f5d5e8bf838e5ee8eb7a28](media/image40.tmp){width="3.8645833333333335in"
            height="2.6041666666666665in"}

        2.  ~~Hover on the bar graph on the TOTAL MESSAGE VOLUME BY DC
            and record the value.~~\
            ![C:\\d6fa9a0841ca33715ccb9d914d697b92](media/image41.tmp){width="3.2291666666666665in"
            height="2.6041666666666665in"}

        3.  ~~Adjust the threshold on the script (the script is located
            in the
            Z-Console:/etc/cron.d/monitor\_elasticsearch\_volume.l) so
            that it is lower than the value you got on the Kibana
            graph.~~

2.  ~~Confirm if the change clears the alert~~

3.  ~~If the change clears the alert, push the change to GitHub.~~

4.  ~~Send an email to <ctl@cascadeo.com> and report the changes that
    were made to the script.~~

** **

#### **Problem: Z**enoss down alerts for x.x.x.200

**Symptom:**

 

Usually preceded by down alerts for ztrap nodes indicating node
replacement

**Solution: Need to manually update load balancer configs**

1.  Look up the load balancer IPs for the affected DC.

    1.  Example Primary: GB3ZGPSYSLBP02

    2.  Example Secondary: GB3ZGPSYSLBS02

2.  ** **ssh to the secondary load balancer

    1.  Note that you will only be able to ssh to the backup LB, while
        active LB will reject ssh connections

3.  Open another session and ssh to the chef-workstation @ 10.128.131.18

4.  To find out the IPs for the ztrap nodes try:

    1.  \# knife node show GB3R8RC2ZGPZTRAP01

    2.  \# knife node show GB3R8RC2ZGPZTRAP02

5.  Now go back to the secondary LB and update the lvs config with the
    new IP's (this will be in three places.

    1.  \`vi /etc/sysconfig/ha/[lvs.cf](http://lvs.cf)\`

    2.  \`service pulse restart\`

    3.  \`ipvsadm -L\`

        1.  note: when you restart pulse on secondary, there will be no
            output for ipvsadm -L since it is inactive

    4.  OR using VIM regexp \`%s/&lt;old-ip&gt;/&lt;new-ip&gt;/g**\`**

6.  scp the lvs config from secondary to primary

    1.  scp /etc/sysconfig/ha/[lvs.cf](http://lvs.cf) &lt;active
        LB&gt;:/etc/sysconfig/ha/[lvs.cf](http://lvs.cf)

7.  ssh from the secondary load balancer to the primary

8.  restart pulse, and check connections

    1.  \`service pulse restart\`

    2.  \`ipvsadm -L\`

9.  Healthy output should look like this:

10. \# ipvsadm -L

 IP Virtual Server version 1.2.1 (size=4096)\
 Prot LocalAddress:Port Scheduler Flags\
 -&gt; RemoteAddress:Port           Forward Weight ActiveConn InActConn\
 TCP  10.105.99.200:webcache rr\
 -&gt; 10.105.99.22:webcache        Route   1      0          0\
 -&gt; 10.105.99.29:webcache        Route   1      0          0\
UDP  10.105.99.200:snmptrap wrr\
  -&gt; 10.105.99.22:snmptrap        Route   1      0          13\
  -&gt; 10.105.99.29:snmptrap        Route   1      0          13\
 UDP  10.105.99.200:syslog wrr\
  -&gt; 10.105.99.22:syslog          Route   1      0          0\
  -&gt; 10.105.99.29:syslog          Route   1      0          0

#### **Problem : \[MISSING\] &lt;Datacenter&gt; Z-MASTER / ZNode hasn't checked in**

**Validation: **

An similar alert is received:

\[MISSING\] VA1 Z-MASTER hasn't checked in

**NOTE: (11/2/2015) for VA1 Z-Master, if there are no other alerts aside
from this alert and NOC spot checks are good, you can wait if this DMS
alerts will persist for 1 hour before taking the steps below or
escalating. This note will be removed once the cause of the issues has
been resolved.**

**Cause:**

-   Most probably caused by high load in the ZNode. Currently under
    investigation

-   Disk space used is high: 

    -   \[root@AU1R82ZGPZNODE01 \~\]\# report\_zenoss.sh -v

> hostname::AU1R82ZGPZNODE01 | uptime::06:29:08 up 2 days, 10:34, 3
> users, load average: 0.87, 0.68, 0.62 | zencount::36 | sdc\_usage::88
> pct full | prodstate::1000 | daemon\_norun::OK: {}
>
> Node is not healthy:\
> disk space used &gt;= 80%

-   \[root@AU1R82ZGPZNODE01 \~\]\# df -h\
    Filesystem Size Used Avail Use% Mounted on\
    /dev/sdc 20G 17G 2.5G 88% /\
    tmpfs 11G 56K 11G 1% /dev/shm\
    /dev/sda1 488M 72M 391M 16% /boot\
    /dev/sdd 20G 44M 20G 1% /opt/zenos\
    tmpfs 4.0G 17M 3.9G 1% /var/lib/rabbitmq\
    tmpfs 5.9G 324M 5.6G 6% /opt/zenoss/perf\
    tmpfs 4.9G 2.3G 2.7G 46% /var/lib/mysql\
    tmpfs 1000M 318M 683M 32% /opt/zenoss/log

**Solution:**\
1) Check if there are no other DMS alerts related to the ZNode. If
there's none, then follow these steps.

2\) SSH to the affected Znode.

3\) Check the load of the Znode using 'top' or 'report\_zenoss.sh -v'. If
the load is greated than 2, then we must restart the zenoss services.
While reviewing 'top' please take note of the processes with the highest
load (at least the top five) and put it in the ticket when you update
it.

4\) Before restarting the Zenoss services, 'monit' needs to be stopped
first:

   \# /etc/init.d/monit stop (verify if it stopped)

   \#  /etc/init.d/zenoss.sh stop

5\) Verify if all the Zenoss processes have stopped. Once verified
restart the Zenoss services:

  \# /etc/init.d/zenoss.sh start

6\) Verify if all Zenoss service have started:

  \# su - zenoss

  \# zenoss status

7\) Check the load if it's decreasing. It might take some time. Wait for
15-20 minutes and check if the DMS alert will clear.

8\) Once the DMS alert has cleared, start the 'monit' service again (as
root):

 \#/etc/init.d/monit start

** **

**Verification:**

** **

Alert should clear once the load decreased. If the steps above does not
resolve the issue immediately, you can try the force replacement recipe.
If the recipe does not fixed the issue, escalated to the CTL team. 
Please note that this issue particulary the cause of the high load is
currently being investigated so the alert might happen multiple times
within a day.

** **

#### **Problem : \[MISSING\] &lt;Datacenter&gt; STATE Z-TRAPLOGXX hasn't checked in**

**Possible causes:**

-   Trap storm

-   Unable to resolve DMS endpoint domain or local resolver issue

##### **Possible cause: How to spot the nature of the storm**

1.  Check the TRAP MESSAGES THROUGHPUT of the Datacenter in Kibana:
    <https://kibana-cascadeo.analytics.ctl.io/goto/0d9d88246f177bfe06ae1f0d3ce1bb55>
     (Need to adjust time range). If most or all of the ztraps go up and
    down this means there might be a storm.\
    \
    Example: Notice in the attached graph below that there’s an
    inconsistency in the number of counts of the IL1 Ztraps hostnames.

2.  We zoom in to the highest peak to get the narrowest range. \
    \
    In IL1 example, clicking the highest peak would redirect to this
    visualization
    ht[tps://kibana-cascadeo.analytics.ctl.io/goto/f5cb22f999d568847145b4633ddf25a3](https://kibana-cascadeo.analytics.ctl.io/goto/f5cb22f999d568847145b4633ddf25a3)
    with time range from 2016-10-07 12:28:45.000 to 2016-10-07
    12:28:49.999.

3.  Use the time range from Step 2 in
    <https://kibana-cascadeo.analytics.ctl.io/goto/8fffbfe1880e53e7e3a3c7c7856a6be9>
     but adjust the value of the header.location with the datacenter.
    This is to identify which events are overwhelming the ZTRAPs.\
    \
    In the given example, it’s the RT\_SCREEN\_TCP: TCP sweep! which
    overwhelming the IL1 ZTRAPs.

4.  Another source of visualization to look at to figure out the nature
    of the storm:

-   -   <https://goo.gl/1fUwvZ> (shows the source device of the TRAP
        events)

    -   <https://goo.gl/qmCA3z> (shows the event class key)

    -   <https://goo.gl/piFcxG> (shows the device class)

**Solution:**

1.  Scale up another trap if confirmed there's a TRAP storm

2.  Use the API to create a new ZTRAP for the DC affected.

> ![C:\\6b6d7d02a696788ef5c2affd4f894621](media/image42.tmp){width="4.71875in"
> height="2.6041666666666665in"}

1.  Create a Trello card and report the storm to CTL NOC -
    <help@ctl.io> cc <ctl-dev@cascadeo.com> and <noc@cascadeo.com>. 

**Reference Trello cards:**

-   -   [***\
        ***https://trello.com/c/wBUBGGRt/3447-sg1-trap-floods](https://trello.com/c/wBUBGGRt/3447-sg1-trap-floods)

    -   <https://trello.com/c/3otBqkvR/2982-repeating-reprovision-of-ny1-trap-nodes>

    -   <https://trello.com/c/SmaIlj4r/3435-unusual-volume-in-sg1-ztraps-mostly-rt-ids-events>

##### Possible cause: Unable to resolve DMS endpoint domain or local resolver issue

Related cards and tickets: 

-   <https://trello.com/c/NhGaQzbe/4052-ca1-local-resolver-issue-was-ca1-network-latency-issue>

-   <https://t3n.zendesk.com/agent/tickets/1354616>

**Symptoms:**

-   Manual ping to DMS is OK but state DMS remains missing

SSH to provisioner and run the command below to check curl calls.

Example:

(replace the URLs below. Source them from: go to the missing DMS, click
the setup tab)

\# curl -d "m=prem in ca1, just checking in"
<https://nosnch.in/a1ec921b5f>

Got it, thanks!

\# time curl -d "m=prem in ca1, just checking in"
<https://nosnch.in/a1ec921b5f>

Got it, thanks!

real 0m5.472s

user 0m0.044s

sys 0m0.036s

-   these two successive logs can be seen in
    [provisioner:/var/log/celery/celery-heartbeat.log](http://provisioner/var/log/celery/celery-heartbeat.log)
    but a TimeLimitExceeded exceptions follows

**Example:**

\[2017-02-13 03:23:07,952: WARNING/Worker-883\] Sending STATE snitch
(a1ec921b5f) for node CA1R82ZGPZTRAP01..

\[2017-02-13 03:23:07,952: WARNING/Worker-883\] Sending STATE snitch
(a1ec921b5f) for node CA1R82ZGPZTRAP01..

\[2017-02-13 03:23:11,110: ERROR/MainProcess\] Task
zcomms.heartbeat.heartbeat.Heartbeat\[585376cd-9a81-4757-b9f0-cac5cd1ec308\]
raised unexpected: TimeLimitExceeded(48.0,)

Traceback (most recent call last):

File "/usr/lib64/python2.6/site-packages/billiard/pool.py", line 645, in
on\_hard\_timeout

raise TimeLimitExceeded(job.\_timeout)

TimeLimitExceeded: TimeLimitExceeded(48.0,)

\[2017-02-13 03:23:11,111: ERROR/MainProcess\] Hard time limit (48.0s)
exceeded for
zcomms.heartbeat.heartbeat.Heartbeat\[585376cd-9a81-4757-b9f0-cac5cd1ec308\]

-   Check /etc/resolv.conf for the local resolver. Try a lookup and
    compare the lookup time with other resolvers (other DCs or Google
    DNS)

Examples:

\[root@CA2R82ZGPPROVISIONER \~\]\# cat /etc/resolv.conf\
nameserver 10.59.10.19. &lt;--- LOCAL RESOLVER!\
nameserver 8.8.8.8

Install dig tool.

\# yum install bind-utils -y

Notice below the answer is empty.

\[root@CA2R82ZGPPROVISIONER \~\]\# dig @10.59.10.19 nosnch.in

; &lt;&lt;&gt;&gt; DiG 9.8.2rc1-RedHat-9.8.2-0.47.rc1.el6\_8.4
&lt;&lt;&gt;&gt; @10.59.10.19 nosnch.in

; (1 server found)

;; global options: +cmd

;; Got answer:

;; -&gt;&gt;HEADER&lt;&lt;- opcode: QUERY, status: SERVFAIL, id: 62422

;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 0

;; QUESTION SECTION:

;nosnch.in. IN A

;; Query time: 2131 msec

;; SERVER: 10.59.10.19\#53(10.59.10.19)

;; WHEN: Mon Feb 13 22:44:26 2017

;; MSG SIZE rcvd: 27

Notice below there is an answer from Google DNS.

\[root@CA2R82ZGPPROVISIONER \~\]\# dig @8.8.8.8 nosnch.in

; &lt;&lt;&gt;&gt; DiG 9.8.2rc1-RedHat-9.8.2-0.47.rc1.el6\_8.4
&lt;&lt;&gt;&gt; @8.8.8.8 nosnch.in

; (1 server found)

;; global options: +cmd

;; Got answer:

;; -&gt;&gt;HEADER&lt;&lt;- opcode: QUERY, status: NOERROR, id: 29584

;; flags: qr rd ra; QUERY: 1, ANSWER: 2, AUTHORITY: 0, ADDITIONAL: 0

;; QUESTION SECTION:

;nosnch.in. IN A

;; ANSWER SECTION:

nosnch.in. 3 IN A 52.202.146.127

nosnch.in. 3 IN A 52.5.80.15

;; Query time: 2 msec

;; SERVER: 8.8.8.8\#53(8.8.8.8)

;; WHEN: Mon Feb 13 22:44:02 2017

;; MSG SIZE rcvd: 59

Also notice how the curl call takes significant time to finish.

\[root@CA2R82ZGPPROVISIONER \~\]\# time curl -d "just checking in"
<https://nosnch.in/de8a2efe02>\
Got it, thanks!

real 0m5.231s\
user 0m0.071s\
sys 0m0.033s\
\[root@CA2R82ZGPPROVISIONER \~\]\# (edited)

Compare it to a working local resolver.

\[root@AU1R82ZGPZNODE01 \~\]\# time curl -d "just checking
in" <https://nosnch.in/66943eee5b>\
Got it, thanks!

real 0m0.958s\
user 0m0.043s\
sys 0m0.029s

**FIX FOR LOCAL RESOLVER ISSUE**:

You can only do this in the provisioner! (DO NOT CHANGE the sequence of
resolvers in z-nodes) Switch the primary resolver to 8.8.8.8.

\[root@CA2R82ZGPPROVISIONER \~\]\# cat /etc/resolv.conf\
nameserver 8.8.8.8\
nameserver 10.59.10.19\
\#nameserver 8.8.8.8

Restart the celery-heartbeat supervisor process.

\[root@CA2R82ZGPPROVISIONER \~\]\# supervisorctl stop celery-heartbeat\
celery-heartbeat: stopped\
\[root@CA2R82ZGPPROVISIONER \~\]\# supervisorctl status
celery-heartbeat\
celery-heartbeat STOPPED Feb 13 10:56 PM\
\[root@CA2R82ZGPPROVISIONER \~\]\# supervisorctl start celery-heartbeat\
celery-heartbeat: started\
\[root@CA2R82ZGPPROVISIONER \~\]\# supervisorctl status
celery-heartbeat\
celery-heartbeat RUNNING pid 9849, uptime 0:00:13

**Problem: Provisioner &lt;Provisioner name&gt;: ('Connection aborted.',
error(111, 'Connection refused'))**

** **\
**Cause: **

The couchdb service in one the couchdb servers dies or is not running.
There is no need to perform the below solution if the alert is not
recurring.

[*\
**Solution:***](https://trello.com/c/hcXGv6Bz)

1.  [COUCHDB-related connection refused (aborted)
    errors](#CTLZenossIncidentResponseRecipes-COUCHD)

#### **Problem:  \[MISSING\] &lt;Datacenter&gt; RABBITMQ hasn't checked in**

**Causes:**

1.  Multiple rabbitmq processes are running

2.  rabbitmq process died for some reason

3.  z-group rabbitmq was accidentally replaced (this z-node is *no*t
    replaceable)

**Example alert**: \[MISSING\] GB1 RABBITMQ hasn't checked in -
<https://cascadeo.zendesk.com/agent/tickets/183265>

**Solution:**

-   SSH to the RabbitMQ instance and check its status.

Example: (replace the manifest below e.g. manifest\_ca3\_r82\_zgp)

\# /usr/local/bin/report\_rabbit.sh -g
<http://10.128.131.220:4984/zenoss_databag/> -m manifest\_ca3\_r82\_zgp
-v

...

hostname::CA3R82ZGPRABBIT | uptime::14:33:31 up 218 days, 7:10, 1 user,
load average: 0.00, 0.01, 0.19 | amqp\_beam\_count::0 | sdc\_usage::27
pct full | rmq\_zcomms\_user::0 | chk\_vhosts\_ret:: |
chk\_thresh\_ret::

Node is not healthy:

not exactly one beam.smp process running\
zcomms rabbitmq user not defined

**ISSUE 1: Multiple rabbitmq processes are running**

-   Use \`ps aux | grep beam\` to find out the process ID of the
    multiple processes

-   \`kill -15 &lt;PROCESS IDs&gt;\` or \`kill -9 &lt;PROCESS IDs&gt;\`
    to kill

-   /etc/init.d/rabbitmq-server start

**ISSUE 2: z-group rabbitmq was accidentally replaced (this z-node
is *no*t replaceable)**

-   Escalate to CTL Devops (ctl-nms) on-call.

**ISSUE 3: rabbitmq process was killed by OOM killer**

-   \`dmesg\` should have something like below. Notice the *beam.smp*
    process.

-   ...

-   \[12585\] 0 12585 26507 53 2 0 0 bash

-   \[12586\] 0 12586 26507 53 7 0 0 bash

-   Out of memory: Kill process 2039 (beam.smp) score 923 or sacrifice
    child

> Killed process 2039, UID 498, (beam.smp) total-vm:43235412kB,
> anon-rss:23187940kB, file-rss:4kB

-   /etc/init.d/rabbitmq-server stop; /etc/init.d/rabbitmq-server start

-   File a Trello card under Production Ops Issues so we can deep dive
    resource usage

    -   Attach graphs from memory graph and link to node monitoring in
        Z-console. Look under this device
        class: <http://10.128.131.100:8080/zport/dmd/itinfrastructure#devices:.zport.dmd.Devices.Server.SSH.Linux.RABBIT>

    -   Attach dmesg output relevant to the OOM killer

-    

**ISSUE 4: rabbitmq process died for some reason**

-   If \`dmesg\` does not show that OOM killer killed it, create a
    Trello card under Production Ops Issues so we can deep dive

#### **Problem: \[GLOBAL Z-CONSOLE\] HTTP CRITICAL: HTTP/1.1 500 Internal Server Error **

** **\
**Cause: **

This is from the inventory HTTPMonitor on the Z-Console:
<http://10.128.131.100:8080/zport/dmd/Devices/Endpoint/Critical_Endpoint/devices/VA1ZGPZCONSOL02/devicedetail#deviceDetailNav:device_overview>

The CouchDB service may not be reachable. 

**Solution:**

1.  [COUCHDB-relatedconnectionrefused(aborted)errors](#CTLZenossIncidentResponseRecipes-COUCHD)

**Note:**

> \[GLOBAL Z-CONSOLE\] **10.128.131.202** HTTP CRITICAL: HTTP/1.1 500
> Internal Server Error
>
>  If va1-znode16 is being replaced, this can be ignored. but it should
> clear once the node (znode16) is in service

** **

**Problem: \[VA1ZGPCOUCHDB\] Connection refused HTTP CRITICAL - Unable
to open TCP socket**

** **\
**Cause: **

This is from the HTTPMonitor on the CouchDB device: 
<http://10.128.131.100:8080/zport/dmd/itinfrastructure#devices:.zport.dmd.Devices.Server.SSH.Linux.COUCHDB>

**Solution:**

1.  [COUCHDB-relatedconnectionrefused(aborted)errors](#CTLZenossIncidentResponseRecipes-COUCHD)

**Problem: &lt;NODE&gt; is missing**\
** **\
**Sample event : **IL1 Z-NODE07 is missing\
\
**Solution:**

1.  The correct recipe is to run drain.l against this node to move
    workload away from it.  The above flapping is usually caused by an
    overloaded Z-Node. Frequency = alerts more than twice, e.g. it
    alerts, clears, alerts again.

2.  If it only happens once, ignore it, but if you see the same node
    throwing any sort of repeating / flapping errors, drain.l should be
    the first thing to try (to move workload away from it) many of the
    things that cause those flapping alarms are ultimately due to the
    node being overloaded drain.l tries to move work away from that
    z-node to other ones in the same z-group.  There are certain types
    of workload that it will not attempt to move, because they are
    special cases, so don't expect it to completely drain all work from
    the node - just most of it.

#### Problem: Threshold of Free Swap Not Met

**Validation: **

An similar alert is received :

NY1R8RC2ZGPZMASTER: threshold of Free Swap not met: current value
1806336.000000\
\[GLOBAL Z-CONSOLE\] "threshold of Free Swap not met: current value
1806336.000000"

**Cause:**

Multiple causes but basically this is a high memory usage event stealing
a lot of swap space

**Solution:**

1.  Use drain and mover script to alleviate the workload - [HOWTO :
    Reduce the workload on a running Z-Node by
    rebalancing](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-HOWTO:ReducetheworkloadonarunningZ-Nodebyrebalancing)

2.  SSH to the znode. Check if swap and memory usage decreases.

3.  If alert persists, proceed vertical scaling and replacing the znode.

    1.  You can add RAM and/or cores on a per-node-basis here:
        <https://zen.mon.ctl.io/docs/#!/Node/setSpecification>

    2.  After doing so, please force node replacements via
        <https://zen.mon.ctl.io/docs/#!/Node/replace> and make sure the
        replacements are successful.

**Verification:**

Alerts should clear within 5 minutes. Escalate to CTL team if issue
persist

***Outdated solution below for reference.***

~~1) Login to the instance and decrease the "swappiness" value. The
default is 60, we set it to 1~~\
~~\# cat /proc/sys/vm/swappiness~~\
~~60~~

~~\# sysctl vm.swappiness=1~~\
~~vm.swappiness = 1~~

~~Verify the change:~~\
~~\# cat /proc/sys/vm/swappiness~~\
~~1~~

**~~(Steps below are optional if you want to start with a clean
swap.)~~**

~~2) Create a temporary swap file and add it to the server~~\
~~\# fallocate -l 2G /tempswap.swap~~\
~~\# mkswap /tempswap.swap~~\
~~\# swapon /tempswap.swap~~

~~3) Stop the default swap file (hint: use \`swapon -s\` to check which
is the default swap file)~~\
~~\# swapoff /dev/sdb~~

~~Verify that "swap" is decreasing and "free mem" should also decrease.
The process will end when "used swap" is zero~~

~~\# free~~\
~~total used free shared buffers cached~~\
~~Mem: 32876496 28894636 3981860 3873276 125732 6110424~~\
~~-/+ buffers/cache: 22658480 10218016~~

~~Swap: 1890904 1890904 0~~

~~(hint: you can also use \`swapon -s\` to check if the swap used is
being drained from the swap being removed. swapoff also takes a few
moment to perform)~~

~~3.A) There are cases when the what is being offloaded in swap cannot
fit into memory (if used swap is greater than free mem) so we
temporarily offload memory by restarting zenoss. Open another terminal
session and restart zenoss while swapoff is running.~~

~~\# /etc/init/zenoss.sh stop~~\
~~\# /etc/init/zenoss.sh start~~

~~4) Reformat the default swap partition that was removed before and add
again as a swap file.~~\
~~\# mkswap /dev/sdb~~\
~~\# swapon /dev/sdb~~

~~5) Remove and delete the temporary swap file created.~~\
~~\# swapoff /tempswap.swap~~\
~~\# rm /tempswap.swap~~

~~If swap alert has cleared, you can just make sure swappiness is set to
1. A patch will be pushed to ctl soon that will already have set this.~~

#### Problem: \[MISSING\] **&lt;SOME INDIVIDUAL DEVICE&gt; hasn't checked in**

Example alert: 

-   \[MISSING\] il1-vc-std05.t3n.dom-vsphere hasn't checked in
    - <https://cascadeo.zendesk.com/agent/tickets/410752>

**Triage steps**

1.  Verify in Kibana / Elasticsearch that the performance data of the
    device is missing.\
    Modify this [saved
    search](https://kibana-cascadeo.analytics.ctl.io/goto/fe94e30b5bcfee64a03269b440276bf9).
    Replace the device in the filter. Modify the time range to zoom in /
    out.\
    \
    ![C:\\074168bd3786d4792846efe8005a4ee5](media/image43.tmp){width="4.875in"
    height="2.3854166666666665in"}\
    \
    Example: this saved search shows when the performance data started
    to go missing

2.  There are three options to track down which z-node is monitoring a
    device.

    1.  Option 1: Checking the manifest. There is a listing in the
        manifest of devices monitored by a z-node.

    2.  Option 2: Use GET /devices/{dc}/{name} in z-api.\
        \
        ![C:\\0e9572f1d7e45d87c824da514ab9e94b](media/image44.tmp){width="4.875in"
        height="2.4583333333333335in"}

    3.  Option 3: Use zen.mon.ctl.io proxy

        1.  Find the \*-vsphere
            device in *http://10.128.131.100/proxy/&lt;REPLACE WITH
            DESIRED
            DATACENTER&gt;* (e.g. <http://10.128.131.100/proxy/VA1>). Note
            which z-node is monitoring the device. *If it is in ZMASTER,
            you need to wait because monitoring failed over. You can
            verify by [tracking down the z-node assigned to it using the
            manifest](https://docs.google.com/presentation/d/1JjyovfWh-3CrbxURIzPgk0ySEKkvnVPxH6OY1hnhEAw/edit?pli=1#slide=id.g1a8ba7d27b_0_0).
            Most probably the z-node is being replaced. If you notice
            that this behavior (failover to zmaster, z-node assigned
            replaced persistently) is persistent, create a Prod Ops
            Issue card in Trello and assign to Peter (CC Prem & Jared).*

        2.  Find out the production state of the device. If it
            is *non-production* (first column is *not* colored green),
            ignore it. If in production state, click the device. \
            \
            \
            Figure: ny1t3nvc01.t3n.dom-event is monitored by z-node
            NY1R82ZGPZNODE04\
            \
            \
            \
            Figure: devices in production and non-production states

        3.  It will redirect to the page of the device in the zenoss
            node. Go to Graphs. The Events Graph should be populated
            with values.

3.  Possible issues:

    1.  **Device not modeled**

> The Device Overview should show that the Modeled Time is "Not
> Modeled". Attempt to model and report as a Prod Ops issue any modeling
> errors.
>
> Run zenmodeler in the command line to allow long-running modeling.
>
> SSH to the z-node. You can use \`screen\` to survive disconnection
> issues or terminal buffer overload.
>
> \# screen
>
> \# su - zenoss
>
> Example: (replace device below)
>
> \$ zenmodeler run -v10 -d va1-vc-f01.t3n.dom-vsphere
>
> (Ctrl+A+D if you want to detach)
>
> To re-attach, (example below)
>
> \[root@VA1R82ZGPZNODE22 \~\]\# screen -list\
> There is a screen on:\
> 13950.pts-0.VA1R82ZGPZNODE22 (Detached)\
> 1 Socket in /var/run/screen/S-root.\
> \[root@VA1R82ZGPZNODE22 \~\]\# screen -r 13950
>
> (The lost connection log like below is expected in most cases if you
> see it after the line INFO zen.ZenModeler: Daemon ZenModeler shutting
> down)
>
> 2016-12-11 07:45:12,312 DEBUG zen.pbclientfactory: Lost connection to
> 127.0.0.1:8789 - \[Failure instance: Traceback (failure with no
> frames): &lt;class 'twisted.internet.error.ConnectionLost'&gt;:
> Connection to the other side was lost in a non-clean fashion:
> Connection lost.\
> \]\
> 2016-12-11 07:45:12,313 DEBUG zen.collector.scheduler: In shutdown
> stage during\
> 2016-12-11 07:45:12,313 DEBUG zen.collector.scheduler: In shutdown
> stage after
>
> Example of a modeling issue
>
> 2016-08-09 04:50:57,324 ERROR zen.python: ca1t3nvc01.t3n.dom-vsphere
> 300 vsphere-cluster-metrics unhandled plugin error:
> (vmodl.RuntimeFault) {\
> dynamicType = &lt;unset&gt;,\
> dynamicProperty = (vmodl.DynamicProperty) \[\],\
> msg = "This operation is restricted by the administrator -
> 'vpxd.stats.maxQueryMetrics'. Contact your system administrator.",\
> faultCause = &lt;unset&gt;,\
> faultMessage = (vmodl.LocalizableMessage) \[\]\
> }

1.  **zeneventserver failed to start in the z-node**\
    **\
    **You should see the z-node reported in the panel [MONIT ALERT:
    zeneventserver failed to start](https://goo.gl/JERC9E).\
    \
    \
    \
    This is still an issue under investigation. Report as a Prod Ops
    Issue in Trello cc Peter Y. It is similar
    to <https://trello.com/c/sQcpmAh3/3056-ny1r82zgpznode06-that-monitors-ny1t3nvc01-t3n-dom-vsphere-has-unusually-high-zenhub-memory-usage>

2.  **Collection failed over to ZMASTER**

    1.  If the device collection failed over to ZMASTER, check if the
        device is already modeled

    2.  ZMASTER can become overloaded and the OOM killer can kill the
        collector daemons (zenpython, zenperfsnmp, etc..). You can check
        the following for any signs of OOM and which daemon was killed.
        You can start the daemon that was killed. If it is persistently
        being killed by OOM killer, [you can increase ZMASTER
        memory](https://goo.gl/so2ryW) by +4GB.

        1.  dmesg

        2.  syslog

        3.  \# /etc/init.d/zenoss status

3.  **Something is wrong during collection**

    1.  You can try to manually invoke collection to see if there are
        errors. Example of a collection of a vSphere:

    2.  To manually invoke collection, run zenoss command as user and
        use the command zenpython run -d &lt;device\_name&gt;. The
        output should be very long which indicates that it is collecting
        okay. After the run is completed, exit in the zenoss command and
        check if /opt/zenoss/var/zenpython.blocked exist (\$cat
        /opt/zenoss/var/zenpython.blocked).

    3.  \[root@UT1R8RC2ZGPZNODE01 \~\]\# su - zenoss

    4.  \[zenoss@UT1R8RC2ZGPZNODE01 root\]\$ zenpython run -d
        &lt;device\_name&gt;

    5.  6.  2016-04-20 10:51:13,638 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx03.t3n.dom

    7.  2016-04-20 10:51:13,887 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx20.t3n.dom

    8.  2016-04-20 10:51:13,887 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx20.t3n.dom

    9.  2016-04-20 10:51:14,128 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx05.t3n.dom

    10. 2016-04-20 10:51:14,128 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx05.t3n.dom

    11. 2016-04-20 10:51:14,383 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nmgmtesx01.t3n.dom

    12. 2016-04-20 10:51:14,383 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nmgmtesx01.t3n.dom

    13. 2016-04-20 10:51:14,628 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx07.t3n.dom

    14. 2016-04-20 10:51:14,629 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx07.t3n.dom

    15. 2016-04-20 10:51:14,869 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx19.t3n.dom

    16. 2016-04-20 10:51:14,869 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx19.t3n.dom

    17. 2016-04-20 10:51:15,132 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx09.t3n.dom

    18. 2016-04-20 10:51:15,132 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx09.t3n.dom

    19. 2016-04-20 10:51:15,378 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx22.t3n.dom

    20. 2016-04-20 10:51:15,378 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx22.t3n.dom

    21. 2016-04-20 10:51:15,630 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx21.t3n.dom

    22. 2016-04-20 10:51:15,631 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx21.t3n.dom

    23. 2016-04-20 10:51:15,879 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx04.t3n.dom

    24. 2016-04-20 10:51:15,880 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx04.t3n.dom

    25. 2016-04-20 10:51:16,121 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx25.t3n.dom

    26. 2016-04-20 10:51:16,122 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx25.t3n.dom

    27. 2016-04-20 10:51:16,383 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx06.t3n.dom

    28. 2016-04-20 10:51:16,383 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx06.t3n.dom

    29. 2016-04-20 10:51:16,635 INFO zen.vSphereHostMetrics: vSphere
        host in Connected state. Collecting metrics for
        ut1t3nesx01.t3n.dom

    30. 2016-04-20 10:51:16,635 INFO zen.vSphereHostMetrics: Host
        metrics collected through API for ut1t3nesx01.t3n.dom

    31. 2016-04-20 10:51:29,411 INFO zen.zenpython: 1 devices processed
        (17275 datapoints)

    32. 2016-04-20 10:51:29,411 INFO zen.collector.scheduler: Tasks: 10
        Successful\_Runs: 9 Failed\_Runs: 0 Missed\_Runs: 0
        Queued\_Tasks: 0 Running\_Tasks: 1

    33. 2016-04-20 10:51:29,413 INFO zen.zenpython: Daemon
        CollectorDaemon shutting down

    34. 35. \[root@UT1R8RC2ZGPZNODE01 \~\]\# cat
        /opt/zenoss/var/zenpython.blocked

> cat: /opt/zenoss/var/zenpython.blocked: No such file or directory

1.  If the file “zenpython.blocked” doesn’t exist, it means the
    collection run is okay. If the file exist, open it with a text file
    and see what zenpython stuff is blocked (e.g. vsphere collectors).
    Then, you can either empty the file or delete the zenpython.blocked
    file. Then restart zenpython daemon.

<!-- -->

1.  **ZNODE runs out of memory**\
    You can check the following for any signs of OOM and which daemon
    was killed. You can start the daemon that was killed. If it is
    persistently being killed by OOM killer, you can [increase the
    memory](https://goo.gl/so2ryW) by +4GB.

    1.  dmesg

    2.  syslog

    3.  \# /etc/init.d/zenoss status

<!-- -->

1.  Create a Prod Ops issue card in Trello if the issue persists. Update
    this incident recipe for errors with discovered solution. 

#### Problem: \[MISSING\] &lt;Datacenter&gt; \*-vsphere Message Volume hasn't checked in

Example alert:

-   \[MISSING\] UT1 \*-vsphere Message Volume hasn't checked in -
    <https://cascadeo.zendesk.com/agent/tickets/184757>

Cause:

-   The error may due to the zenpython patch that blocks collection runs
    that hog the zenpython daemon

-   zenpython is killed by Out-of-memory (OOM) killer

-   zenpython collector is too busy or overloaded

-   The device is not modeled (until the next modeling period)

-   Other causes are still under investigation.

Steps:

-   SSH to the Zconsole to check the output of the script that monitors
    the message volume of vSphere devices.\
    Example:

\# /usr/bin/python /usr/local/bin/es-monitor-vsphere-devices.py -s
http://10.128.131.220:4984/zenoss\_databag/

Checking ES message volumes in all vsphere devices.

Execution Start Time: 2016-07-21 14:51:00

WARNING!! The ff. devices are exempted from alerting.

\['ny1-vc-std03.t3n.dom-vsphere', 'ny1-vc-std03.t3n.dom-event'\]

sg1-vc-std03.t3n.dom-vsphere mcount=5735 OK

\[CRITICAL\] No messages found for device sg1-vc-hpc01.t3n.dom-vsphere

sg1-vc-std02.t3n.dom-event mcount=12 OK

sg1-vc-std03.t3n.dom-event mcount=12 OK

sg1-vc-std02.t3n.dom-vsphere mcount=6251 OK

Skipping sg1-vc-std01.t3n.dom-vsphere, device is not in Production
state(300)

sg1-vc-std01.t3n.dom-event mcount=12 OK

sg1-vc-m01.t3n.dom-vsphere mcount=1444 OK

sg1-vc-hpc01.t3n.dom-event mcount=12 OK

\[CRITICAL\] No messages found for device sg1-vc-m01.t3n.dom-event

\[NOT-OK\] Issues found in MANIFEST\_SG1\_R82\_ZGP devices.

 

...

Notice the line: 

\[CRITICAL\] No messages found for device sg1-vc-hpc01.t3n.dom-vsphere

-   You can use this recipe to triage individual -vsphere
    devices: [Problem: \[MISSING\] &lt;SOME INDIVIDUAL DEVICE&gt; hasn't
    checked in](https://goo.gl/tidGEI)

#### Problem: \[MISSING\] &lt;Datacenter&gt; \*-event Message Volume hasn't checked in

This recipe is similar to the above recipe on \*-vsphere message volume
hasn't checked in.

You can use this recipe to triage individual -vsphere devices: [Problem:
\[MISSING\] &lt;SOME INDIVIDUAL DEVICE&gt; hasn't checked
in](https://goo.gl/tidGEI)

#### Problem: \[MISSING\] ESMsgVolume &lt;Datacenter&gt; hasn't checked in

#### 

The script that ping these DMS endpoints is in Z-console.

/usr/bin/python /usr/local/bin/es-monitor-vsphere-devices.py -s
http://10.128.131.220:4984/zenoss\_databag/

The script shows a summary of the datacenters with critical message
counts.

The ff. devices have CRITICAL message counts:

In UC1:

\[CRITICAL\] No messages found for device uc1-vc-hpc-a01.t3n.dom-event
(UC1R82ZGPZNODE09)

\[CRITICAL\] No messages found for device uc1-vc-d01.t3n.dom-event
(UC1R82ZGPZNODE04)

In SG1:

\[CRITICAL\] No messages found for device sg1-vc-m01.t3n.dom-event
(SG1R82ZGPZNODE01)

In GB3:

\[CRITICAL\] No messages found for device gb3-vc-hpc-a03.t3n.dom-vsphere
(GB3R82ZGPZNODE04)

In DE1:

\[CRITICAL\] No messages found for device de1-vc-std04.t3n.dom-event
(DE1R82ZGPZNODE05)

\[CRITICAL\] No messages found for device de1-vc-std03.t3n.dom-vsphere
(DE1R82ZGPZNODE04)

In VA2:

\[CRITICAL\] No messages found for device va2-vc-m01.t3n.dom-vsphere
(VA2R82ZGPZNODE04)

In VA1:

\[CRITICAL\] No messages found for device va1-vc-a01.t3n.dom-event
(VA1R82ZGPZNODE02)

\[CRITICAL\] No messages found for device va1-vc-a02.t3n.dom-event
(VA1R82ZGPZNODE02)

\[CRITICAL\] No messages found for device va1-vc-hpc-c03.t3n.dom-event
(VA1R82ZGPZNODE20)

\[CRITICAL\] No messages found for device va1-vc-f01.t3n.dom-event
(VA1R82ZGPZNODE18)

In IL1:

\[CRITICAL\] No messages found for device il1t3nvc01.t3n.dom-event
(IL1R82ZGPZNODE06)

\[CRITICAL\] No messages found for device il1-vc-std03.t3n.dom-event
(IL1R82ZGPZNODE06)

\[CRITICAL\] No messages found for device il1-vc-a02.t3n.dom-vsphere
(IL1R82ZGPZNODE02)

\[CRITICAL\] No messages found for device il1-vc-std05.t3n.dom-vsphere
(IL1R82ZGPZNODE02)

\[CRITICAL\] No messages found for device il1-vc-m01.t3n.dom-vsphere
(IL1R82ZGPZNODE02)

In WA1:

\[CRITICAL\] No messages found for device wa1-vc-hpc-a01.t3n.dom-event
(WA1R82ZGPZNODE01)

**Solution:**

1.  Triage each device.

    1.  If it is a -vsphere device, follow the triage steps in [Problem:
        \[MISSING\] &lt;Datacenter&gt; \*-vsphere Message Volume hasn't
        checked in](https://goo.gl/PVi4Ge)

    2.  If it is a -event device, follow the triage steps in [Problem:
        \[MISSING\] &lt;Datacenter&gt; \*-event Message Volume hasn't
        checked in](https://goo.gl/7eEVvc)

2.  Make sure a Prod Ops Issue Trello card exists for each datacenter

    1.  Find out if there is already an existing card by searching in
        Trello. Try searching using one of the devices or the DMS ID.
        Example: in the
        URL <https://deadmanssnitch.com/snitches/f214ecfc16/setup> the
        ID is f214ecfc16.

    2.  If there is no card yet, for each datacenter create a Prod Ops
        Issue card and prefix the title with the ID of the DMS. (For now
        assign to Jared & Prem. More steps to follow.)

    3.  Point out if the device has a recurring collection issue. (Feel
        free to create a separate card highlighting the device and the
        noticed recurring issue)

#### Problem: This operation is restricted by the administrator - 'vpxd.stats.maxQueryMetrics'. Contact your system administrator

**Symptom:** The following error is encountered when modeling a -vsphere
or -event device:

2016-11-18 02:45:53,451 ERROR zen.python: gb3-vc-a02.t3n.dom-vsphere 300
vsphere-cluster-metrics unhandled plugin error: (vmodl.RuntimeFault) {

dynamicType = &lt;unset&gt;,

dynamicProperty = (vmodl.DynamicProperty) \[\],

msg = "This operation is restricted by the administrator -
'vpxd.stats.maxQueryMetrics'. Contact your system administrator.",

faultCause = &lt;unset&gt;,

faultMessage = (vmodl.LocalizableMessage) \[\]

}

**Solution:**

This requires CTL NOC intervention. Create a ticket regarding this
issue. You can refer to <https://t3n.zendesk.com/agent/tickets/1303422>
for the ticket template. Once CTL NOC confirmed that the issue is fixed,
re-model the device again and verify that the error is gone.

#### Problem: \[MISSING\] ESMsgVol Exemption List hasn't checked in

#### 

This DMS endpoint is activated (not pinged) when the script
in https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes\#CTLZenossIncidentResponseRecipes-Problem:\[MISSING\]ESMsgVolume&lt;Datacenter&gt;hasn'tcheckedin has
something in its exemption list. The exemption list is
in /usr/local/bin/vsphere-exemption-list.txt.

The exemption list looks like this:

device1.name1.example This first device is not be ignored.\
device2.name2.example The rest of the texts after the dev\_name are
considered as comments.

Normally, the exemption list should be empty.

This alert is a placeholder that some device/s (with prod state = 1000)
are in the exemption list.

**Action:** Just create a Trello card for Prem to track down the
monitoring status of the devices in the exemption list.

#### Problem:\[GLOBAL Z-CONSOLE\] &lt;COUCHDB\_SERVER&gt; threshold of Greater than 40 percent used not met: current value XXXX on /home/couchdb mountpoint

**Symptom:** disk usage alert for Couchdb on mountpoint /home/couchdb
(see sample: <https://cascadeo.zendesk.com/agent/tickets/122937>)

Note: CouchDB currently has ip of 10.128.131.68 and 10.128.131.79. This
may change so check http://control.ctl.io if ever. 

**Solution: **

1.  SSH into server and check disk space if indeed already exceeded
    threshold. (df -h). Threshold as of 05/05/2016 is 40% disk
    utilization.

2.  If disk usage is above threshold, remove the server from load
    balancer rotation (10.128.131.22). Do this one server at a time.

    1.  To disable the load balancer from the rotation edit the LB
        config and set 'active = 0' for the couchdb you will be working
        on (In this example, couch01 was disabled)

> \[root@VA1ZGPPROXYLB01 \~\]\# vi /etc/sysconfig/ha/lvs.cf\
> ...\
> virtual COUCHDB {\
> active = 1\
> \*\*\* snipped \*\*\*\
> server VA1ZGPCOUCHDB01 {\
> address = 10.128.131.68\
> active = 0\
> weight = 1\
> }\
> server VA1ZGPCOUCHDB02 {\
> address = 10.128.131.79\
> active = 1\
> weight = 1\
> }\
> }\
> ...
>
> \[root@VA1ZGPPROXYLB01 \~\]\# service pulse restart
>
> \[root@VA1ZGPPROXYLB01 \~\]\# ipvsadm -l\
> \*You should see that the disabled load couchdb is out of rotation

1.  Adjust size of /home/couchdb partition of the couchdb node in
    question via Control Portal.

2.  Wait for the changes to take into effect.

3.  Verify. Inspect http://&lt;ip&gt;:5984/\_utils and
    /var/log/messages.

#### Problem: \[GLOBAL Z-CONSOLE\] VA1ZGPPROXY01/02 Connection Refused

**Symptom**: zenoss-inventory on the server has stopped responding. This
can be seen on z-console as an event and confirmed by checking the log
in /var/log/zenoss-inventory.log

**Solution**:

1.  SSH into the server.

2.  Check the zenoss-inventory log in /var/log and note any potential
    issue. It will state here if daemon is down.

3.  Perform a stop of the zenoss-inventory daemon (service
    zenoss-inventory stop). Check if there are orphaned processes via ps
    -aux | grep node

4.  Perform a start of the zenoss-inventory daemon (service
    zenoss-inventory start).

5.  Also
    see [COUCHDB-relatedconnectionrefused(aborted)errors](#CTLZenossIncidentResponseRecipes-COUCHD) if
    the app keeps crashing due to couchdb.

#### Problem: \[GLOBAL Z-CONSOLE\] XXXX HTTP WARNING: HTTP/1.1 404 Not Found

**Symptom**: This alert is triggered whenever VA1 Z-Node 08 is being
replaced. \
**Solution**:

1.  Wait for the VA1 Z-Node 08 replacement to finish.

2.  Escalate to Jerome if this alert occurs without an ongoing
    replacement of VA1 Z-Node 08.

#### Problem: \[GLOBAL Z-CONSOLE\] VA1ZGPWEB0X/0Y threshold of API\_Proxy not met: current value -2000.000000

**Solution**:

1.  Verify the error by going to <http://10.128.131.202:8080/proxy> and
    clicking any device (preferably one with an active Z-Node).This will
    redirect to the proxy app (VIP: 10.128.131.202)

2.  Change the URL to whichever proxy server is affected (10.128.131.47
    or 10.128.131.48). If the connection is refused, then the z-webui
    service might not be running.

3.  Do the following to restart the service:

    1.  SSH to the instance and run /etc/init.d/pm2-init.sh restart

    2.  Verify:

> Status for pm2:\
> ┌──────────┬────┬──────┬──────┬────────┬─────────┬────────┬──────────────┬──────────┐\
> │ App name │ id │ mode │ pid │ status │ restart │ uptime │ memory │
> watching │\
> ├──────────┼────┼──────┼──────┼────────┼─────────┼────────┼──────────────┼──────────┤\
> │ z-webui │ 0 │ fork │ 5655 │ online │ 14 │ 2D │ 411.145 MB │ enabled
> │\
> └──────────┴────┴──────┴──────┴────────┴─────────┴────────┴──────────────┴──────────┘
>
> Verify that the log is moving:

1.  pm2 logs

<!-- -->

1.  Repeat step 2 to confirm that the URL is working. The alert should
    clear by this point.

2.  Also
    see [COUCHDB-relatedconnectionrefused(aborted)errors](#CTLZenossIncidentResponseRecipes-COUCHD)

#### **Problem: Found orphaned node &lt;hostname&gt; (&lt;ip&gt;) in &lt;DC&gt;**

#### Problem: Found IP address (&lt;ip&gt;) in &lt;DC&gt; with unknown hostname.** **

**Cause: **

An possible orphaned znode was found in the datacenter. Because the
monitor relies on snmp to guess the hostname of a node, an alert may be
generated for new non-znode instance.

**Solution:**

1.  Login to ZGP Control Portal and find the instance in the datacenter
    in question.

2.  Check if host is a:

    1.  **new node replacement**:

        1.  wait for the replacement process to finish. Manually close
            the event in zconsole and ticket in zendesk after successful
            replacement.

    2.  **node being replaced:**

        1.  wait for the replacement process to finish. Provisioner will
            automatically delete the node if replacement process was
            successful. If the replaced node was not deleted, proceed to
            step 2.c.

    3.  **failed node replacement**:

        1.  delete the machine manually in control portal.  Manually
            close the event in zconsole and ticket in zendesk.

    4.  **znode or master that is NOT VISIBLE or in STUCK in Control
        Portal**: 

        1.  Try to SSH in to the instance using the standard znode
            password or key.

        2.  The hostname should give you hint about the instance. If it
            is a znode, or master (usually has ZNODE, ZMASTER, RABBIT
            keyword in its hostname), it is probably an orphaned
            instance. Stop the instance by executing the following:
            **chkconfig zenoss off; chkconfig supervisor off; halt**.
            There were times that instances kept running even though
            they were already deleted from Control Portal. This step
            will ensure that zenoss and supervisor will not run if they
            are rebooted. Additionally, request CTL Support
            <help@ctl.io> to delete the instance.

        3.  If you are unable to SSH in to the host OR if the host is
            NOT a znode or master: Create a ticket in Cascadeo Zendesk
            for CTL ops team to identify the instance and add the IP
            address to ignore list if needed (see step 2.f). 

    5.  **znode, master that is VISIBLE and NOT STUCK in Control
        Portal**:

        1.  Verify that the instance is a znode, or master. If so,
            delete the instance manually in Control Portal.

    6.  **production device other than znode, master**:

        1.  Add the IP address to the ignore list in OrphanZNodeMonitor
            template (Z-Console &gt; Advanced &gt; Monitoring Template).
            Ensure that the IP address is added to the correct
            datacenter.

        2.  Add the device to Z-Console IF it needs to be monitored.

    7.  **NOT Orphan Node. **

        1.  There are times that active nodes are flagged as orphaned
            when state DB does not have IP address of the active znode.
            This is a provisioner bug and should be reported to
            provisioner code owner (jerome@cascadeo.com). Non-urgent
            unless it affects production.

    8.  **NOT any of the above**: Create a ticket in Cascadeo Zendesk
        for CTL ops team to identify the instance and add the IP address
        to ignore list if needed. Non-urgent. (see step 2.f for adding
        the IP address to ignore  list).

#### HOWTO: Identifying a CTL Event Storm

**Symptom**: Most connectio

**Steps**:

1.  Check the event count of the Z-Trap nodes in the Z-Console
    (Events &gt; EvConsole). An unusually high number of events may be
    seen, typically greater than 5000. This equates to a throughput
    greater than 5 messages per second. 

2.  Check Kibana

    1.  Click on the affected datacenter under Total Message Volume
        by DC.

    2.  Scroll down to Total Zenoss Events by Node and click on a Z-Trap
        node (UC1 Z-Trap 01 in this example).

    3.  Scroll all the way down to All Messages and click on the blue
        tile with the arrow to expand the menu. Look for
        header.messageType on the left-hand side and click on it, select
        Terms, then Bar. This will display a bar graph. Click on
        zenossEvent.\
        \
        \
          

    4.  The left-hand side menu will have more entries. Look for
        zenossEvent.device, click on it, select Terms, then Bar. This
        will pull up a bar graph of the 10 devices which have the most
        Zenoss events. Click on the device with the most events (usually
        the leftmost one).\
           

    5.  Go back to the Total Message Throughput by DC graph at the top.
        An event storm will usually display spikes and/or other
        abnormalities in the graph which will coincide with the time
        when the repeated provisioning is happening.

    6.  Repeat steps b-e for the other Z-Trap node. 

>                    

3. Send the findings (screenshots, timelines, which Z-nodes, counts,
samples of events that you can see from Zenoss event console) to
<ctl@cascadeo.com> so it can be correlated to other events. 

**UPDATE**: There is a new graph in Kibana (Trap Messages Throughput by
DC) which makes it easier to determine if there is an event (traps)
storm. Notice the UC1 storm in this example:

 

#### HOWTO: Get to a znode monitoring a certain device

-   Check the device name (e.g.ut1-vc-01.t3n.dom-vsphere) in
    <http://10.128.131.100/inventory>. It is a link that brings you
    directly to the znode that is monitoring the device (with some
    component and graphing). Credentials is in LP → CTL Zenoss Instances

 

#### HOWTO: Enabling -ops (one packet scheduling) on the ZGP load balancer (ipvsadm)

**Symptom**: As per investigation of a ztrap issue (on UC1,
<https://trello.com/c/jaaznjz2>), it was discovered that the trap/syslog
events seem to be not distributed to the ztrap nodes. This is evident
when most of the syslogs are just received by one of the ztrap node even
though the other one is also up. As per
<http://serverfault.com/questions/503211/per-packet-round-robin-load-balancing-for-udp>,
it seems that UDP packets (such as syslog, and SNMP traps) coming from a
single source (e.g SRX device) will only send all its packets (syslogs,
etc) to only one real server (ztrap node), regardless if there's another
one available. To avoid this issue, it was suggested to enable the
'-ops' parameter of ipvsadm. Enabling it is not that straightforward
since the lvs.cf configuration file doesn't support the said parameter.
Below are the steps to enable -ops:

**Steps**:

1.  Restart the 'pulse' service if there's an update on the lvs.cf
    configration: ***service pulse restart***

2.  /etc/init.d/ipvsadm save to save the LVS table
    to /etc/sysconfig/ipvsadm

3.  Once the services are running, modify the /etc/sysconfig/ipvsadm
    file so it will look like this:  

> -A -t 10.121.186.200:8080 -s rr
>
> -a -t 10.121.186.200:8080 -r 10.121.186.13:8080 -g -w 1
>
> -a -t 10.121.186.200:8080 -r 10.121.186.31:8080 -g -w 1
>
> **-A -u 10.121.186.200:162 -s wrr -o**
>
> -a -u 10.121.186.200:162 -r 10.121.186.13:162 -g -w 1
>
> -a -u 10.121.186.200:162 -r 10.121.186.31:162 -g -w 1
>
> **-A -u 10.121.186.200:514 -s wrr -o**
>
> -a -u 10.121.186.200:514 -r 10.121.186.13:514 -g -w 1
>
> -a -u 10.121.186.200:514 -r 10.121.186.31:514 -g -w T
>
> Take note of the **'-o'** option on the VIP lines

1.  Restart the /etc/init.d/ipvsadm service\
    \
    /etc/init.d/ipvsadm restart

> ipvsadm: Clearing the current IPVS table: \[ OK \]
>
> ipvsadm: Unloading modules: ip\_vs \[FAILED\]
>
> ipvsadm: Clearing the current IPVS table: \[ OK \]
>
> ipvsadm: Applying IPVS configuration: \[ OK \]
>
> 4:26
>
> ipvsadm: Applying IPVS configuration: \[ OK \] ← THIS SHOULD BE OK!
>
> You can ignore the Failed status on 'Unloading modules: ip\_vs'.
> However, make sure that 'Applying IPVS configuration' is OK

1.  If the configuration is good, the ipvsadm table (\`ipvsadm -L\`)
    should look like this:

> IP Virtual Server version 1.2.1 (size=4096)
>
> Prot LocalAddress:Port Scheduler Flags
>
> -&gt; RemoteAddress:Port Forward Weight ActiveConn InActConn
>
> TCP 10.121.186.200:webcache rr
>
> -&gt; 10.121.186.13:webcache Route 1 0 6
>
> -&gt; 10.121.186.31:webcache Route 1 0 6
>
> **UDP 10.121.186.200:snmptrap wrr *ops***
>
> -&gt; 10.121.186.13:snmptrap Route 1 0 42
>
> -&gt; 10.121.186.31:snmptrap Route 1 0 1
>
> **UDP 10.121.186.200:syslog wrr *ops***
>
> -&gt; 10.121.186.13:syslog Route 1 0 1
>
> -&gt; 10.121.186.31:syslog Route 1 0 0\
>  \
> Notice the 'ops' on the VIP address line. This means that 'ops' is
> enabled for the said VIP.

1.  Verify the events in the ztrap nodes if they are distributed. The
    ztrap nodes should more or less have events coming from the same
    device. This means that the source of events is not tied anymore to
    a specific real server (ztrap node).

#### ** **COUCHDB-related connection refused (aborted) errors

#### ** Symptom**: Most connection refused errors from Z-Console are due to CouchDB being out of service. The following assets or systems use CouchDB:

-   ZenPacks.CTL.ZNodeMonitor ZenPack - for orphaned nodes monitoring,
    rrd monitor, modeling time monitor

    -   ZenPacks.CTL.ZNodeMonitor/OrphanZNodeMonitor/OrphanedZnodeMonitor -
        NY1 Error: &lt;class 'requests.exceptions.ConnectionError'&gt;
        ('Connection aborted.', error(111, 'Connection refused')).

-   Provisioners - pushes znode, device information to couchdb

    -   Provisioner SG1R8RC2ZGPPROVISIONER: ('Connection aborted.',
        error(111, 'Connection refused')

    -   HTTPError: 500 Server Error: Internal Server Error\
        File "/home/zenoss/zcomms/heartbeat/heartbeat.py", line 1217, in
        get\_devices\
        r.raise\_for\_status()\
        File "/usr/lib/python2.6/site-packages/requests/models.py", line
        808, in raise\_for\_status\
        raise HTTPError(http\_error\_msg, response=self)\
        HTTPError: 500 Server Error: Internal Server Error

-   Global Proxy - fetches znode, device information from couchdb

-   Zenoss API - fetches znode, device information from couchdb** **

[*\
**Solution:***](https://trello.com/c/hcXGv6Bz)

1.  Retrieve the IP of the CouchDB instance from the Z-Console
    - <http://10.128.131.100:8080/zport/dmd/itinfrastructure#devices:.zport.dmd.Devices.Server.SSH.Linux.COUCHDB>

2.  SSH and check the status of CouchDB service. The output should be
    similar to the example below

> \[root@VA1ZGPCOUCHDB06 \~\]\# systemctl status couchdb\
> ● couchdb.service - CouchDB server daemon\
> Loaded: loaded (/etc/systemd/system/couchdb.service; enabled; vendor
> preset: disabled)\
> Active: active (running) since Thu 2016-12-01 10:03:16 UTC; 4 days
> ago\
> ...

1.  Try to restart couchdb by executing: \# systemctl restart couchdb .
    Verify.

2.  Check for disk fill especially /usr/local as it contains the couch
    database itself. Note that threshold for /usr/local disk space has
    been lowered to 70% as couchdb usage can quickly grow.

    1.  When the filesystem crosses the threshold execute cron jobs
        in /etc/cron.d/couchdb\_compaction

    2.  OR increase the disk space.

        1.  To increase disk space, make sure that there is at least one
            working couchdb instance.

        2.  Remove the couchdb node in question from load balancer by
            setting active=0 in the two load balancers (.13, .12).

        3.  Stop couchdb in question.

        4.  Increase /home/couchdb partition via Control Portal.

        5.  Restart couchdb, check web endpoints
            http://&lt;ip&gt;:5984/\_utils.

        6.  Check logs in /var/log/messages.

        7.  Add couchdb back to rotation in load balancers.

3.  Check if couch processes are not running. If not running - \#
    systemctl restart couchdb.  

4.  Other causes are currently unknown, feel free to update the recipe
    if you notice other causes.

#### \[GLOBAL Z-CONSOLE\] 10.128.131.27 (or .19) threshold of Greater than xx percent used not met: current value xx

**Symptom**: These are couchdb nodes. see  COUCHDB-related connection
refused (aborted) errors - disk space issue.

#### **INFORMATION: COUCHDB, proxy related alerts (those are from IPs 10.128.131.12, .13, .19, .27)**

Note: Do not merge the tickets into one or config/code push, those nodes
are not affected by code/config push

#### INFORMATION: 'Update: Ticket bucket'

Note: ticket can be ignored

Validity: Indefinite

#### INFORMATION: Disregard DMS alerts coming from CA2R8D0xx

Note: <https://trello.com/c/vsnqESpj/3590-ca2r8d0xx-dms-alerts-was-unclear-snitch-source> →
please check

#### INFORMATION: CTL Z-Console:  Anything with a count greater than 100

Note: requires operator intervention as it will almost certainly not
clear itself.

 

#### HOWTO: Diagnosing a Z-Node DMS Health Issue

**Symptom**: DMS alarm goes missing and is not triggered by
provisioning. Also, this missing state may occur within an hour or so
after replacement is done.

**Steps**:

1.  SSH to the node and check syslog to see if the cron that is in
    charge of sending the DMS ping was activated:\
         tail -f /var/log/cron

2.  Verify the health of the Z-Node:\
          /usr/local/bin/report\_zenoss.sh -v

3.  Check the evconsole of the affected Z-Node. This will also verify
    the health of the Z-Node and provide additional details.

4.  Coordinate the findings with CTL on-call so that a card may be
    created.

 

#### Problem: Provisioner &lt;provisioner&gt;: Unable to reset IP of &lt;Z-Master/Z-Node&gt; in zconsole OR IP address conflicts between nodes in Z-Console

**Symptom**: Down alerts triggered by Z-Console even though the node has
already been provisioned

**Cause**: Provisioner was not able to auto-update the IP of the newly
provisioned node. 

 **Steps**:

1.  Cross-check the IP of the affected node in Z-Console with the node's
    IP in Chef Workstation.\
    *        /root/zenoss-cookbooks/scripts/knife\_ssh.sh &lt;DC&gt; all
    'hostname'*

2.  If there is a conflict, attempt to update the IP address of the node
    in Z-Console.\
    \
     **NOTE: Only use the following as a last resort**

3.  If updating the IP address does not work (usually due to the IP
    already assigned to another device), delete the node(s) manually
    from Z-Console. Make sure that the performance data and close events
    boxes are UNCHECKED.

4.  Manually add the device(s) back to Z-Console (Monitor icon &gt; Add
    a single device). Make sure that *Name or IP* and *Title* are filled
    in and Model Device is checked.

5.  Wait for the process to finish and verify that the device is UP.

 

#### Problem: Could not connect to Redis at 127.0.0.1:6379: Connection refused

** **

> \[root@VA1R82ZGPPROVISIONER \~\]\# redis-cli\
> Could not connect to Redis at 127.0.0.1:6379: Connection refused\
> not connected&gt;
>
> \[root@VA1R82ZGPPROVISIONER \~\]\# telnet 127.0.0.1 6379\
> Trying 127.0.0.1...
>
> telnet: connect to address 127.0.0.1: Connection refused 

**Solution:**

1.  Restart redis using /etc/init.d/redis stop / status / start.

2.  Restart supervisorctl services: supervisorctl restart all

3.  Confirm if redis is now running.

#### Problem: ZENRABBIT PROVISIONING\_TIMEOUT reached.

**Symptom:** Missing ZENRABBIT (&lt;SOME DC&gt;R82ZGPZENRABBIT) from
STATEDB.\
Note this is a temporary recipe. Check progress of
<https://trello.com/c/UkKomMtD/3304-zenrabbit-provisioning-timeout-reached-missing-zenrabbit-wa1r82zgpzenrabbit-from-statedb>

**Cause:**

1.  ZENRABBIT state table was deliberately deleted

2.  redis-cli del &lt;SOME DC&gt;zenrabbit\` which tries to reprovision
    ZENRABBIT (edited)

3.  Some component sets the state to (nil). The component is still
    unidentified.

Cause 1 should never be done. In case it is done the fix below still
applies.

Cause 2 is not supported yet. There is already a card to allow zenrabbit
to be reprovisioned.

**Steps:**

1.  Check if ZENRABBIT is still OK. Execute
    \`/usr/local/bin/report\_rabbit.sh -v\` in ZENRABBIT

2.  If it is OK, set the state to PROVISIONED:

> redis-cli hset &lt;REPLACE NODE PREFIX&gt;ZENRABBIT state PROVISIONED
>
> Example:
>
> redis-cli hset WA1R82ZGPZENRABBIT state PROVISIONED

1.   We are still narrowing down Cause 3. Create a Trello card and
    document:

    1.  when you noticed the issue, when the states changed, any action
        you executed

    2.  in Chef workstation, get the output of: 

\[root@VA1ZGPCHEF-W01 \~\]\#
/root/zenoss-cookbooks/scripts/knife\_ssh.sh all provisioner 'for i in
\$(redis-cli keys "\*" | grep -E "ZENRABBIT"); do echo -n \$i" " &&
redis-cli hget \$i state; done' R82

10.128.131.60 VA1R82ZGPZENRABBIT "PROVISIONED"

10.92.142.30 IL1R82ZGPZENRABBIT "PROVISIONED"

10.100.107.23 CA3R82ZGPZENRABBIT "PROVISIONED"

10.56.153.24 CA2R82ZGPZENRABBIT "PROVISIONED"

10.166.3.13 VA2R82ZGPZENRABBIT "PROVISIONED"

148.156.13.23 NE1R82ZGPZENRABBIT "PROVISIONED"

10.71.168.23 NY1R82ZGPZENRABBIT "PROVISIONED"

10.121.186.13 UC1R82ZGPZENRABBIT "PROVISIONED"

10.95.147.17 UT1R82ZGPZENRABBIT "PROVISIONED"

10.81.25.20 WA1R82ZGPZENRABBIT "PROVISIONED"

10.51.72.15 CA1R82ZGPZENRABBIT "PROVISIONED"

10.60.112.15 GB1R82ZGPZENRABBIT "PROVISIONED"

10.105.99.23 GB3R82ZGPZENRABBIT "PROVISIONED"

10.110.119.24 DE1R82ZGPZENRABBIT "PROVISIONED"

10.160.8.18 AU1R82ZGPZENRABBIT "PROVISIONED"

10.130.73.37 SG1R82ZGPZENRABBIT "PROVISIONED"

#### Problem: \[MISSING\] &lt;DATACENTER&gt; ZGPZENRABBIT hasn't checked in

(**or ZENRABBIT hasn't checked in**)

There are two RABBITMQ instances in a z-group. Check
[Terms](#CTLZenossIncidentResponseRecipes-Terms) (rabbits) for more
info. This recipe is only applicable to ZENRABBIT.

 

**Cause**: Number of messages on node has reached its limit

 

 **Steps**:

 

1.  SSH to the affected ZENRABBIT instance. 

2.  Get the script or command that checks the health of ZENRABBIT.\
    \
    Pick the line in crontab that calls report\_rabbit.sh. Add -v to the
    command. Example:

3.  \# crontab -l

4.  \# Chef Name: snitch on rabbit

> \* \* \* \* \* /usr/local/bin/report\_rabbit.sh -g
> http://10.128.131.220:4984/zenoss\_databag/ -m manifest\_au1\_r82\_zgp
>
> The command to check will be:
>
> /usr/local/bin/report\_rabbit.sh -g
> http://10.128.131.220:4984/zenoss\_databag/ -m manifest\_au1\_r82\_zgp
> -v

1.  Find out what the issue is or which node is unhealthy.

> Example 1:
>
> \#run the command below to check for unhealthy nodes. In this case the
> alert was "\[MISSING\] GB3R8RC2ZGPZENRABBIT hasn't checked in"
>
> hostname::GB3R8RC2ZGPZENRABBIT | uptime::03:54:08 up 33 days, 9:41, 2
> users, load average: 0.00, 0.01, 0.00 | amqp\_beam\_count::1 |
> sdc\_usage::22 pct full | rmq\_zcomms\_user::1 | chk\_vhosts\_ret::
> /GB3R8RC2ZGPZMASTER 12 msgs. /GB3R8RC2ZGPZNODE01 1065 msgs.
> /GB3R8RC2ZGPZNODE02 661 msgs. /GB3R8RC2ZGPZNODE03 3076 msgs. CRITICAL:
> 30012 messages in vhost /GB3R8RC2ZGPZNODE04. Limit is 10000.
> /GB3R8RC2ZGPZNODE05 167 msgs. /GB3R8RC2ZGPZNODE06 1754 msgs.
> /GB3R8RC2ZGPZNODE07 308 msgs. /GB3R8RC2ZGPZNODE08 214 msgs.
> /GB3R8RC2ZGPZNODE09 4842 msgs. /GB3R8RC2ZGPZTRAP01 0 msgs.
> /GB3R8RC2ZGPZTRAP02 12 msgs. | chk\_thresh\_ret:: 10392 MB disk free.
> Free limit: 47 MB. 823 MB memory used. Used limit: 4 GB. 23 used file
> descriptors. 102400 available. 35551 Erlang processes in use. 1048576
> available. 3 file descriptors used as sockets. 92068 available.
>
> Threshold checks:
>
> 10392 MB disk free. Free limit: 47 MB.
>
> 823 MB memory used. Used limit: 4 GB.
>
> 23 used file descriptors. 102400 available.
>
> 35551 Erlang processes in use. 1048576 available.
>
> 3 file descriptors used as sockets. 92068 available.
>
> Node is not healthy:
>
> /GB3R8RC2ZGPZMASTER 12 msgs.
>
> /GB3R8RC2ZGPZNODE01 1065 msgs.
>
> /GB3R8RC2ZGPZNODE02 661 msgs.
>
> /GB3R8RC2ZGPZNODE03 3076 msgs.
>
> CRITICAL: 30012 messages in vhost /GB3R8RC2ZGPZNODE04. Limit is 10000.
> &lt;========================= BACKING UP ISSUE!
>
> /GB3R8RC2ZGPZNODE05 167 msgs.
>
> /GB3R8RC2ZGPZNODE06 1754 msgs.
>
> /GB3R8RC2ZGPZNODE07 308 msgs.
>
> /GB3R8RC2ZGPZNODE08 214 msgs.
>
> /GB3R8RC2ZGPZNODE09 4842 msgs.
>
> /GB3R8RC2ZGPZTRAP01 0 msgs.
>
> /GB3R8RC2ZGPZTRAP02 12 msgs.
>
> Example 2: the error below is related to missing vhosts (a vhost has
> the same name as the z-node where its queued perf data messages are
> coming from).
>
> \[root@AU1R82ZGPZENRABBIT \~\]\# /usr/local/bin/report\_rabbit.sh -g
> http://10.128.131.220:4984/zenoss\_databag/ -m manifest\_au1\_r82\_zgp
> -v
>
> hostname::AU1R82ZGPZENRABBIT | uptime::01:21:28 up 42 days, 31 min, 1
> user, load average: 0.03, 0.01, 0.00 | amqp\_beam\_count::1 |
> sdc\_usage::20 pct full | rmq\_zcomms\_user::1 | chk\_vhosts\_ret::
> ERROR: Need to set 'amqp\_endpoint=remote' in node AU1R82ZGPZNODE03.
> ERROR: Need to set 'amqp\_endpoint=remote' in node AU1R82ZGPZNODE06.
> ERROR: Need to set 'amqp\_endpoint=remote' in node AU1R82ZGPZNODE04.
> ERROR: Need to set 'amqp\_endpoint=remote' in node AU1R82ZGPZNODE05.
> /AU1R82ZGPZMASTER 3049 msgs. /AU1R82ZGPZNODE01 3071 msgs.
> /AU1R82ZGPZNODE02 123 msgs. /AU1R82ZGPZTRAP01 0 msgs.
> /AU1R82ZGPZTRAP02 0 msgs. /AU1R82ZGPZTRAP03 16 msgs. Accounting for
> missing vhosts ... ERROR: Missing vhost for AU1R82ZGPZNODE03 ERROR:
> Missing vhost for AU1R82ZGPZNODE06 ERROR: Missing vhost for
> AU1R82ZGPZNODE04 ERROR: Missing vhost for AU1R82ZGPZNODE05 |
> chk\_thresh\_ret:: 10664 MB disk free. Free limit: 47 MB. 490 MB
> memory used. Used limit: 4 GB. 23 used file descriptors. 102400
> available. 19538 Erlang processes in use. 1048576 available. 1 file
> descriptors used as sockets. 92068 available.
>
> Threshold checks:
>
> 10664 MB disk free. Free limit: 47 MB.
>
> 490 MB memory used. Used limit: 4 GB.
>
> 23 used file descriptors. 102400 available.
>
> 19538 Erlang processes in use. 1048576 available.
>
> 1 file descriptors used as sockets. 92068 available.
>
> Node is not healthy:
>
> ERROR: Need to set 'amqp\_endpoint=remote' in node AU1R82ZGPZNODE03.
>
> ERROR: Need to set 'amqp\_endpoint=remote' in node AU1R82ZGPZNODE06.
>
> ERROR: Need to set 'amqp\_endpoint=remote' in node AU1R82ZGPZNODE04.
>
> ERROR: Need to set 'amqp\_endpoint=remote' in node AU1R82ZGPZNODE05.
>
> /AU1R82ZGPZMASTER 3049 msgs.
>
> /AU1R82ZGPZNODE01 3071 msgs.
>
> /AU1R82ZGPZNODE02 123 msgs.
>
> /AU1R82ZGPZTRAP01 0 msgs.
>
> /AU1R82ZGPZTRAP02 0 msgs.
>
> /AU1R82ZGPZTRAP03 16 msgs.
>
> Accounting for missing vhosts ...
>
> ERROR: Missing vhost for AU1R82ZGPZNODE03
>
> ERROR: Missing vhost for AU1R82ZGPZNODE06
>
> ERROR: Missing vhost for AU1R82ZGPZNODE04
>
> ERROR: Missing vhost for AU1R82ZGPZNODE05

1.  If you get an output similar to the highlighted section of the
    output above, SSH to the unhealthy node and check the status of
    zenperfdataforwarder. In this case the unhealthy node
    is GB3R8RC2ZGPZNODE04

    1.  Check /opt/zenoss/log/zenperfdataforwarder.log if there are any
        errors

    2.  Check if the log is moving and you are seeing tasks are still
        being dispatched\
        sample log:

> \[zenoss@GB3R8RC2ZGPZNODE04 root\]\$ tail -f
> /opt/zenoss/log/zenperfdataforwarder.log\
> 2016-05-02 11:09:54,658 INFO zen.zenperfdataforwarder: In
> gb3-esx-hpc-a01-18.m.t3n.dom: Starting pullData()\
> 2016-05-02 11:09:54,666 INFO zen.zenperfdataforwarder: In
> gb3-esx-hpc-a01-18.m.t3n.dom: Established connection to Kafka.\
> 2016-05-02 11:09:54,666 INFO zen.zenperfdataforwarder: pullData 0
> queues for gb3-esx-hpc-a01-18.m.t3n.dom in 0.0 seconds at 0.0
> queues/s\
> 2016-05-02 11:09:54,669 INFO zen.zenperfdataforwarder: Sent
> perfDFHeartbeat for gb3-esx-hpc-a01-18.m.t3n.dom to Kafka.\
> 2016-05-02 11:09:54,669 INFO zen.zenperfdataforwarder: Successful scan
> of gb3-esx-hpc-a01-18.m.t3n.dom completed\
> 2016-05-02 11:09:58,599 INFO zen.zenperfdataforwarder: In
> gb3-esx-hpc-a01-07.m.t3n.dom: Starting pullData()\
> 2016-05-02 11:09:58,606 INFO zen.zenperfdataforwarder: In
> gb3-esx-hpc-a01-07.m.t3n.dom: Established connection to Kafka.\
> 2016-05-02 11:09:58,606 INFO zen.zenperfdataforwarder: pullData 0
> queues for gb3-esx-hpc-a01-07.m.t3n.dom in 0.0 seconds at 0.0
> queues/s\
> 2016-05-02 11:09:58,609 INFO zen.zenperfdataforwarder: Sent
> perfDFHeartbeat for gb3-esx-hpc-a01-07.m.t3n.dom to Kafka.\
> 2016-05-02 11:09:58,610 INFO zen.zenperfdataforwarder: Successful scan
> of gb3-esx-hpc-a01-07.m.t3n.dom completed\
> 2016-05-02 11:10:26,587 INFO zen.zenperfdataforwarder: In
> gb3-vc-b03.t3n.dom-vsphere: Starting pullData()\
> 2016-05-02 11:10:26,600 INFO zen.zenperfdataforwarder: In
> gb3-vc-b03.t3n.dom-vsphere: Established connection to Kafka.\
> 2016-05-02 11:10:39,366 INFO zen.zenperfdataforwarder: pullData 192
> queues for gb3-vc-b03.t3n.dom-vsphere in 12.8 seconds at 15.0
> queues/s\
> 2016-05-02 11:10:39,366 INFO zen.zenperfdataforwarder: Successfully
> sent 528 messages to Kafka.\
> 2016-05-02 11:10:39,367 INFO zen.zenperfdataforwarder: Sent
> perfDFHeartbeat for gb3-vc-b03.t3n.dom-vsphere to Kafka.\
> 2016-05-02 11:10:39,369 INFO zen.zenperfdataforwarder: Successful scan
> of gb3-vc-b03.t3n.dom-vsphere completed\
> 2016-05-02 11:11:29,218 INFO zen.zenperfdataforwarder: In
> gb3-veeam01-b01.t3n.dom: Starting pullData()\
> 2016-05-02 11:11:29,225 INFO zen.zenperfdataforwarder: In
> gb3-veeam01-b01.t3n.dom: Established connection to Kafka.\
> 2016-05-02 11:11:29,383 INFO zen.zenperfdataforwarder: pullData 3
> queues for gb3-veeam01-b01.t3n.dom in 0.2 seconds at 18.0 queues/s

1.  Restart zenperfdataforwarder as zenoss user\
    \[root@GB3R8RC2ZGPZNODE04 \~\]\# su zenoss\
    \[zenoss@GB3R8RC2ZGPZNODE04 \~\]\# zenperfdataforwarder stop\
    \
    \#check if the daemon was really stopped\
    \[zenoss@GB3R8RC2ZGPZNODE04 \~\]\# ps aux |
    grep zenperfdataforwarder\
    \
    \#if the daemon was not really stopped force kill the daemon\
    \[zenoss@GB3R8RC2ZGPZNODE04 \~\]\# kill -9 zenperfdataforwarder\
    \
    \[zenoss@GB3R8RC2ZGPZNODE04 \~\]\# zenperfdataforwarder start

<!-- -->

1.  If the health check returns, (amqp\_beam\_count::0)

>   Node is not healthy:   
>
>     not exactly one beam.smp process running  
>
>     zcomms rabbitmq user not defined
>
> Start the rabbitmq server
>
>      /etc/init.d/rabbitmq-server start
>
> Restart zenperfdataforwarder in all z-nodes to force them to reconnect
> to the RabbitMQ instance that you just started.
>
> In Chef Workstation,
>
> \# DC=VA2 \# Replace this with the target DC\
> \# REL=R82 \# Replace this if necessary\
> \# /root/zenoss-cookbooks/scripts/knife\_ssh.sh "\$DC" znodes
> '/etc/init.d/zendaemonctl.sh stop zenperfdataforwarder' "\$REL"
>
> There is no need to start because monit will detect that the daemon is
> down and it will start it.
>
> You can then tail the logs and there should be *no errors* like the
> following.
>
> \[root@VA1ZGPCHEF-W01 \~\]\#
> /root/zenoss-cookbooks/scripts/knife\_ssh.sh "\$DC" znodes 'tail -n 10
> /opt/zenoss/log/zenperfdataforwarder.log' R82
>
> ...
>
> 10.166.3.19 2017-03-29 14:25:02,401 INFO zen.zenperfdataforwarder:
> Successful scan of 10.170.15.24-10.170.15.24 completed\
> 10.166.3.32 2017-03-29 14:17:52,504 ERROR zen.zenperfdataforwarder: In
> proc\_QueueHandler(Devices/localhost/os/filesystems/opt\_zenoss/usedBlocks\_usedBlocks):
> AMQPConnectionError: Connection to 10.166.3.17:5672 failed: \[Errno
> 111\] Connection refused
>
> ...
>
> 10.166.3.27 2017-03-29 13:03:45,230 CRITICAL
> pika.adapters.base\_connection: Tried to handle an error where no
> error existed\
> 10.166.3.27 2017-03-29 14:24:17,720 ERROR
> pika.adapters.base\_connection: Error event 8, IOError(4, 'Interrupted
> system call')\
> 10.166.3.27 2017-03-29 14:24:57,304 ERROR
> pika.adapters.base\_connection: Error event 8, IOError(4, 'Interrupted
> system call')\
> 10.166.3.27 2017-03-29 14:25:08,135 ERROR
> pika.adapters.base\_connection: Error event 8, IOError(4, 'Interrupted
> system call')
>
> ...
>
> 10.166.3.20 2017-03-29 13:17:37,842 ERROR
> pika.adapters.base\_connection: Socket Error on fd 64: 104\
> 10.166.3.20 2017-03-29 13:17:37,843 WARNING
> zen.zenperfdataforwarder.queuehandler: Connection closed, reopening in
> 5 seconds: (0) Not specified\
> 10.166.3.20 2017-03-29 13:17:37,843 ERROR
> pika.adapters.base\_connection: Error event 25, None\
> 10.166.3.20 2017-03-29 13:17:37,843 CRITICAL
> pika.adapters.base\_connection: Tried to handle an error where no
> error existed
>
> ...

1.  If the check does not recover after 15mins, delete-restore
    the corresponding vhost of the node with the message limit
    violation. Possible reasons why we need to do this:

    1.  Device is NOT modeled but previously was modeled with components
        discovered. Stuck messages correspond to these components.

    2.  Device is no longer existing (e.g. moved to another znode).

    3.  Here are the steps for vhost deletion and restoration:

        1.  SSH to the ZENRABBITMQ node.\
            Run: \
            \
            /usr/local/bin/rabbitmqadmin -H &lt;zenrabbitmq\_host e.g.
            CA2R8RC2ZENRABBIT&gt; -u perfdf -p &lt;perfdf\_password&gt;
            delete vhost name=/&lt;node\_name e.g. CA2R8RC2ZNODE01&gt;\
            \
            You can get *perfdf\_password* from the affected node in
            /opt/zenoss/etc/global.conf, line "perfdfpassword
            -------------"

        2.  SSH to affected node. Run chef-client.

2.  If the check does not recover after 30mins, reprovision the
    unhealthy node

3.  If the alert does not recover after reprovisioning, the threshold
    can be temporarily increased (as long as the message count is not
    increasing , remains roughly the same level).
    Edit /usr/local/bin/rabbitmq-stats-health.py, MSG\_COUNT\_LIMIT
    parameter.  After increasing the threshold, create a trello card
    under prod ops issue for Prem (urgent, non-emergency)\
    \
    Example, this was was increased from 10k to 20k\
    \# diff /usr/local/bin/rabbitmq-stats-health.py.orig
    /usr/local/bin/rabbitmq-stats-health.py

> \`\`\`6c6\
> &lt; MSG\_COUNT\_LIMIT = 100000  \# per vhost\
> ---\
> &gt; MSG\_COUNT\_LIMIT = 150000  \# per vhost

1.  Check the volume of metrics processed by the z-node. This gives you
    a rough idea if it is more than the agreed threshold of 100,000.\
    \
    [Sample
    visualization](https://kibana-cascadeo.analytics.ctl.io/app/kibana#/visualize/edit/Count-metrics-per-znode-per-dc-(replace-header.location)?_g=(refreshInterval:(display:Off,pause:!f,value:0),time:(from:now-15m,mode:quick,to:now))&_a=(filters:!((%27$state%27:(store:appState),meta:(alias:!n,disabled:!f,index:%5Bie_zenoss-%5DYYYY.MM.DD,key:header.messageType,negate:!f,value:zenoss_ts_data),query:(match:(header.messageType:(query:zenoss_ts_data,type:phrase))))),linked:!f,query:(query_string:(analyze_wildcard:!t,query:%27header.location:va1%27)),uiState:(),vis:(aggs:!((id:%273%27,params:(field:hostname,order:desc,orderBy:%272%27,size:10),schema:segment,type:terms),(id:%272%27,params:(),schema:metric,type:count)),listeners:(),params:(addLegend:!t,addTimeMarker:!f,addTooltip:!t,defaultYExtents:!f,mode:stacked,scale:linear,setYExtents:!f,shareYAxis:!t,times:!(),yAxis:()),title:%27Count%20metrics%20per%20znode%20per%20dc%20(replace%20header.location)%27,type:histogram))):
    replace header.location.\
    \
     

> *(If there is only a single device monitored by the z-node, the drain
> step below is useless. Create a card for CTL Devs (Prem / Jared) to
>  deep dive the performance data volume)*\
> \
> Proceed to drain the
> node ( [HOWTO:ReducetheworkloadonarunningZ-Nodebyrebalancing](#CTLZenossIncidentResponseRecipes-HOWTO:) )
> or use the mover script to selectively move the devices to the node
> with fewer message count:
>
> Example: move il1-srx-core in IL1 NODE07 to IL1 NODE06 since NODE06
> has the fewer number of count message and is not overloaded. \
>                   \[root@VA1ZGPZCONSOL16 \~\]\# perl
> /usr/local/bin/mover.l il1r82zgpznode06
>
>                  Paste a list of devices to move to il1r82zgpznode06
> in IL1
>
>                   il1-srx-core

1.  Check again if all the nodes are now healthy:

> \[root@IL1R82ZGPZENRABBIT \~\]\# /usr/local/bin/report\_rabbit.sh -g
> http://10.128.131.220:4984/zenoss\_databag/ -m manifest\_il1\_r82\_zgp
> -v
>
> hostname::IL1R82ZGPZENRABBIT | uptime::16:15:02 up 229 days, 2:35, 1
> user, load average: 0.15, 0.15, 0.16 | amqp\_beam\_count::1 |
> sdc\_usage::23 pct full | rmq\_zcomms\_user::1 | chk\_vhosts\_ret::
> /IL1R82ZGPZMASTER 468 msgs. /IL1R82ZGPZNODE01 2601 msgs.
> /IL1R82ZGPZNODE02 605 msgs. /IL1R82ZGPZNODE03 803 msgs.
> /IL1R82ZGPZNODE04 644 msgs. /IL1R82ZGPZNODE05 196 msgs.
> /IL1R82ZGPZNODE06 296 msgs. /IL1R82ZGPZNODE07 2804 msgs.
> /IL1R82ZGPZNODE08 945 msgs. /IL1R82ZGPZNODE09 200 msgs.
> /IL1R82ZGPZNODE10 804 msgs. /IL1R82ZGPZNODE11 0 msgs.
> /IL1R82ZGPZNODE12 19707 msgs. /IL1R82ZGPZNODE13 753 msgs.
> /IL1R82ZGPZNODE14 342 msgs. /IL1R82ZGPZNODE15 0 msgs.
> /IL1R82ZGPZNODE16 0 msgs. /IL1R82ZGPZNODE17 0 msgs. /IL1R82ZGPZNODE18
> 0 msgs. /IL1R82ZGPZNODE19 0 msgs. /IL1R82ZGPZNODE20 0 msgs.
> /IL1R82ZGPZNODE21 0 msgs. /IL1R82ZGPZTRAP01 32 msgs. /IL1R82ZGPZTRAP02
> 16 msgs. Accounting for missing vhosts ... | chk\_thresh\_ret:: 10320
> MB disk free. Free limit: 47 MB. 1733 MB memory used. Used limit: 4
> GB. 10777 used file descriptors. 102400 available. 85502 Erlang
> processes in use. 1048576 available. 7 file descriptors used as
> sockets. 92068 available.
>
> Messages per vhost:
>
> /IL1R82ZGPZMASTER 468 msgs.
>
> /IL1R82ZGPZNODE01 2601 msgs.
>
> /IL1R82ZGPZNODE02 605 msgs.
>
> /IL1R82ZGPZNODE03 803 msgs.
>
> /IL1R82ZGPZNODE04 644 msgs.
>
> /IL1R82ZGPZNODE05 196 msgs.
>
> /IL1R82ZGPZNODE06 296 msgs.
>
> /IL1R82ZGPZNODE07 2804 msgs.
>
> /IL1R82ZGPZNODE08 945 msgs.
>
> /IL1R82ZGPZNODE09 200 msgs.
>
> /IL1R82ZGPZNODE10 804 msgs.
>
> /IL1R82ZGPZNODE11 0 msgs.
>
> /IL1R82ZGPZNODE12 19707 msgs.
>
> /IL1R82ZGPZNODE13 753 msgs.
>
> /IL1R82ZGPZNODE14 342 msgs.
>
> /IL1R82ZGPZNODE15 0 msgs.
>
> /IL1R82ZGPZNODE16 0 msgs.
>
> /IL1R82ZGPZNODE17 0 msgs.
>
> /IL1R82ZGPZNODE18 0 msgs.
>
> /IL1R82ZGPZNODE19 0 msgs.
>
> /IL1R82ZGPZNODE20 0 msgs.
>
> /IL1R82ZGPZNODE21 0 msgs.
>
> /IL1R82ZGPZTRAP01 32 msgs.
>
> /IL1R82ZGPZTRAP02 16 msgs.
>
> Accounting for missing vhosts ...
>
> Threshold checks:
>
> 10320 MB disk free. Free limit: 47 MB.
>
> 1733 MB memory used. Used limit: 4 GB.
>
> 10777 used file descriptors. 102400 available.
>
> 85502 Erlang processes in use. 1048576 available.
>
> 7 file descriptors used as sockets. 92068 available.
>
> Node is healthy

#### Problem: **10.128.131.202: Datasource HttpMonitor/HttpMonitor command timed out**

**Symptom**: The following alerts are flapping:

-   **10.128.131.202: Datasource HttpMonitor/HttpMonitor command timed
    out**

-   **10.128.131.13: Datasource
    HttpMonitor-Zenoss-DeviceUID/zenoss-deviceuid command timed out**

-   **10.128.131.202: connect to address 10.128.131.202 and port 8080:
    Connection refused**

**Cause**: zenoss-inventory is not working properly on the Proxy
instance

**Steps**:** **

1.  SSH to the current proxy LB and check the virtual server table if
    there are two entries for 10.128.131.202:webcache\
    \
     

    1.  You can check who the current proxy LB is by checking which one
        has the virtual ip 

> \[root@VA1ZGPPROXYLB01 \~\]\# ifconfig\
> eth0 Link encap:Ethernet HWaddr 00:0C:29:8B:2C:74\
> inet addr:10.128.131.22 Bcast:10.128.131.255 Mask:255.255.255.0\
> inet6 addr: fe80::20c:29ff:fe8b:2c74/64 Scope:Link\
> UP BROADCAST RUNNING MULTICAST MTU:1500 Metric:1\
> RX packets:1821246217 errors:0 dropped:0 overruns:0 frame:0\
> TX packets:1816830770 errors:0 dropped:0 overruns:0 carrier:0\
> collisions:0 txqueuelen:1000\
> RX bytes:1457429962584 (1.3 TiB) TX bytes:1457461339908 (1.3 TiB)
>
>  \
> eth0:1 Link encap:Ethernet HWaddr 00:0C:29:8B:2C:74\
> inet addr:10.128.131.201 Bcast:10.128.131.255 Mask:255.255.255.0\
> UP BROADCAST RUNNING MULTICAST MTU:1500 Metric:1\
>  \
> **eth0:2** Link encap:Ethernet HWaddr 00:0C:29:8B:2C:74\
> inet addr:10.128.131.202 Bcast:10.128.131.255 Mask:255.255.255.0\
> UP BROADCAST RUNNING MULTICAST MTU:1500 Metric:1\
>  \
> lo Link encap:Local Loopback
>
> inet addr:127.0.0.1 Mask:255.0.0.0\
> inet6 addr: ::1/128 Scope:Host\
> UP LOOPBACK RUNNING MTU:65536 Metric:1\
> RX packets:642 errors:0 dropped:0 overruns:0 frame:0\
> TX packets:642 errors:0 dropped:0 overruns:0 carrier:0\
> collisions:0 txqueuelen:0\
> RX bytes:61424 (59.9 KiB) TX bytes:61424 (59.9 KiB)

1.  Check the virtual server table. As you can see from the output
    below, its only balancing to one instance\
     \
    \[root@VA1ZGPPROXYLB01 \~\]\# ipvsadm -L\
    IP Virtual Server version 1.2.1 (size=4096)\
    Prot LocalAddress:Port Scheduler Flags\
    -&gt; RemoteAddress:Port Forward Weight ActiveConn InActConn

> TCP 10.128.131.201:couchdb wlc\
> -&gt; 10.128.131.19:couchdb Route 1 108 194\
> -&gt; 10.128.131.27:couchdb Route 1 112 191\
> **TCP 10.128.131.202:webcache wlc persistent 360**\
> **-&gt; 10.128.131.12:webcache Route 1 26 0**

1.   

2.            10.128.131.12 is VA1ZGPPROXY02

3.  4.  SSH to the proxy instance that is not listed
    under 10.128.131.202:webcache and restart zenoss-inventory \
    In this case, the IP of the instance that is not included on the
    virtual server table is 10.128.131.13 (VA1ZGPPROXY01)\
    \
    \[root@VA1ZGPPROXY01 \~\]\# /etc/init.d/zenoss-inventory restart\
    Restart service SERVICE\_NAME\
    info: Forever restarted process(es):\
    data: uid command script forever pid id logfile uptime\
    data: \[0\] xSmh /usr/bin/node proxy-couch.js 10098 10104
    /var/log/zenoss-inventory.log 0:11:10:13.154

5.  Check the virtual server table again on the LB

> \[root@VA1ZGPPROXYLB01 \~\]\# ipvsadm -L\
> IP Virtual Server version 1.2.1 (size=4096)\
> Prot LocalAddress:Port Scheduler Flags\
> -&gt; RemoteAddress:Port Forward Weight ActiveConn InActConn\
> TCP 10.128.131.201:couchdb wlc\
> -&gt; 10.128.131.19:couchdb Route 1 60 182\
> -&gt; 10.128.131.27:couchdb Route 1 60 181\
> **TCP 10.128.131.202:webcache wlc persistent 360**\
> **-&gt; 10.128.131.12:webcache Route 1 25 0**\
> **-&gt; 10.128.131.13:webcache Route 1 23 1477**

1.  The alerts should clear and stop reoccurring.

 

#### HOWTO: Testing the Kafka Brokers

**Symptom**: When an entire datacenter is missing in Kibana, it is
possible that the pipeline from our Z-Group to Kibana itself is broken.
We can only check up to the Kafka stage and by doing so we will be
making sure that the problem is not from our end.

**Steps**:

1.   The connection to the Kafka brokers endpoint can be tested using
    ping or telnet. Testing the connection to ALL brokers on only one
    Z-Node is usually sufficient.\
       \
           \[root@VA1R8RC2ZGPZNODE01 \~\]\# grep broker\_list
    /opt/logstash/forwarder/etc/conf.d/logstash\_forwards.conf\
         broker\_list =&gt;
    "[kafka-va1-01.analytics.ctl.io](http://kafka-va1-01.analytics.ctl.io):9092,kafka-va1-[02.analytics.ctl.io](http://02.analytics.ctl.io):9092,[kafka-va1-03.analytics.ctl.io](http://kafka-va1-03.analytics.ctl.io):9092"\
         broker\_list =&gt;
    "[kafka-va1-01.analytics.ctl.io](http://kafka-va1-01.analytics.ctl.io):9092,kafka-va1-[02.analytics.ctl.io](http://02.analytics.ctl.io):9092,[kafka-va1-03.analytics.ctl.io](http://kafka-va1-03.analytics.ctl.io):9092"\
    \
           \[root@VA1R8RC2ZGPZNODE01 \~\]\# telnet
    [kafka-va1-01.analytics.ctl.io](http://kafka-va1-01.analytics.ctl.io)
    9092\
           Trying 10.125.81.41...\
           Connected to
    [kafka-va1-01.analytics.ctl.io](http://kafka-va1-01.analytics.ctl.io).\
           Escape character is '\^\]'.\
           \^\]\
           ===\
           \[root@VA1R8RC2ZGPZNODE01 \~\]\# telnet
    [kafka-va1-02.analytics.ctl.io](http://kafka-va1-02.analytics.ctl.io)
    9092\
           Trying 10.125.81.42...\
           Connected to
    [kafka-va1-02.analytics.ctl.io](http://kafka-va1-02.analytics.ctl.io).\
           Escape character is '\^\]'.\
           \^\]\
           ===\
           \[root@VA1R8RC2ZGPZNODE01 \~\]\# telnet
    [kafka-va1-03.analytics.ctl.io](http://kafka-va1-03.analytics.ctl.io)
    9092\
           Trying 10.125.81.43...\
           Connected to
    [kafka-va1-03.analytics.ctl.io](http://kafka-va1-03.analytics.ctl.io).\
           Escape character is '\^\]'.\
           \^\]

2.  If ALL brokers are not reachable, check if all the other Z-Nodes on
    same DC have the same issue. Request a ticket to CTL NOC to have the
    Kafka broker IPs reachable from the Z-Group VLAN.

3.  If one of the brokers remains reachable, include a brief summary of
    the results of the tests below in your report, along with which
    brokers are unreachable. Set the ticket to CTL NOC as normal
    priority.

    -   Check the tail end of /opt/zenoss/log/zenperfdataforwarder.log
        before stopping zenperfdataforwarder daemon and kill any stale
        process before starting it.\
        \# tail –f /opt/zenoss/log/zenperfdataforwarder.log\
        \# su - zenoss\
        \$ zenperfdataforwarder stop\
        \$ ps -ef | grep zenperfdataforwarder\
        \$ kill -9 &lt;pid if any&gt;\
        \$ zenperfdataforwarder start 

    -   Inspect zenperfdataforwarder.log if the issue is resolved. Also
        verify in the Kibana that log volume is back to normal. Verify
        that Zenoss daemons are running and actively monitoring the
        devices.\
         

    -   Check status of the daemons. Ensure that the
        zenperfdataforwarder daemon is running. This daemon forwards the
        RRD data to the Kafka brokers.\
        \# /etc/init.d/zenoss status\
        \# su - zenoss -c "zenperfdataforwarder status"\
         

    -   Check the daemon logs and verify that the last timestamp is
        recent.\
        \# tail -n1 /opt/zenoss/log/\*.log\
         

    -   Check for errors in the logs. If there are no errors and the
        daemon just appears to hang, attempt to stop the daemon and kill
        any stale process. Start the daemon and verify that it is
        running.\
         

    -   Verify that logstash service is running. Check logstash logs in
        /opt/logstash/forwarder/log for errors.\
        \# /etc/init.d/logstash\_forwarder status\
         

    -   If the issue persists with all services running, check if there
        are monitoring gaps on the Zenoss graphs. Verify that the
        devices are reachable and observe any errors (e.g. timeout,
        device down) on the event console which indicates failure to
        collect data.

 

#### PROBLEM: How to manually replace IPVS with Samplicator to load balance UDP \[syslogs, snmp traps\] (Whenever a ZTRAP is replaced in NY1)

**Solution**

1.  SSH to the Primary and Secondary Load Balancers of NY1 (IP Address
    and credentials are in
    : [https://control.ctl.io](https://control.ctl.io/)) 

> Primary: 10.71.168.13\
> \
> Secondary: 10.71.168.14 Look for the load balancer that is active.\
> \
> It is the host assigned the Virtual IP:
>
> eth0:1 Link encap:Ethernet HWaddr 00:0C:29:7A:58:8D\
> **inet addr:10.71.168.200** Bcast:10.71.168.255 Mask:255.255.255.0\
> UP BROADCAST RUNNING MULTICAST MTU:1500 Metric:1

1.  Execute /etc/init.d/ipvsadm restart

> This applies the config  /etc/sysconfig/ipvsadm\
> Notice the syslog and snmptrap config lines are commented:
>
> ~\[root@NY1ZGPSYSLBP02\ \~\]\#\ cat\  /etc/sysconfig/ipvsadm~
>
> ~-A\ -t\ 10.71.168.200:8080\ -s\ rr~
>
> ~-a\ -t\ 10.71.168.200:8080\ -r\ 10.71.168.19:8080\ -g\ -w\ 1~
>
> ~-a\ -t\ 10.71.168.200:8080\ -r\ 10.71.168.25:8080\ -g\ -w\ 1~
>
> ~-a\ -t\ 10.71.168.200:8080\ -r\ 10.71.168.31:8080\ -g\ -w\ 1~
>
> ~-a\ -t\ 10.71.168.200:8080\ -r\ 10.71.168.32:8080\ -g\ -w\ 1~
>
> ~-a\ -t\ 10.71.168.200:8080\ -r\ 10.71.168.38:8080\ -g\ -w\ 1~
>
> ~\#-A\ -u\ 10.71.168.200:162\ -s\ wrr\ -o~
>
> ~\#-a\ -u\ 10.71.168.200:162\ -r\ 10.71.168.19:162\ -g\ -w\ 1~
>
> ~\#-a\ -u\ 10.71.168.200:162\ -r\ 10.71.168.25:162\ -g\ -w\ 1~
>
> ~\#-a\ -u\ 10.71.168.200:162\ -r\ 10.71.168.31:162\ -g\ -w\ 1~
>
> ~\#-a\ -u\ 10.71.168.200:162\ -r\ 10.71.168.32:162\ -g\ -w\ 1~
>
> ~\#-a\ -u\ 10.71.168.200:162\ -r\ 10.71.168.38:162\ -g\ -w\ 1~
>
> ~\#-A\ -u\ 10.71.168.200:514\ -s\ wrr\ -o~
>
> ~\#-a\ -u\ 10.71.168.200:514\ -r\ 10.71.168.19:514\ -g\ -w\ 1~
>
> ~\#-a\ -u\ 10.71.168.200:514\ -r\ 10.71.168.25:514\ -g\ -w\ 1~
>
> ~\#-a\ -u\ 10.71.168.200:514\ -r\ 10.71.168.31:514\ -g\ -w\ 1~
>
> ~\#-a\ -u\ 10.71.168.200:514\ -r\ 10.71.168.32:514\ -g\ -w\ 1~
>
> ~\#-a\ -u\ 10.71.168.200:514\ -r\ 10.71.168.38:514\ -g\ -w\ 1~

1.  After the restart, confirm that only the following (webcache/8080
    load balancer) remains:

>  
>
> ~\[root@NY1ZGPSYSLBP02\ \~\]\#\ ipvsadm\ -L~
>
> ~IP\ Virtual\ Server\ version\ 1.2.1\ (size=4096)~
>
> ~Prot\ LocalAddress:Port\ Scheduler\ Flags~
>
> ~-&gt;\ RemoteAddress:Port\           Forward\ Weight\ ActiveConn\ InActConn~
>
> ~TCP\  10.71.168.200:webcache\ rr~
>
> ~-&gt;\ 10.71.168.19:webcache\        Route\   1\      0\          0~
>
> ~-&gt;\ 10.71.168.25:webcache\        Route\   1\      0\          0~
>
> ~-&gt;\ 10.71.168.31:webcache\        Route\   1\      0\          1~
>
> ~-&gt;\ 10.71.168.32:webcache\        Route\   1\      0\          1~
>
> ~-&gt;\ 10.71.168.38:webcache\        Route\   1\      0\          1~
>
>  

1.  Modify the \`samplicate\` config\
     

> First find out what PIDs are for samplicate
>
> \[root@NY1ZGPSYSLBP02 \~\]\# pidof samplicate
>
> 32473 32087
>
> Then kill -15 the procs
>
> Example:
>
> \[root@NY1ZGPSYSLBP02 \~\]\# kill -15 32473
>
> \[root@NY1ZGPSYSLBP02 \~\]\# kill -15 32087
>
> \[root@NY1ZGPSYSLBP02 \~\]\# pidof samplicate
>
> (none shows)
>
>  
>
> Edit the following config files to reflect the updated IP address of
> the ztraps
>
> \[root@NY1ZGPSYSLBP02 \~\]\# cat /etc/samplicate-syslog
>
> 0.0.0.0/0.0.0.0:10.71.168.26/514 10.71.168.36/514 10.71.168.31/514
> 10.71.168.38/514 10.71.168.35/514
>
> \[root@NY1ZGPSYSLBP02 \~\]\# cat /etc/samplicate-snmptrap
>
> 0.0.0.0/0.0.0.0:10.71.168.26/162 10.71.168.36/162 10.71.168.31/162
> 10.71.168.38/162 10.71.168.35/162
>
> Re-run \`samplicate\` by running the two commands below. The \`-f\`
> switch puts them in the background
>
> \[root@NY1ZGPSYSLBP02 \~\]\# samplicate -b 1048576 -d 1 -s
> 10.71.168.200 -p 162 -S -c /etc/samplicate-snmptrap -f
>
> \[root@NY1ZGPSYSLBP02 \~\]\# samplicate -b 1048576 -d 1 -s
> 10.71.168.200 -p 514 -S -c /etc/samplicate-syslog -f
>
> \[root@NY1ZGPSYSLBP02 \~\]\#
>
>  

**Verification**

-   This visualization should contain bars from all the ztraps:
    <https://goo.gl/u1DkWD>.\
    \
    \
    Example:\
    \
     

 

#### **HOWTO: Smoketest** <https://zen.mon.ctl.io/>

**Example alerts**

-   [zen.mon.ctl.io](http://zen.mon.ctl.io/) HTTP CRITICAL: HTTP/1.1 500
    Internal Server Error - 249 bytes in 0.421 second response time

<!-- -->

-   [zen.mon.ctl.io](http://zen.mon.ctl.io) Connection refused

-   [zen.mon.ctl.io](http://zen.mon.ctl.io) Socket timeout after 10
    seconds

**Overview:**

-   [zen.mon.ctl.io](https://zen.mon.ctl.io/) resolves to 206.128.152.77
    which has 1-1 NAT with 10.137.128.200 on ZDMZ. You need to add your
    public IP address to whitelist to be able to access
    [https://zen.mon.ctl.io](https://zen.mon.ctl.io/).

-   \* 10.137.128.200 is a floating VIP assigned to either
    <https://control.ctl.io/manage#/va1/server/va1zdmzsyslbp01> or
    <https://control.ctl.io/manage#/va1/server/va1zdmzsyslbp02> (LVS
    load balancers).

-   \* Nginx proxies for api/web nodes in ZGP.

**How to whitelist your public IP address:**

1.  Go to <https://control.ctl.io/> and select ZDMZ account in the
    topmost left corner.

2.  Go to this node
    <https://control.ctl.io/manage#/va1/server/va1zdmzsyslbp01> and
    notice the public IP address 206.128.152.77 is clickable.

3.  Click 206.128.152.77 and it should load the IP configuration.

4.  Add your IP address in CIDR Notation. With a subnet of /32, it means
    a unique address and not a network.

5.  After adding your IP and updating, you should see a blueprint run.
    After blueprint is completed, you should now be able to access
    <https://zen.mon.ctl.io/>.

6.  After logging in, open the links and see if it works specifically
    the zenoss web
    app[\]](https://cascadeo.slack.com/archives/D06K7QZ1U/p1470394948000432)
    and zcosystem API links.

**NOTE**: To access frontend server/virtual IP, you need zdmz VPN. You
can download it in   <https://control.ctl.io/network/vpn> , first switch
to ZDMZ account.

**Smoketest steps:**

1.  Check the 2 backend servers: <http://10.128.131.48:8080/> and
    <http://10.128.131.47:8080/>, check if both servers are accessible.
    Credentials is in LP with username svc\_zenoss.

    1.  If servers is not okay, SSH to
        <https://control.ctl.io/manage#/va1/server/va1zgpweb03> and
        <https://control.ctl.io/manage#/va1/server/va1zgpweb04>.

    2.  Check the "node" process by executing: *pm2 list*, all processes
        should be in running state.

    3.  If not, try restarting processes by executing: *pm2 restart all*
        , all processes should be in running state.

    4.  If processes still do not start, escalate to component owner
        (Jerome).

<!-- -->

1.  If both backend servers are accessible, check frontend server (nginx
    proxy), <https://10.137.128.12/> and <https://10.137.128.19/>.

    1.  If frontend server is not okay, SSH to
         <https://control.ctl.io/manage#/va1/server/va1zdmzproxy01>  and
        <https://control.ctl.io/manage#/va1/server/va1zdmzproxy02>.

    2.  Check if nginx is running: *ps ax | grep nginx*. If not running.
        try to restart the service: *service nginx restart*

> *\
> *

1.  Check <https://10.137.128.200/> which is the front end virtual IP.

    1.  If frontend virtual IP is not okay, SSH to
        <https://control.ctl.io/manage#/va1/server/va1zdmzsyslbp01>  and
        <https://control.ctl.io/manage#/va1/server/va1zdmzsyslbp02>.

    2.  Execute *ipvsadm --list,* there should be healthy nodes under
        https virtual server on va1zdmzsyslb01/02. Example:

> TCP  10.137.128.200:https wlc persistent 360
>
> -&gt; 10.137.128.12:https          Route   1      0          4
>
> -&gt; 10.137.128.19:https          Route   1      0          0

1.  If both load balancers do not have this, escalate to component
    owner, Jerome.

<!-- -->

1.  Also check the backend virtual IP, <http://10.128.131.202:8080/>.

    1.  If backend virtual IP is not accessible, SSH in to
        <https://control.ctl.io/manage#/va1/server/va1zgpproxylb01>
         and/or
        <https://control.ctl.io/manage#/va1/server/va1zgpproxylb02>.

    2.  Execute *ipvsadm --list*. There should be two nodes under
        webcache virtual server. Like this:

> TCP  10.128.131.202:webcache wlc persistent 360
>
> -&gt; 10.128.131.47:webcache       Route   1      0          24
>
> -&gt; 10.128.131.48:webcache       Route   1      0          40

1.  Note that only one of LB01 and LB02 is active at a time. if both
    load balancers do not have nodes under webcache, escalate to
    component owner (Jerome).

<!-- -->

1.  Then check if <https://zen.mon.ctl.io/> is accessible. If not, this
    is most probably network issue on CTL side. Report to CTL NOC but
    make sure your IP is already in the whitelist.

**NOTE**: To access frontend server/virtual IP, you need zdmz VPN. You
can download it in  <https://control.ctl.io/network/vpn>, first switch
to ZDMZ account.

References:

-   <https://zen.mon.ctl.io/>

-   <https://zen.mon.ctl.io/proxy>

-   <https://zen.mon.ctl.io/docs/>

-   <https://support.ctl.io/hc/en-us/articles/207789316-Zenoss-Monitoring-Important-Links-Start-here>

#### 

#### **PROBLEM: Missing DMS &lt;VA1ZDMZ | ZGP&gt; "Chef Data Bag to Couchbase Sync" or "Couchbase to Chef Data Bag Sync"**

Note: This resides in Chef Workstation (10.128.131.18) as
/root/zenoss-cookbooks/scripts/sync\_chef\_databag\_to\_couchbase.py run
on cron as root.  It is VERY CRITICAL (EMERGENCY) when this breaks
because most probably the Couchbase Cluster is out of sync from the Chef
Data Bag.

Solution:

1.  Login to Chef Workstation and identify the script that Chef Data Bag
    to Couchbase\
    syncs in cron. The script in red is the line that syncs in cron.\
    \
    \[root@VA1ZGPCHEF-W01 \~\]\# crontab -l

> \*/1 \* \* \* \* m=\`hostname && uptime && echo " - " && df -h | grep
> sdc | cut -c35-36 && echo pct full\` && curl -o /dev/null --silent -d
> "m=\$m" <https://nosnch.in/2aae17ca5c>
>
> \*/10 \* \* \* \* m=\`time ( sh /usr/local/bin/backup\_databag.sh
> &&gt; /dev/null) 2&gt;&1\` && curl -d "m=\$m"
> <https://nosnch.in/9d87c536c5>
>
> \#\*/5 \* \* \* \* m=\`python
> /root/zenoss-cookbooks/scripts/sync\_chef\_databag\_to\_couchbase.py
> 2&gt;&1\` && curl -d "m=\$m" <https://nosnch.in/85db4d44ef>
>
> \*/3 \* \* \* \* m=\`python
> /root/zenoss-cookbooks/scripts/sync\_chef\_databag\_to\_couchbase.py
> -s
> [http://10.128.131.220:4984/zenoss\_databag/](http://10.128.131.49:4984/zenoss_databag/)
> 2&gt;&1\` && curl -d "m=\$m" <https://nosnch.in/85db4d44ef>
>
> \#\*/2 \* \* \* \* /usr/bin/python /root/prem/vsphere-monit.py
> &gt;&gt; /root/prem/vsphere-monit.log 2&gt;&1

       2. Try to execute the command from cron related to “Chef Data Bag
to Couchbase Sync” to see where it fails. The line in red is what errors
will look like.

> \[root@VA1ZGPCHEF-W01 \~\]\# python
> /root/zenoss-cookbooks/scripts/sync\_chef\_databag\_to\_couchbase.py
> -s
> [http://10.128.131.220:4984/zenoss\_databag/](http://10.128.131.49:4984/zenoss_databag/)
>
> SYNC\_GATEWAY:
> [http://10.128.131.220:4984/zenoss\_databag/](http://10.128.131.49:4984/zenoss_databag/)
>
> Getting couchbase\_canary
>
> get\_cbdoc: couchbase\_canary
>
> Traceback (most recent call last):
>
> File
> "/root/zenoss-cookbooks/scripts/sync\_chef\_databag\_to\_couchbase.py",
> line 107, in &lt;module&gt;
>
>   doc = get\_cbdoc(d)
>
> File
> "/root/zenoss-cookbooks/scripts/sync\_chef\_databag\_to\_couchbase.py",
> line 30, in get\_cbdoc
>
>   response = requests.request("GET", url, data=payload,
> headers=headers)
>
> File "/usr/lib/python2.6/site-packages/requests/api.py", line 57, in
> request
>
>   return session.request(method=method, url=url, \*\*kwargs)
>
> File "/usr/lib/python2.6/site-packages/requests/sessions.py", line
> 475, in request
>
>   resp = self.send(prep, \*\*send\_kwargs)
>
> File "/usr/lib/python2.6/site-packages/requests/sessions.py", line
> 585, in send
>
>   r = adapter.send(request, \*\*kwargs)
>
> File "/usr/lib/python2.6/site-packages/requests/adapters.py", line
> 467, in send
>
>   raise ConnectionError(e, request=request)
>
> requests.exceptions.ConnectionError:
> HTTPConnectionPool(host='10.128.131.220', port=4984): Max retries
> exceeded with url: /zenoss\_databag/couchbase\_canary (Caused by
> NewConnectionError('&lt;requests.packages.urllib3.connection.HTTPConnection
> object at 0x7f304ff9e9d0&gt;: Failed to establish a new connection:
> \[Errno 111\] Connection refused',))
>
> 10.128.131.220 is the Couchbase Sync Gateway Server . It cannot
> connect to port 4984 because the sync\_gateway service is down, thus
> it should be started.
>
> SSH to Couchbase Sync Gateway server (credentials is in
> <https://control.ctl.io>) indicated in the exception. Find if
> sync\_gateway is running.
>
> \[root@VA1ZGPCHBASE101 logs\]\# ps aux | grep sync\_gateway
>
> root     23862  0.0  0.0 112644   960 pts/3    S+   09:28   0:00 grep
> --color=auto sync\_gateway
>
> \[root@VA1ZGPCHBASE101 logs\]\# service sync\_gateway start
>
> Redirecting to /bin/systemctl start  sync\_gateway.service
>
> \[root@VA1ZGPCHBASE101 logs\]\# ps aux | grep sync\_gateway
>
> sync\_ga+ 23889  0.0  0.0 113116  1220 ?        Ss   09:28   0:00
> /usr/bin/bash -c /opt/couchbase-sync-gateway/bin/sync\_gateway
> /home/sync\_gateway/sync\_gateway.json &gt;&gt;
> /home/sync\_gateway/logs/sync\_gateway\_access.log 2&gt;&gt;
> /home/sync\_gateway/logs/sync\_gateway\_error.log
>
> sync\_ga+ 23890  6.6  0.2 524156 34044 ?        Sl   09:28   0:00
> /opt/couchbase-sync-gateway/bin/sync\_gateway
> /home/sync\_gateway/sync\_gateway.json
>
> root     23973  0.0  0.0 112644   964 pts/3    S+   09:28   0:00 grep
> --color=auto sync\_gateway
>
> \[root@VA1ZGPCHBASE101 logs\]\#

NOTE: It takes time for the z-nodes to sync to couchbase sync gateway

#### PROBLEM: Rogue/Stale Workers Causing Celery Worker Heartbeat Queue (celeryev) to Back Up

**Symptom**: **&lt;SOME DC&gt; RabbitMQ is missing in DMS. Example: IL1
RABBITMQ is missing.**

**Steps**:

-   To know which script activated the DMS alarm, run the following:

> \[root@GB1R8RC2ZGPRABBIT \~\]\# crontab -l
>
> \# Chef Name: logrotate \* \* \* \* \* /usr/sbin/logrotate -f
> /etc/logrotate.d/logstash\_forwarder
>
> \# Chef Name: snitch on rabbit \* \* \* \* \*
> /usr/local/bin/report\_rabbit.sh -s

-   Run the script in verbose mode:

> \[root@GB1R8RC2ZGPRABBIT \~\]\# /usr/local/bin/report\_rabbit.sh -v
>
> hostname::GB1R8RC2ZGPRABBIT | uptime::13:05:02 up 291 days, 3:40, 2
> users, load average: 2.02, 0.81, 0.42 | amqp\_beam\_count::1 |
> sdc\_usage::81 pct full |
>
> rmq\_zcomms\_user::1 | chk\_vhosts\_ret:: CRITICAL: 3031298 messages
> in vhost /heartbeat. Limit is 10000. /zcomms\_tasks 8064 msgs. |
> chk\_thresh\_ret::
>
> 2634 MB disk free. Free limit: 47 MB. 1851 MB memory used. Used limit:
> 4 GB. 1593 used file descriptors. 102400 available. 4536 Erlang
> processes in use.
>
> 1048576 available. 312 file descriptors used as sockets. 92068
> available. Threshold checks:
>
> 2634 MB disk free. Free limit: 47 MB.
>
> 1851 MB memory used. Used limit: 4 GB.
>
> 1593 used file descriptors. 102400 available.
>
> 4536 Erlang processes in use. 1048576 available.
>
> 312 file descriptors used as sockets. 92068 available.
>
> Node is not healthy:
>
> load average &gt;= 2
>
> disk space used &gt;= 80%
>
> CRITICAL: 3031298 messages in vhost /heartbeat. Limit is 10000.
>
> /zcomms\_tasks 8064 msgs.
>
> See possible issues below.

##### ISSUE: RABBITMQ DATABASE MNESIA IS CONSUMING A LOT OF DISK

-   1.  Verify the results from running the script in verbose mode

> \[root@GB1R8RC2ZGPRABBIT \~\]\# df -h
>
> Filesystem Size Used Avail Use% Mounted on
>
> /dev/sdc 14G 11G 2.6G 81% /
>
> tmpfs 5.9G 0 5.9G 0% /dev/shm
>
> /dev/sda1 495M 51M 420M 11% /boot

1.  Another way to check:

> du --max-depth=1 -h
>
> 8.4G ./var
>
> \[root@GB1R8RC2ZGPRABBIT /\]\# cd /var/
>
> \[root@GB1R8RC2ZGPRABBIT var\]\# du --max-depth=1 -h
>
> 7.9G ./lib
>
> ===
>
> culprit:
>
> \[root@GB1R8RC2ZGPRABBIT rabbitmq\]\# pwd /var/lib/rabbitmq
>
> \[root@GB1R8RC2ZGPRABBIT rabbitmq\]\# du --max-depth=1 -h
>
> 7.8G ./mnesia
>
> ===
>
> In this example, mnesia, which is the storage of rabbitmq, is the
> culprit. 
>
> This is the rabbitmq database, proceed to the backing up issue below
> to find the culprit.

##### ISSUE: BACKING UP OF SOME QUEUES 

Explanation: Recently we saw the celery worker heartbeat (not
zcomms.heartbeat) queue back up because of rogue / stale workers.

-   1.  Check flower (&lt;provisioner&gt;:5555) of the affected DC and
        compare it to other DCs. If it is unusually high, then it is
        also an indicator of an unhealthy RabbitMQ.

        1.  You can restart the rabbitmq service. 

        2.  /etc/init.d/rabbitmq-server stop

        3.  ps aux | grep rabbitmq-server

        4.  /etc/init.d/rabbitmq-server start

    2.  Look into RabbitMQ Management UI *http://&lt;ZGROUP RABBITMQ OR
        ZENRABBITMQ&gt;:15672/*\
        These are the vhosts to look at zcomms.messaging vhost (creds:
        zcomms/8vUx32E656AQ43h) or zcomms.heartbeat vhost (creds:
        heartbeatuser/heartbeatpass).\
        \
        \
        Figure: Example of a vhost that is backing up

    3.  Inspect the queues at *http://&lt;ZGROUP RABBITMQ OR
        ZENRABBITMQ&gt;:15672/\#/queues* and look for a very high number
        of messages. Change the number of queues to render in the table
        so you scan quickly. Turn off auto-refresh. The offending queue
        might be backing up because there are no workers to consume the
        messages. \
        \
        [*\
        *](http://10.60.112.17:15672/#/queues)Figure: Change the number
        of items to show in the table\
        \
        \
        \
        Figure: at the bottom of the page you can change the Update
        frequency to never\
        [*\
        *](http://10.60.112.17:15672/#/queues)

    4.  [Z](http://10.60.112.17:15672/#/queues)oom in to the queue that
        is backing up. The queue below is prefixed **celeryev,** which
        is the queue used for celery events for celery (internals)
        monitoring. If it is not prefixed with celeryev, you can use
        succeeding steps to get more hints. \
        \
        Check where it is coming from. Shut down the node that is
        publishing if it is an old / rogue / stale z-node. Delete or
        purge the queue.\
        \
        \
        Figure: Trace the publisher and consumer by looking at the
        Message rates breakdown and Consumers drop down

    5.  (If the previous steps already remedied the issue, no need to
        proceed) Restart the heartbeats of the provisioner, then the
        Z-nodes. Check if the queue is still increasing.

> \[root@GB1R8RC2ZGPPROVISIONER celery\]\# supervisorctl restart
> celery-heartbeat
>
> celery-heartbeat: stopped
>
> celery-heartbeat: started
>
> \[root@VA1ZGPCHEF-W01 zenoss\]\#
> /root/zenoss-cookbooks/scripts/knife\_ssh.sh GB1 znodes 'supervisorctl
> restart celery-heartbeat'
>
> 10.60.112.22 celery-heartbeat: stopped
>
> 10.60.112.23 celery-heartbeat: stopped
>
> 10.60.112.15 celery-heartbeat: stopped
>
> 10.60.112.25 celery-heartbeat: stopped
>
> 10.60.112.31 celery-heartbeat: stopped
>
> 10.60.112.16 celery-heartbeat: stopped
>
> 10.60.112.21 celery-heartbeat: stopped
>
> 10.60.112.20 celery-heartbeat: stopped
>
> 10.60.112.29 celery-heartbeat: stopped
>
> 10.60.112.30 celery-heartbeat: stopped
>
> 10.60.112.24 celery-heartbeat: stopped
>
> 10.60.112.28 celery-heartbeat: stopped
>
> 10.60.112.22 celery-heartbeat: started
>
> 10.60.112.21 celery-heartbeat: started
>
> 10.60.112.25 celery-heartbeat: started
>
> 10.60.112.23 celery-heartbeat: started
>
> 10.60.112.20 celery-heartbeat: started
>
> 10.60.112.31 celery-heartbeat: started
>
> 10.60.112.16 celery-heartbeat: started
>
> 10.60.112.15 celery-heartbeat: started
>
> 10.60.112.29 celery-heartbeat: started
>
> 10.60.112.24 celery-heartbeat: started
>
> 10.60.112.30 celery-heartbeat: started
>
> 10.60.112.28 celery-heartbeat: started

1.  If the queue is still increasing, then it must be deleted. The
    RabbitMQ DMS should report back shortly after the deletion of the
    queue.

#### PROBLEM: SNMP agent down (for CTL monitored devices only, not for zNodes or Cascadeo managed resources)

**Symptom**: \[zenoss\] gb3-be-r6-10g-u0 SNMP agent down - no response
received

**Steps**:

1.  Go the zNode monitoring the device. Check first if the SNMP of the
    device is accessible, by going to the device page, clicking the
    "command" button and selecting "snmpwalk". If SNMP is accessible,
    the output should display some stats while if not, it would indicate
    a Time Out.\
    \
    Below is example of time out result through zenoss UI:\
    \
    *==== uc1t3nnsvpx01 ====*\
    *snmpwalk -\${device/zSnmpVer} -c\${device/zSnmpCommunity}
    64.15.184.4 system*\
    *Timeout: No Response from 64.15.184.4*\
    \
    Image below is where you can find snmpwalk:

2.  If SNMP is accessible, spot check some device graphs if they're
    collecting. Also try to model the device if successful (some plugins
    may thrown errors depending on the components, but ignore them if
    others are good). If there are no issues, then the event can be
    closed/ignored.

3.  If SNMP is not accessible as indicated by a time out, also try to
    model the device.

4.  If modeling shows the error below (regardless if SNMP is successful
    or not), replace the znode:\
    \
    \[zenoss@GB3R82ZGPZNODE13 \~\]\$ zenmodeler run -d
    gb3-be-r4r5-40g-u1\
    2016-11-28 02:57:00,700 INFO zen.ZenModeler: Connecting to
    localhost:8789\
    2016-11-28 02:57:00,703 INFO zen.ZenModeler: Connected to ZenHub\
    2016-11-28 02:57:00,766 ERROR zen.ZenModeler: Error occured:
    \[Failure instance: Traceback (failure with no frames): &lt;class
    'Products.ZenHub.PBDaemon.RemoteException'&gt;: : Traceback (most
    recent call last):\
    File
    "/opt/zenoss/Products/ZenHub/[PBDaemon.py](http://pbdaemon.py/)",
    line 97, in inner\
    return callable(\*args, \*\*kw)\
    File
    "/opt/zenoss/Products/ZenHub/services/[ModelerService.py](http://modelerservice.py/)",
    line 80, in remote\_getClassCollectorPlugins\
    for dc in self.dmd.Devices.getSubOrganizers():\
    File
    "/opt/zenoss/Products/ZenModel/[Organizer.py](http://organizer.py/)",
    line 443, in getSubOrganizers\
    orgs = self.children()\
    File
    "/opt/zenoss/Products/ZenModel/[Organizer.py](http://organizer.py/)",
    line 125, in children\
    kids = \[ kid for kid in kids if self.checkRemotePerm(ZEN\_VIEW,
    kid)\]\
    File
    "/opt/zenoss/Products/ZenModel/[ZenModelBase.py](http://zenmodelbase.py/)",
    line 319, in checkRemotePerm\
    return user.has\_permission(permission, robject.primaryAq())\
    File
    "/opt/zenoss/lib/python/ZODB/[Connection.py](http://connection.py/)",
    line 860, in setstate\
    self.\_setstate(obj)\
    File
    "/opt/zenoss/lib/python/ZODB/[Connection.py](http://connection.py/)",
    line 914, in \_setstate\
    self.\_reader.setGhostState(obj, p)\
    File
    "/opt/zenoss/lib/python/ZODB/[serialize.py](http://serialize.py/)",
    line 613, in setGhostState\
    obj.**setstate**(state)\
    TypeError: **setstate**() takes exactly 2 arguments (1 given)\
    : &lt;no traceback&gt;\
    \]

5.  If the znode is replaced, check if modeling is successful (this is
    assuming SNMP is accessible). If modeling is successful, check if
    there are still SNMP down events coming from the said znode. If the
    error above still persists after replacing the zNode, try replacing
    again. And if still not fixed, escalate the issue to Prem or Jerome
    as it might be a provisioning issue.

6.  If there are no modeling errors (the error above), SNMP is verified
    not accessible, and no collection happening on the device, there
    might be an issue with the said device so report/forward the event
    to CTL NOC (along with the SNMPwalk result and other tests done).
    Ask them to check the SNMP settings of the device or if the device
    needs to be monitored (or maybe change monitoring status).

7.  You can check also if the port is open using nmap command, see below
    example result.

> \# nmap -p 161 -sU 64.15.184.4
>
> Starting Nmap 5.51 ( <http://nmap.org> ) at 2016-12-06 00:03 UTC\
> Nmap scan report for 64.15.184.4\
> Host is up (0.0017s latency).\
> PORT STATE SERVICE\
> 161/udp open|filtered snmp
>
> Nmap done: 1 IP address (1 host up) scanned in 0.32 seconds
>
> **Failed snmpwalk**\
> \# snmpwalk -v2c -c&lt;SNMP COMMUNITY REMOVED&gt; 64.15.184.4 system\
> Timeout: No Response from 64.15.184.4\
> **Working snmpwalk targeted at another device**\# snmpwalk -v2c
> -c&lt;SNMP COMMUNITY REMOVED&gt; 10.124.15.98 system
>
> SNMPv2-MIB::sysDescr.0 = STRING: Linux UC1T3NPLATDNS01
> 3.13.0-79-generic \#123-Ubuntu SMP Fri Feb 19 14:27:58 UTC 2016
> x86\_64

1.  You can find SNMP COMMUNITY REMOVED in the image below

 9. Lastly, verify the issue from multiple znodes in the same
datacenter.

10. If still not fixed there might be an issue and report the event to
CTL NOC along with SNMPWALK results with other investigations.

#### PROBLEM: host\_table = (rabbit\_details\['internal\_ipaddr'\], rabbit) KeyError: 'internal\_ipaddr'

Example:
<https://trello.com/c/3cBSucAu/3826-provisioner-au1r82zgpprovisioner-internal-ipaddr>

Traceback looks like:

\[2016-12-07 23:47:59,384: ERROR/MainProcess\] Task
zcomms.provisioner.provisioner.replace\_node\[dc44cdd3-9d0d-4553-9d9d-23f7fb2eafe0\]
raised unexpected: KeyError('internal\_ipaddr',)

Traceback (most recent call last):

File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 240,
in trace\_task

R = retval = fun(args, \*\*kwargs)

File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 437,
in protected\_call

return self.run(args, \*\*kwargs)

File "/home/zenoss/zcomms/provisioner/provisioner.py", line 258, in
replace\_node

host\_table = (rabbit\_details\['internal\_ipaddr'\], rabbit)

KeyError: 'internal\_ipaddr'

Caused:

- The zgroup rabbit (node name is: \`&lt;SOME DATACENTER&gt;&lt;SOME
RELEASE&gt;ZGPRABBIT\`) is missing from provisioner. Most probably
someone deleted it manually

Solution:

1\. Get the following information of ZGPRABBIT (NOT ZENRABBIT) of the
datacenter from [https://control.ctl.io](https://control.ctl.io/):

- IP address

- ID: example: ca3zgprabbt07

- locationId: name of datacenter e.g. AU1

2\. After collecting the information, in the provisioner execute the
following (replacing the values from the information you collected
earlier):

\# redis-cli

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT internal\_ipaddr
10.160.8.22

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT role rabbit

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT powerState active

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT state PROVISIONED

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT status active

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT description rabbit

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT id ca3zgprabbt07

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT locationId AU1

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT groupId
dfdfa668a00b475fb9e5caa0105ea3f8

redis 127.0.0.1:6379&gt; hset AU1R82ZGPRABBIT account\_id zgp

Verification:

- The event "Provisioner \[DC\]r82zgpprovisioner internal-ipaddr" is not
persistent

#### PROBLEM: Juniper NetConf Alerts

**Symptom**: "zJUNOSNetConfUser is not configured ..." ;
"zJUNOSNetConfPassword is not configured..."; "zJUNOSNetConfHost is not
configured ..."

**Steps**:

1.  Checking the reporeted zProperty of the device: zJUNOSNetConfUser,
    zJUNOSNetConfPassword or zJUNOSNetConfHost. Make sure that they're
    properly filled up.

2.  If the zProperty has no entry, modify the zProperty of the device in
    the zController. Crendetials (for zJUNOSNetConfUser and
    zJUNOSNetConfPassword ) can be found at "Updated Juniper SRX
    Credentials and Inventory" in  LastPass (under the CTL folder &gt;
    ZGP Production ). As for zJUNOSNetConfHost alert, make sure that the
    device has a defined IP address in Zenoss. Create a trello card that
    changes were done for the device (please put the details of changes
    done) in the zController (add Peter / Leo as members), as this needs
    to be included in the next config push for the changes to take
    effect.

3.  If the next scheduled push is still some days away and the alert
    keeps firing, you can try modifying the reported zProperties in the
    zNode that monitors the device. However, please note that you have
    to modify every time the zNode is replaced.

**Symptom**: "No cluster groups discovered for the device..."

**Steps**:

1.  Check the device (in the zNode) if it has the "Cluster Groups"
    component

2.  If it has the Cluster groups components, try to remodel the device
    using this command: zenmodeler run -d device\_name   -v10
    --collect="CTL.python.JuniperExpClusterMap"

3.  Check if the modeling has any errors or issues discovering the
    cluster group component. If the discovery is successful, you'll see
    an 'XML' like output which is basically the API response to the
    cluster discovery request.

4.  If there's no 'XML' output observed and the alert is persistent,
    create a Trello card and assign to Peter

5.  If there's 'XML' output and verified that cluster components are
    discovered, wait for around 20 minutes. If the alert still persists,
    create a Trello card and assign to Peter. Make sure to detail what
    you did and observed

6.  If there's no Cluster group components on the device but the alert
    is persistent, try to remodel like step 2. If there's no cluster
    group components but the alert still persists for 20 minutes, again
    create a Trello card (Peter).

**Symptom**: " Netconf port on &lt;ip addr&gt; accessible but user
zenossro login failed: ConnectAuthError(ip addr)."

**Steps**:

1.  The alert means that the NetConf API login failed. This is indicated
    specifically by "ConnectAuthError". First check if the device has
    the necessary credentials (zJUNOSNetConfUser, zJUNOSNetConfPassword
    ) defined. The NetConf credentials should be under "Updated Juniper
    SRX Credentials and Inventory" in LastPass (under the CTL
    folder &gt; ZGP Production )

2.  Try to remodel the device using this command: zenmodeler run -d
    device\_name   -v10 --collect="CTL.python.JuniperExpClusterMap"

3.  If the same error is indicated in the modeling logs, wait for around
    30 minutes and try to remodel again.

4.  If the error persists and the alert didn't clear, create a CTL
    ticket indicating that Netconf API login on the device failed.
    Indicate that the zenossro account failed and that this prevents
    monitoring of components dependent on NetConf API. Request them to
    check if the zenossro account is properly configured on the device.
    Make sure to also put the logs of modeling test done emphasizing the
    error encountered. Also make sure to update the ticket created in
    case clears (in case the alert clears, wait for 15 minutes before
    concluding that the alert indeed cleared)

5.  In case the error is other than "ConnectAuthError", make a trello
    card and assign to Peter

#### PROBLEM: Devices were not found while running zb\_commit script to update backup version (CONFIG PUSH RELATED)

**Symptoms:**

- Can't add device using zb\_commit script, sample below:

+-----------------------------------------------------------------------+
| **{u'msg': u'ObjectNotFoundException: Cannot find                     |
| "/zport/dmd/Devices/Discovered/devices/10.104.15.36-10.104.15.36".    |
| NotFound: 10.104.15.36-10.104.15.36', u'type': u'exception',          |
| u'success': False}\                                                   |
| {u'msg': u'ObjectNotFoundException: Cannot find                       |
| "/zport/dmd/Devices/Discovered/devices/10.104.15.36-10.104.15.36".    |
| NotFound: 10.104.15.36-10.104.15.36', u'type': u'exception',          |
| u'success': False}\                                                   |
| {u'msg': u'ObjectNotFoundException: Cannot find                       |
| "/zport/dmd/Devices/Discovered/devices/10.104.15.36-10.104.15.36".    |
| NotFound: 10.104.15.36-10.104.15.36', u'type': u'exception',          |
| u'success': False}\                                                   |
| {u'msg': u'ObjectNotFoundException: Cannot find                       |
| "/zport/dmd/Devices/Discovered/devices/10.104.15.36-10.104.15.36".    |
| NotFound: 10.104.15.36-10.104.15.36', u'type': u'exception',          |
| u'success': False}**                                                  |
|                                                                       |
| **Failed to add the following device/s:\                              |
| 10.104.15.36-10.104.15.36 | /Discovered**                             |
|                                                                       |
| **Traceback (most recent call last):\                                 |
| File "helpers/zb\_commit.py", line 199, in &lt;module&gt;\            |
| args.check\_locpath)\                                                 |
| File "helpers/zb\_commit.py", line 96, in validate\_zcontroller\      |
| check\_locpath)\                                                      |
| File "/home/zenoss/zcomms/messaging/zcontroller\_tasks.py", line 409, |
| in validate\_device\_inventory\                                       |
| raise Exception('ERROR/Problem in adding devices!')\                  |
| Exception: ERROR/Problem in adding devices!**                         |
+-----------------------------------------------------------------------+

- pending zenjobs

- db conflict errors on /opt/zenoss/log/event.log

**Remediation**:\
- as zenoss, run zenossdbpack and restart zenoss, then you can repeat
step 5 in ZController run zb\_commit script.

#### PROBLEM: ZenRancid Backup alerts

**Symptom**: ... Old lockfile still exists ...

**Steps**:

**NOTE: Check first if the source of the alert is from an active znode
that's been seeded completely. It's possible that an orphaned znode or a
newly provisioned znode not yet seeded might run rancid (CRON). If
that's the case, you can ignore the alert (if possible remove/terminate
the orphan node).**

1.  SSH to the node that reports the error. The source node is also
    indicated in the alert itself

2.  Check if the lock file reported in the alert still exists (under
    /tmp). If it still exists, remove the lockfile: rm -f /tmp/lockfile

3.  The next scheduled RANCID run should not complain this error (every
    2 hours). If the error still persists create a trello card.

**Symptom**: rancid-run has failed

**Steps**:

**NOTE: Check first if the source of the alert is from an active znode
that's been seeded completely. It's possible that an orphaned znode or a
newly provisioned znode not yet seeded might run rancid (CRON). If
that's the case, you can ignore the alert (if possible remove/terminate
the orphan node).**

1.  SSH to the node that generated the alert.

2.  Check the logs under /opt/zenoss/rancid/var/log.

3.  If you errors see in the logs, copy those logs and create a trello
    card. Attach the logs in the card.

4.  You can also try to run zenrancid manually to check:

    1.  as zenoss user, edit its crontab (crontab -e) and comment the
        rancid to schedule to prevent it from running

    2.  check if there are rancid or git processes (ps aux |grep git; ps
        aux |grep rancid). If you can wait for the backup to finish (if
        it has just run as per CRON when you check) do so, or you can
        manually kill the processes. Also kill any zenrancid process

    3.  Run (as zenoss user): zenrancid run -v10

    4.  Check the /opt/zenoss/rancid/var/log.

    5.  Enable the commented CRON Rancid schedule.

#### PROBLEM: TypeError: expected integer key when browsing Infrastructure tab, Zenpython shutting down

**Symptom**: This is normally caused by the corruption of ZEO cache in
memcached.

**Verification :**

When browsing through the infrastructure tab, an error like the one
shown below exists

A related symptom would be Zenpython is shutting down with the following
messages (note that you will have an ESMsg snitch missing as well when
this happens)

\[zenoss@GB3R82ZGPZNODE10 root\]\$ zenpython run -d
gb3-vc-a03.t3n.dom-vsphere\
2016-10-07 00:11:23,747 INFO zen.python: plugins disabled by watchdog:
\[\]\
2016-10-07 00:11:23,747 INFO zen.python: starting watchdog with 7200.0s
timeout\
2016-10-07 00:11:23,748 INFO zen.zenpython: Connecting to
localhost:8789\
2016-10-07 00:11:23,751 INFO zen.zenpython: Connected to ZenHub\
2016-10-07 00:11:33,156 ERROR zen.collector.config: Configuration for
gb3-vc-a03 .t3n.dom-vsphere unavailable -- is that the correct name?\
2016-10-07 00:11:33,156 INFO zen.zenpython: Daemon CollectorDaemon
shutting down

**Steps**:

1.  Restart memcached on the instance as root\
    /etc/init.d/memcached stop\
    /etc/init.d/memcached start

2.  Restart zope\
    zopectl stop\
    zopectl start

3.  Additionally,if Zenpython is not runnung, start it as well\
    zenpython start

4.  The infrastructure tab should now load and you should also be able
    to do collection via zenpython

#### PROBLEM: \[Errno 113\] No route to host from AMQP transport (Z-group RabbitMQ)

**Solution: **

Note: The work queue of zcomms resides in the z-group rabbit.

1.  Locate the z-group rabbit: 

    1.  

>   \[root@VA1R82ZGPPROVISIONER \~\]\# cat /etc/hosts
>
> 10.128.131.34    VA1R82ZGPRABBIT

1.  SSH to the z-group rabbit node.

    1.  \[root@VA1ZGPCHEF-W01 \~\]\# ssh\_node VA1R82ZGPRABBIT\
        ssh-ing to 10.128.131.34…\
        ssh: connect to host 10.128.131.34 port 22: Network is
        unreachable

    2.  \[root@VA1ZGPCHEF-W01 \~\]\# telnet 10.128.131.34 22\
        Trying 10.128.131.34...\
        telnet: connect to address 10.128.131.34: No route to host

2.  If SSH is unresponsive, search the IP address of z-group rabbit in
    control portal and reboot the node. Note: reboot of the z-group
    rabbit may trigger “\[Errno 110\] Connection timed out”, you may
    ignore if not persistent.

> In the example, search returns to
> <https://control.ctl.io/manage#/va1/server/va1zgprabbt16>

1.  Monitor the blueprint after rebooting the z-group rabbit:\
    Example:
    <https://control.ctl.io/blueprints/queue/requestdetails/518025>.

2.  If the error “ \[Errno 113\] No route to host “ still persistent in
    celery-provisioning.log, restart the supervisor.

**Verification:**

1.  Check if you can SSH now to z-group rabbit

> f01:\~ prem\$ ssh\_node VA1R82ZGPRABBIT
>
> ssh-ing to 10.128.131.34...
>
> Last login: Wed Oct 19 14:19:20 2016 from 10.128.131.18
>
> \[root@VA1R82ZGPRABBIT \~\]\#

2\. Test from the provisioiner is connected. Note that 5672 is the amqp /
rabbitmq port.

> \[root@VA1R82ZGPPROVISIONER \~\]\# telnet  VA1R82ZGPRABBIT  5672
>
> Trying 10.128.131.34...
>
> Connected to VA1R82ZGPRABBIT.
>
> Escape character is '\^\]'.
>
> \^\]

3\. No more error related to  \[Errno 113\] No route to host

> File "/usr/lib/python2.6/site-packages/amqp/transport.py", line 95, in
> init
>
> raise socket.error(last\_err)

error: \[Errno 113\] No route to host

#### PROBLEM: getSecrets(): raise HTTPError(http\_error\_msg, response=self) requests.exceptions.HTTPError: 404 Client Error: Not Found

The traceback should look like the following to blame it to Couchbase
Sync Gateway.

Traceback (most recent call last):

File "/usr/bin/celery", line 11, in &lt;module&gt;

sys.exit(main())

File "/usr/lib/python2.6/site-packages/celery/main.py", line 30, in main

main()

File "/usr/lib/python2.6/site-packages/celery/bin/celery.py", line 81,
in main

cmd.execute\_from\_commandline(argv)

File "/usr/lib/python2.6/site-packages/celery/bin/celery.py", line 769,
in execute\_from\_commandline

super(CeleryCommand, self).execute\_from\_commandline(argv)))

File "/usr/lib/python2.6/site-packages/celery/bin/base.py", line 305, in
execute\_from\_commandline

argv = self.setup\_app\_from\_commandline(argv)

File "/usr/lib/python2.6/site-packages/celery/bin/base.py", line 465, in
setup\_app\_from\_commandline

self.app = self.find\_app(app)

File "/usr/lib/python2.6/site-packages/celery/bin/base.py", line 485, in
find\_app

return find\_app(app, symbol\_by\_name=self.symbol\_by\_name)

File "/usr/lib/python2.6/site-packages/celery/app/utils.py", line 232,
in find\_app

sym = imp(app)

File "/usr/lib/python2.6/site-packages/celery/utils/imports.py", line
101, in import\_from\_cwd

return imp(module, package=package)

File "/usr/lib/python2.6/site-packages/importlib/init.py", line 37, in
import\_module

import(name)

File "/home/zenoss/zcomms/provisioner/provisioner.py", line 64, in
&lt;module&gt;

SECRETS = MANIFESTOBJ.getSecrets()

File "/home/zenoss/zcomms/common/manifest.py", line 23, in getSecrets

data = self.getAll()

File "/home/zenoss/zcomms/common/manifest.py", line 19, in getAll

r.raise\_for\_status()

File "/usr/lib/python2.6/site-packages/requests/models.py", line 808, in
raise\_for\_status

raise HTTPError(http\_error\_msg, response=self)

requests.exceptions.HTTPError: 404 Client Error: Not Found

##### **Cause: pouchcouch (node.js app on port 3000) is down. **

pouchcouch syncs with Couchbase Servers through Sync Gateway.

Access port 3000 (http service) on the node where you found the
exception. Example: for CA1R82ZGPPROVISIONER open in the
browser <http://10.51.72.15:3000/>.

You should see something like below. You should see a list of docs and
*update\_seq* incremented.

{

"version": "0.0.3",

"localdbinfo": {

"doc\_count": 40,

"update\_seq": 327,

"backend\_adapter": "MemDOWN",

"db\_name": "zenoss\_databag",

"auto\_compaction": false,

"adapter": "leveldb"

},

"remotedbinfo": {

"committed\_update\_seq": 103123,

"compact\_running": false,

"db\_name": "zenoss\_databag",

"disk\_format\_version": 0,

"instance\_start\_time": 1478338237932771,

"purge\_seq": 0,

"state": "Online",

"update\_seq": 103123,

"host": "http://10.128.131.220:4984/zenoss\_databag/",

"auto\_compaction": false,

"adapter": "http"

},

"docs": {

"total\_rows": 40,

"offset": 0,

"rows": \[

{

"id": "a1",

"key": "a1",

"value": {

"rev": "2-3e7ec077359d2d4c8c8f59e7e2b1a048"

}

},

{

"id": "couchbase\_canary",

"key": "couchbase\_canary",

"value": {

"rev": "30105-538ca9b19e14d950d48e3a8e18e6cc43"

}

},

{

"id": "global",

"key": "global",

"value": {

"rev": "39-523efc7a044a8b40363f2679385af4a5"

}

},

{

"id": "manifest\_au1\_r82\_zgp",

"key": "manifest\_au1\_r82\_zgp",

"value": {

"rev": "2697-d488e813dc2a6a1464f2ec9a4b0b0fb5"

}

},

...

If the http service is down, try to check the status of the node.js app
pouchouch run as service on PM2.

\[root@CA1R82ZGPPROVISIONER \~\]\# pm2 list

┌──────────┬────┬──────┬──────┬────────┬─────────┬────────┬──────────────┬──────────┐

│ App name │ id │ mode │ pid │ status │ restart │ uptime │ memory │
watching │

├──────────┼────┼──────┼──────┼────────┼─────────┼────────┼──────────────┼──────────┤

│ www │ 0 │ fork │ 5789 │ online │ 3 │ 20h │ 439.973 MB │ disabled │

└──────────┴────┴──────┴──────┴────────┴─────────┴────────┴──────────────┴──────────┘

Use \`pm2 show &lt;id|name&gt;\` to get more details about an app

You have new mail in /var/spool/mail/root

\[root@CA1R82ZGPPROVISIONER \~\]\# pm2 show www

Describing process with id 0 - name www

┌───────────────────┬────────────────────────────────────────────────────────┐

│ status │ online │

│ name │ www │

│ restarts │ 3 │

│ uptime │ 20h │

│ script path │ /home/zenoss/zcomms-0.8.0-zcomms264/pouchcouch/bin/www │

│ script args │ N/A │

│ error log path │ /root/.pm2/logs/www-error-0.log │

│ out log path │ /root/.pm2/logs/www-out-0.log │

│ pid path │ /root/.pm2/pids/www-0.pid │

│ interpreter │ node │

│ interpreter args │ N/A │

│ script id │ 0 │

│ exec cwd │ /home/zenoss/zcomms-0.8.0-zcomms264/pouchcouch │

│ exec mode │ fork\_mode │

│ node.js version │ 0.10.46 │

│ watch & reload │ ✘ │

│ unstable restarts │ 0 │

│ created at │ 2016-11-02T01:01:55.150Z │

└───────────────────┴────────────────────────────────────────────────────────┘

Code metrics value

┌────────────┬────────┐

│ Loop delay │ 0.58ms │

└────────────┴────────┘

Add your own code metrics: http://bit.ly/code-metrics

Use \`pm2 logs www (--lines 1000)\` to display logs

Use \`pm2 monit\` to monitor CPU and Memory usage www

\[root@CA1R82ZGPPROVISIONER \~\]\# pm2 stop www

\[root@CA1R82ZGPPROVISIONER \~\]\# pm2 start www

##### **Cause: Sync Gateway is down**

Try getting a manifest using
Postman: [PostmanCollection](#CTLZenossIncidentResponseRecipes-Postma)

##### **Cause: Sync Gateway is slow**

Access port 3000 (http service) on the node where you found the
exception. Example: for CA1R82ZGPPROVISIONER open in the
browser <http://10.51.72.15:3000/>.

One symptom that it is slow is when pouchcouch on port 3000 returns an
HTTP error code of 500 and the remotedbinfo shows an error code of 400.
This could mean that the call to Sync Gateway timed out. Escalate this
issue to Prem. While waiting for Prem, attempt to restart Sync Gateway.

The Sync Gateway servers (right now we are striping and not load
balancing) can be found in this Server
Group <https://control.ctl.io/manage#/va1/group/cda048309b014567be3f701bbf599b2b>.

\[root@VA1ZGPSYNCGW02 \~\]\# initctl stop sync\_gateway

(\`ps aux | grep sync\`  if sync\_gateway went away)

\[root@VA1ZGPSYNCGW02 \~\]\# initctl start sync\_gateway

Sync gateway log files can found in */home/sync\_gateway/logs*.

#### PROVISIONER: PROVISIONER\_SEEDING\_ZNODE\_FAILURE

Supplemental message: 

*No new ZenBackup image in ZController: ***&lt;some timestamp in
epoch&gt;***. Latest zb\_version in Z-Node CA1R82ZGPZNODE05 is:
***&lt;some other timestamp in epoch&gt;***. Check 'zboutput\_ver' and
mapping 'version' in the manifest!*

**Explanation: **This was flagged because ****&lt;some timestamp in
epoch&gt;**** is less than ****&lt;some other timestamp in
epoch&gt;****. This probably means there is no new zenbackup image in
zcontroller because no zenbackup commit was seen to have run after the
time marking in the currently deployed zenbackup image.

**Causes:**

1.  for some reason provisioner did not update the state table with the
    time marking of the currently deployed zenbackup image

2.  the flag is accurate that there is really no new zenbackup image in
    z-controller

For cause 1, you can manually override *zboutput\_ver* in the state
table but it is simpler to re-do the [config
push](https://docs.google.com/document/d/1w-wnvMlTaDD2MDlslxFlnfYb2KwxAhNI8rkZpbIj28Y/edit#heading=h.ukqzo4fodfqb)
in the entire datacenter. For cause 2, do the config push.

#### PROBLEM: BadStatusLine in validate\_zcontroller()

The traceback must look like the following to blame it to Z-controller.
This happens during zbcommit at the validation stage or in any stage
that requires to connect to the local zenoss JSON API. The call failed
because zenoss might be busy or one of its services (zope, zenhub,
etc..) might be unhealthy.

\[root@VA1ZGPZCNTL13 messaging\]\# cd /home/zenoss/zcomms/messaging &&
env PYTHONPATH=/home/zenoss python helpers/zb\_commit.py --zb-commit
--check-guid -a "\$auth" -r manifest\_ca1\_r82\_zgp
manifest\_sg1\_r82\_zgp manifest\_au1\_r82\_zgp

Running Z-Controller Dispatcher Validate Devices ...

Traceback (most recent call last):

File "helpers/zb\_commit.py", line 192, in &lt;module&gt;

args.check\_guid)

File "helpers/zb\_commit.py", line 77, in validate\_zcontroller

dev\_dict = dev\_uid\_dict()

File "/home/zenoss/zcomms/messaging/zcontroller\_tasks.py", line 59, in
dev\_uid\_dict

zen = ZenossAPI()

File "/home/zenoss/zcomms/messaging/zenoss\_api.py", line 49, in
\_\_init\_\_

loginParams)

File "/usr/lib64/python2.6/urllib2.py", line 391, in open

response = self.\_open(req, data)

File "/usr/lib64/python2.6/urllib2.py", line 409, in \_open

'\_open', req)

File "/usr/lib64/python2.6/urllib2.py", line 369, in \_call\_chain

result = func(\*args)

File "/usr/lib64/python2.6/urllib2.py", line 1190, in http\_open

return self.do\_open(httplib.HTTPConnection, req)

File "/usr/lib64/python2.6/urllib2.py", line 1163, in do\_open

r = h.getresponse()

File "/usr/lib64/python2.6/httplib.py", line 1012, in getresponse

response.begin()

File "/usr/lib64/python2.6/httplib.py", line 404, in begin

version, status, reason = self.\_read\_status()

File "/usr/lib64/python2.6/httplib.py", line 368, in \_read\_status

raise BadStatusLine(line)

httplib.BadStatusLine

Attempt to check if port 8080 (http service) of Z-controller can be
opened in a browser. If not, try to restart Z-controllers' zenoss
instance. You can also look at zenoss logs (/opt/zenoss/log) to check
 the health of zenoss services.

#### PROBLEM: Provisioner: Can't retry zcomms.provisioner.provisioner.poll\_modeling\_status

The traceback looks like:

Traceback (most recent call last):

File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 240,
in tracetask

R = retval = fun(\*args, \*\*kwargs)

File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 437,
in \_\_protected\_call\_

return self.run(\*args, \*\*kwargs)

File "/home/zenoss/zcomms/provisioner/provisioner.py", line 716, in
poll\_modeling\_status

self.retry()

File "/usr/lib/python2.6/site-packages/celery/app/task.py", line 665, in
retry

self.name, request.id, S.args, S.kwargs))

MaxRetriesExceededError: Can't retry
zcomms.provisioner.provisioner.poll\_modeling\_status\[92a9e059-38d7-4efc-a72d-2459d0222aeb\]
args:(u'WA1R82ZGPZNODE11',) kwargs:{}

**Explanation: **This timeout is on the polling task that checks if
modeling of devices is already done for a certain z-node. There might be
other corner cases that will cause this timeout exception to be
triggered.

**ACTION: **You can close the ticket immediately and document the issue
in Trello under Prod Ops issue for Prem & Jerome to triage.

History of cards that tackled this issue:

<https://trello.com/c/ZAZD4fyl/3586-can-t-retry-zcomms-provisioner-provisioner-poll-modeling-status-5ff71643-d875-4d6b-9d7c-5291de92509e>

#### **Problem: **<celery@heartbeat.xxxxxxxxxxxxxx.DC> **worker tasks are backing up.**

**Sample
ticket:** <https://cascadeo.zendesk.com/agent/tickets/317798>, <https://cascadeo.zendesk.com/agent/tickets/341541>

**Overview:** New threshold to monitor if the worker tasks are backing
up.

**Resolution:**

-   You can close the ticket if it is not persistent from the indicated
    node in the ticket.

-   If it is persistent, try restarting celery-heartbeat app in the node
    indicated.

\#supervisorctl restart celery-heartbeat

-   If it still persists, escalate as an emergency.

#### Problem: No new ZenBackup image in ZController

**Background**

This happens because the z-node (which is not part of a config push)
wrongly propagates the latest zenbackup image seen from the set of
zenbackup images shipped from Z-controller. The latest symlink is
updated everytime zbcommit is run in Z-controller regardless of the DC’s
included in zbcommit. See below when the flag / alert happens.

This recipe  a temporary measure while we architect the permanent fix in
<https://trello.com/c/8SZQFmLl/3651-invalid-no-new-zenbackup-image-alerts-was-provisioner-seeding-znode-failure-in-de1-gb3-wa1-and-ny1>.

**Sample error message**

No new ZenBackup image in ZController: 1478641938. Latest zb\_version in
Z-Node WA1R82ZGPZNODE09 is: 1478662757. Check 'zboutput\_ver' and
mapping 'version' in the manifest!

**Reference ticket**

<https://cascadeo.zendesk.com/agent/tickets/349302>

**Notations**

In the example above, let’s call this timestamp (epoch time)
*1478641938* the “expected zenbackup image”. This version is taken from
the manifest field “zb\_version”. (Denote as *zenbackup-T1*)

Consider the timestamp *1478662757* as the “zenbackup image propagated
by the z-node to the provisioner state table”. (Denote as
*zenbackup-T2*)

**When it is flagged**

The alert is triggered when *zenbackup-T1* is less than *zenbackup-T2*.

**Triage steps**

-   Check the message if valid (if *zenbackup-T1* exists in the set of
    zenbackup images shipped from z-controller to the z-node).

SSH in the affected node.

List the zenbackup images under /home/zenoss/zb directory.

\[root@WA1R82ZGPZNODE09 \~\]\# ls -l /home/zenoss/zb

total 888888

lrwxrwxrwx 1 root   root         35 Nov  9 03:55 last\_applied -&gt;
/home/zenoss/zb/zboutput.1478662757

lrwxrwxrwx 1 root   root         35 Nov  9 03:40 latest -&gt;
/home/zenoss/zb/zboutput.1478662757

-rw-rw-r-- 1 zenoss zenoss 90699097 Nov  2 01:54 zboutput.1478051600

-rw-rw-r-- 1 zenoss zenoss 90708576 Nov  2 07:27 zboutput.1478071559

-rw-rw-r-- 1 zenoss zenoss 90717200 Nov  3 00:04 zboutput.1478131338

-rw-rw-r-- 1 zenoss zenoss 90715029 Nov  3 02:00 zboutput.1478138329

-rw-rw-r-- 1 zenoss zenoss 90723914 Nov  3 05:11 zboutput.1478149815

-rw-rw-r-- 1 zenoss zenoss 90734795 Nov  5 15:32 zboutput.1478359844

-rw-rw-r-- 1 zenoss zenoss 90734645 Nov  5 16:40 zboutput.1478363918

-rw-rw-r-- 1 zenoss zenoss 91721777 Nov  8 17:06 zboutput.1478624674

-rw-rw-r-- 1 zenoss zenoss 91719750 Nov  8 21:53 zboutput.1478641938

-rw-rw-r-- 1 zenoss zenoss 91719768 Nov  9 03:40 zboutput.1478662757

-   Look for *zenbackup-T1*.

-rw-rw-r-- 1 zenoss zenoss 91719750 Nov  8 21:53 zboutput.1478641938

The example shows that zenbackup-T1 exists. The note is therefore
*VALID*.

-   If zenbackup-T1 exists and you do not want the alerts to recur,
    adjust “zb\_version” in the manifest to equal *zenbackup-T2*.

    -   Or you can tell NOC T1 to ignore and close temporarily until
        <https://trello.com/c/8SZQFmLl/3651-invalid-no-new-zenbackup-image-alerts-was-provisioner-seeding-znode-failure-in-de1-gb3-wa1-and-ny1>
        is fixed.

#### PROBLEM: ConnectionError: ('Connection aborted.', BadStatusLine('',)) in provisioners

Look closely at the traceback. The cases we have seen so far are the
following.

##### Case: The CLC (Centurylink Cloud) API call is failing

The traceback will look like the screenshot below. Notice the
ConnectionError happens after the CLC API call.

Figure: traceback of ConnectionError

Observe the events stream (see screenshot below how to get to the
Related Events) if it is persistent. If yes, create ticket
to <help@ctl.io> that includes the traceback. You can expand the
following calls to include in the ticket (see screenshots below on
getting the traceback for CLC API calls).

Figure: Related Events tab

Figure: getting the traceback for CLC API calls to include in the ticket
to <help@ctl.io>

##### Case: The manifest (inventory) fetch is failing

The traceback from zcomms.provisioner,heartbeat,flower looks like the
following.

Notice below the **ConnectionError** is raised right after the
**getAll()** call in **manifest.py**.

\[root@DE1R82ZGPPROVISIONER \~\]\# CTL\_MANIFEST\_DATABAG="zenoss"
CTL\_MANIFEST\_ITEM="manifest\_de1\_r82\_zgp" PYTHONPATH="/home/zenoss"
/usr/bin/celery flower --app=zcomms.provisioner.provisioner --port=5555
--broker=amqp://heartbeatuser:heartbeatpass@DE1R82ZGPRABBIT//heartbeat

\^@Traceback (most recent call last):\
File "/usr/bin/celery", line 11, in &lt;module&gt;\
sys.exit(main())\
File "/usr/lib/python2.6/site-packages/celery/\_\_main\_\_.py", line 30,
in main\
main()\
File "/usr/lib/python2.6/site-packages/celery/bin/celery.py", line 81,
in main\
cmd.execute\_from\_commandline(argv)\
File "/usr/lib/python2.6/site-packages/celery/bin/celery.py", line 769,
in execute\_from\_commandline\
super(CeleryCommand, self).execute\_from\_commandline(argv)))\
File "/usr/lib/python2.6/site-packages/celery/bin/base.py", line 305, in
execute\_from\_commandline\
argv = self.setup\_app\_from\_commandline(argv)\
File "/usr/lib/python2.6/site-packages/celery/bin/base.py", line 465, in
setup\_app\_from\_commandline\
self.app = self.find\_app(app)\
File "/usr/lib/python2.6/site-packages/celery/bin/base.py", line 485, in
find\_app\
return find\_app(app, symbol\_by\_name=self.symbol\_by\_name)\
File "/usr/lib/python2.6/site-packages/celery/app/utils.py", line 232,
in find\_app\
sym = imp(app)\
File "/usr/lib/python2.6/site-packages/celery/utils/imports.py", line
101, in import\_from\_cwd\
return imp(module, package=package)\
File "/usr/lib/python2.6/site-packages/importlib/\_\_init\_\_.py", line
37, in import\_module\
\_\_import\_\_(name)\
File "/home/zenoss/zcomms/provisioner/provisioner.py", line 64, in
&lt;module&gt;\
SECRETS = MANIFESTOBJ.getSecrets()\
File "/home/zenoss/zcomms/common/manifest.py", line 22, in getSecrets\
data = self.getAll()\
**File "/home/zenoss/zcomms/common/manifest.py", line 17, in getAll**\
**r = requests.get(self.manifesturl, headers=headers)**\
File "/usr/lib/python2.6/site-packages/requests/api.py", line 59, in
get\
return request('get', url, \*\*kwargs)\
File "/usr/lib/python2.6/site-packages/requests/api.py", line 48, in
request\
return session.request(method=method, url=url, \*\*kwargs)\
File "/usr/lib/python2.6/site-packages/requests/sessions.py", line 451,
in request\
resp = self.send(prep, \*\*send\_kwargs)\
File "/usr/lib/python2.6/site-packages/requests/sessions.py", line 557,
in send\
r = adapter.send(request, \*\*kwargs)\
File "/usr/lib/python2.6/site-packages/requests/adapters.py", line 407,
in send\
**raise ConnectionError(err, request=request)**\
**requests.exceptions.ConnectionError: ('Connection aborted.',
BadStatusLine('',))**

**Background**

Provisioners (and also z-nodes) fetch their manifest from Couchbase. The
fetch looks like this.

provisioner / znode &lt;-- local manifest cache (pouchcouch) &lt;--
couchbase sync gateway fleet &lt;-- couchbase cluster

**Triage steps**

-   Similar
    to <https://cascadeo.atlassian.net/wiki/pages/viewpage.action?spaceKey=CLCDEV&title=CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-PROBLEM:getSecrets():raiseHTTPError(http_error_msg,response=self)requests.exceptions.HTTPError:404ClientError:NotFound>

-   Create a production ops issue card for Prem if it is persistent

#### **PROBLEM: \[GLOBAL Z-CONSOLE\] VA1ZGPAPI05 Datasource HttpMonitor/HttpMonitor Swagger API Functionality command timed out**

**Background**: This is usually because of one of the API servers (API05
in the subject) is down.

Solution:

1.   Find node in question
    in <https://control.ctl.io/manage#/va1/group/66933ab7011840b4aea878722df9113b>

2.  Identify IP address, and browse http://&lt;ipaddress&gt;:8080/docs

3.  If the swagger doc above is not reachable, SSH in to the node.

4.  Execute \`pm2 list\` to check status of the app. A good output is
    shown below:

> \[root@VA1ZGPAPI05 \~\]\# pm2 list\
> ┌──────────┬────┬──────┬───────┬────────┬─────────┬────────┬─────┬───────────┬──────────┐\
> │ App name │ id │ mode │ pid │ status │ restart │ uptime │ cpu │ mem │
> watching │\
> ├──────────┼────┼──────┼───────┼────────┼─────────┼────────┼─────┼───────────┼──────────┤\
> │ z-api │ 0 │ fork │ 21737 │ online │ 88 │ 17m │ 0% │ 71.5 MB │
> enabled │\
> │ z-worker │ 1 │ fork │ 21743 │ online │ 6 │ 17m │ 0% │ 54.7 MB │
> enabled │\
> └──────────┴────┴──────┴───────┴────────┴─────────┴────────┴─────┴───────────┴──────────┘\
> Use \`pm2 show &lt;id|name&gt;\` to get more details about an app

1.  If any of the apps is down, restart app by running \`pm2 restart
    all\`

2.  If any of the app is still down, investigate logs in
    /var/log/zenoss-api.

3.  Verify by browsing  http://&lt;ipaddress&gt;:8080/docs 

#### PROBLEM: Provisioner \[DC\]R82ZGPPROVISIONER: maximum recursion depth exceeded while calling a Python object

Safe to ignore until this issue is resolved
<https://github.com/CenturyLinkCloud/clc-python-sdk/issues/39>.

Reference trello card: <https://trello.com/c/Tb9EdMDq/>

#### **PROBLEM: &lt;SOME DC&gt;PROVISIONER: "Response code 408” exception in provisioner.cleanup\_zgroup() call**

**\
**

**Background:**

This event is caused by CTL API error response in socket 408.

This can also be caused by supervisor restart in the provisioner. If so,
the alert can be disregarded unless it recurs for after the restart.

**Sample error message:**

&lt;SOME DC&gt;PROVISIONER: "Response code 408” exception in
provisioner.cleanup\_zgroup() call

**Reference ticket:**

<https://cascadeo.zendesk.com/agent/tickets/342147>

**Solution (s):**

1.  SSH  into the Znode and check the traceback. Check call
    cleanup\_zgroup log.

Traceback (most recent call last):

File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 240,
in trace*task*

*R = retval = fun(\*args, \*\*kwargs)*

*File "/usr/lib/python2.6/site-packages/celery/app/trace.py", line 437,
in \_\_protected\_call*\_

return self.run(\*args, \*\*kwargs)

File "/home/zenoss/zcomms/provisioner/provisioner.py", line 898, in
cleanup*zgroup*

*return provisioner.cleanup\_zgroup(manifest, STATEDB, clc\_creds,
CTL\_ENDPOINT, CTL\_SSLVERIFY)*

*File "/home/zenoss/zcomms/utils/provisioner.py", line 243, in
cleanup\_zgroup*

*g=clc.v2.Group(group, alias=account)*

*File "/usr/lib/python2.6/site-packages/clc/APIv2/group.py", line 139,
in \_\_init*\_

else: self.Refresh()

File "/usr/lib/python2.6/site-packages/clc/APIv2/group.py", line 158, in
Refresh

self.data = clc.v2.API.Call('GET','groups/%s/%s' % (self.alias,self.id))

File "/usr/lib/python2.6/site-packages/clc/APIv2/api.py", line 137, in
Call

raise(e)

**APIFailedResponse: Response code 408.
&lt;html&gt;&lt;body&gt;&lt;h1&gt;408 Request Time-out&lt;/h1&gt;**

**Your browser didn't send a complete request in time.**

&lt;/body&gt;&lt;/html&gt;

1.  Monitor for 10-15 mins and check the zendesk if the event is
    recurring.

2.  Check /var/log/celery/celery-provisioning.log if succeeding calls to
    cleanup\_zgroup are succeeding (see example above).

3.  If the event is succeeding, resolve the ticket  as a temporary
    issue. Else create a card in Trello as this is a client side issue.

#### RECIPE: BULK UPDATE DATACENTER MANIFEST

Manual page of the tool:

\[In chef-workstation zenoss-cookbooks\]\# python
/root/zenoss-cookbooks/scripts/sync-gw-manifest-update.py --help

Examples:

To check current values of drop\_zenperfdf\_msg\_forwarderlagsec:

\[In chef-workstation zenoss-cookbooks\]\# 

python /root/zenoss-cookbooks/scripts/sync-gw-manifest-update.py \\

-s http://&lt;prod-sync-gw-ip&gt;:4984/zenoss\_databag/ -l ALL -r r82 -d
drop\_zenperfdf\_msg\_forwarderlagsec

To update the field value:

\# python sync-gw-manifest-update.py -s
http://&lt;prod-sync-gw-ip&gt;:4984/zenoss\_databag/ -l ALL \\

-r &lt;REPLACE WITH RELEASE NUMBER e.g. r82&gt; -o
'{"drop\_zenperfdf\_msg\_forwarderlagsec": "true"}' \\

-a &lt;REPLACE WITH AUTH HASH&gt;

#### Resource: VA1ZGPSYNCGW{02,03,04 or more} Component: / Event Class: /Perf/Filesystem Status: New Message: threshold of Greater than &lt;SOME PERCENTAGE THRESHOLD&gt; percent used not met: current value &lt;SOME VALUE&gt;

The approach below assumes that the disk is mostly consumed by sync
gateway server logs. You will notice this when you inspect the size of
the log files (access or error logs).

Look where 10.128.131.220 (VIP for Couchbase Sync Gateway cluster) is.
You can SSH to it and verify if nginx is on it.

The real servers are declared in /etc/nginx/conf.d/default.conf (this
location might change soon).

\`\`\`\
\#\
\# The default server\
\#\
upstream sync\_gateway {\
server 127.0.0.1:4984;\
server 10.128.131.77:4984;\
server 10.128.131.136:4984;\
}\
\`\`\`

SSH to each server and execute:

-   Stop sync gateway

initctl stop sync\_gateway

-   Delete all logs in /home/sync\_gateway/logs (BE CAREFUL!!!)

\# cd /home/sync\_gateway/logs/

**(After changing to the directory above! You have been warned)**

/home/sync\_gateway/logs \# \\rm -f \*

-   Start sync gateway

initctl start sync\_gateway

#### PROBLEM: SEEDING IS STILL NOT TRIGGERED EVEN AFTER INCREMENT OF MANIFEST VERSION

**Symptom:**

In /var/log/celery/celery-heartbeat.log you can see a different version
seen by zcomms.heartbeat.

Example: Even if you already incremented the version to a later date
(2016112200), the logs still show:

\[2016-11-22 17:20:20,283: INFO/Worker-2\] ZNode AU1R82ZGPZTRAP03 is
already using the latest manifest version ***2016111500*.**\
\[2016-11-22 17:20:20,283: INFO/Worker-2\] ZNode AU1R82ZGPZTRAP02 is
already using the latest manifest version 2016111500.\
\[2016-11-22 17:20:20,284: INFO/Worker-2\] ZNode AU1R82ZGPZTRAP01 is
already using the latest manifest version 2016111500.\
\[2016-11-22 17:20:20,284: INFO/Worker-2\] ZNode AU1R82ZGPZNODE06 is
already using the latest manifest version 2016111500.\
\[2016-11-22 17:20:20,285: INFO/Worker-2\] ZNode AU1R82ZGPZNODE05 is
already using the latest manifest version 2016111500.\
\[2016-11-22 17:20:20,285: INFO/Worker-2\] ZNode AU1R82ZGPZNODE04 is
already using the latest manifest version 2016111500.\
\[2016-11-22 17:20:20,286: INFO/Worker-2\] ZNode AU1R82ZGPZNODE03 is
already using the latest manifest version 2016111500.\
\[2016-11-22 17:20:20,287: INFO/Worker-2\] ZNode AU1R82ZGPZNODE02 is
already using the latest manifest version 2016111500.\
\[2016-11-22 17:20:20,287: INFO/Worker-2\] ZNode AU1R82ZGPZNODE01 is
already using the latest manifest version 2016111500.\
\[2016-11-22 17:20:20,288: INFO/Worker-2\] ZNode AU1R82ZGPZMASTER is
already using the latest manifest version 2016111500.

**Triage:**

-   Compare the revisions of the manifest. Get the revision from
    pouchcouch (http://&lt;PROVISIONER\_IP&gt;:3000) and compare it with
    the revision you get from Postman (GET from Sync Gateway).

-   If they are different, pouchcouch could be behind. (Theory: the
    retry time could already be very long because of the sync gateway
    cluster load issue. The pouchcouch instance was not restarted after
    we introduced the temporary remediation for the sync gateway
    cluster.)

-   Restart pouchcouch to force an immediate resync.

\[root@AU1R82ZGPPROVISIONER \~\]\# pm2 restart www

\[PM2\] Applying action restartProcessId on app \[www\](ids: 0)

\[PM2\] \[www\](0) ✓

┌──────────┬────┬──────┬──────┬────────┬─────────┬────────┬────────────┬──────────┐

│ App name │ id │ mode │ pid │ status │ restart │ uptime │ memory │
watching │

├──────────┼────┼──────┼──────┼────────┼─────────┼────────┼────────────┼──────────┤

│ www │ 0 │ fork │ 8706 │ online │ 4 │ 0s │ 5.738 MB │ disabled │

└──────────┴────┴──────┴──────┴────────┴─────────┴────────┴────────────┴──────────┘

Use \`pm2 show &lt;id|name&gt;\` to get more d

-   Compare again the revisions. They should be already the same.

-   Check the state of the z-nodes, they should queueing already for
    seeding.

#### PROBLEM: Disk space issue for /var/lib/mysql

Sample ticket: <https://cascadeo.zendesk.com/agent/tickets/385418>

**Solution:**

-   Replace the znode for disk space issues on /var/lib/mysql. If this
    issue persists across multiple znodes escalate to T3.**\
    **\
    - T3 needs to shrink the MySQL ibdata files on the z-controller per
    instructions here then zb\_commit on all DCs 

-   card
    reference: <https://trello.com/c/9ZcfOSlA/3547-shrink-mysql-ibdata1-in-z-controller>

 

2016-11-18 02:45:53,451 ERROR zen.python: gb3-vc-a02.t3n.dom-vsphere 300
vsphere-cluster-metrics unhandled plugin error: (vmodl.RuntimeFault) {\
dynamicType = &lt;unset&gt;,\
dynamicProperty = (vmodl.DynamicProperty) \[\],\
msg = "This operation is restricted by the administrator -
'vpxd.stats.maxQueryMetrics'. Contact your system administrator.",\
faultCause = &lt;unset&gt;,\
faultMessage = (vmodl.LocalizableMessage) \[\]\
}

#### PROBLEM: \[DC\]PROVISIONER: Cannot replace ztrap at the moment. Check overall ztrap health.

Sample ticket: <https://cascadeo.zendesk.com/agent/tickets/374897>

This is informational and that it is triggered because you cannot
replace all ztraps at the same time.

#### PROBLEM: Task configLoader configure failed

Background:

There  could be an issue with Zenoss that is most probably related with
zenhub.

Sample error message:

ERROR zen.collector.config: Task configLoader configure failed:
\[Failure instance: Traceback (failure with no frames): &lt;class
'twisted.internet.error.ConnectionDone'&gt;: Connection was closed
cleanly.

Reference ticket:

<https://cascadeo.zendesk.com/agent/tickets/350174>

**Solution (s):**

1.  Look into the Znode and
    [remodel](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-HOWTO:ReducetheworkloadonarunningZ-Nodebyrebalancing)
    the affected device.

  Monitor for 10 minutes if the error is persistent.

     2. If the same error persist. Remodel the device in debug mode.
Monitor for 10 minutes.

SSh into the znode.

\# zenmodeler run -v10 -d gb3-vc-m01.t3n.dom-vsphere

-   Else, use tools such as WinSCP to get the file. Create a trello card
    and attach the debug files for further review of the CTL Team. Save
    the output to a file.

Example:

\# zenmodeler run -v10 -d gb3-vc-m01.t3n.dom-vsphere &gt; output.file
2&gt;&&1

     3. Re-try to restart the zenoss stack and then re-model.

\# su zenoss

\# zenoss stop; zenoss start;

     4. Re-try replacing the znode and check if modeling now works.

Force Z-Node replacement on the Z-Master using "del". (see Forcing
Z-Node Replacement)

\# redis-cli

redis 127.0.0.1:6379&gt; del ZMASTER\_INSTANCE\_NAME

exception\
\[9:04\]  Unable to replace un-SEEDED znode. Set force to true to force
replacement.

\# snmpwalk -v2c -c&lt;SNMP COMMUNITY REMOVED&gt; 10.124.15.98
systemSNMPv2-MIB::sysDescr.0 = STRING: Linux UC1T3NPLATDNS01
3.13.0-79-generic \#123-Ubuntu SMP Fri Feb 19 14:27:58 UTC 2016 x86\_64

#### PROBLEM: &lt;urlopen error  \[[Errno 111](file:///C:\wiki\pages\createpage.action%3fspaceKey=CLCDEV&title=Errno+111&linkCreation=true&fromPageId=43909190)\] Connection refused&gt;

**Information**: This is a hint that the call to the z-node zenoss JSON
API failed probably because the z-node is unhealthy or down

**Solution(s)**:The Action is to ignore unless recurring

The traceback must contain:

File "/home/zenoss/zcomms/Zenoss/[zenoss.py](http://zenoss.py/)", line
111, in getComponents\
return self.\_router\_request('DeviceRouter', 'getComponents',
\[data\])\
File "/home/zenoss/zcomms/Zenoss/[zenoss.py](http://zenoss.py/)", line
66, in \_router\_request\
return json.loads(self.urlOpener.open(req, reqData,
timeout=APITIMEOUT).read())

If it persists, inspect the z-node and consider replacing it

**Notes:** Kindly add the event in this trello card
: <https://trello.com/c/ZwbM26tN>

#### PROBLEM: \[zenoss\] &lt;device name&gt; vSphere Connection / authentication failed

**Sample event: **

\[zenoss\] il1-vc-std03.t3n.dom-vsphere  vSphere Connection /
authentication failed - Component: IL1STD03CL01

**Solution(s)**: 

1.  Upon receiving the alert, acknowledge the event directly on the
    zNode that generated the event. This is to prevent further
    escalation to CTL after 30 minutes (if event is still not
    acknowledged). If you fail to acknowledge the event wiithin 30
    minutes, it's possible a ticket is already generated for CTL. So
    search first if a ticket is already generated for CTL. If that's the
    case no need to proceed with the steps below, but monitor the said
    ticket in case CTL passes it back to us for investigation. If CTL
    asks as for further investigation, you can follow the steps below
    for initial findings. If CTL requires more information or
    investigation, then you can assign to members of the Cascadeo CTL
    dev team/support (**Peter - primary vSphere dev, Jared, Prem,
    Jerome, Leo**)

2.  Check if the zVSphereUsername and zVSpherePassword are configured
    for the device. They should not be empty. zVSphereUsername should
    have a value of "t3n\\svc\_zenoss"

3.  Also take note if the device suddenly stop collecting, meaning there
    are graphs before but suddently stopped.

4.  If zVSphereUsername and zVSpherePassword are configured, try to
    model the device:\
    **zenmodel run -d device\_name**

5.  Also try to run zenpython collection on the device:\
    **zenpython run -d device\_name**

6.  For zenpython collection, once you observed the authentication
    failed error, you can abort its run by pressing Ctrl + C. If vSphere
    Connection / authentication failed is present, take note if there
    are any other errors that might be related to it. If you see
    **'vpxd.stats.maxQueryMetrics'. Contact your system administrator**,
    there's a separate recipe for this in the wiki so follow that. For
    any any other errors, take note of that.

7.  Wait for around 10 minutes and try to do steps 4 and 5 again. If the
    authentication failed error still persist, escalate the issue to CTL
    NOC. Indicate that the said vSphere device is encountering
    authentication issue prevent collection. It's also possible that the
    vCenter device itself have issues with its API (like being
    unresponsive) thus the alert. Please put any useful logs in the
    ticket. Also make sure to specify the IP address of the device. Also
    remove the -event and -vsphere suffix of the device name when put it
    in the ticket.

#### **PROBLEM: &lt;SOME DATACENTER&gt; PROVISIONER hasn't checked in**

**Sample ticket:** <https://cascadeo.zendesk.com/agent/tickets/383445>

**Note:** Run in verbose mode the script that pings the DMS.

**Solution(s):**

1.  SSH to the affected Provisioner and run the following commands:

    1.  \[root@GB3R82ZGPPROVISIONER \~\]\# crontab -l *(this is the
        script that pings the DMS)*

    2.  \[root@GB3R82ZGPPROVISIONER \~\]\# cat
        /usr/local/bin/report\_provisione.sh

    3.  \[root@GB3R82ZGPPROVISIONER \~\]\# cat /etc/snitchconfig

2.  Match the snitch ID in DMS. (Go to the provisioner in question and
    check if matched with the snitch ID you get from the ChefWS. (Sample
    image below is the URL of the GB3R82ZGPPROVISIONER in DMS).

3.  Run below code  again in terminal and check if the node is healthy

    1.  \[root@GB3R82ZGPPROVISIONER
        \~\]\# /usr/local/bin/report\_provisioner.sh -v

4.  Check on the DMS if the provisioner has checked in. Then close the
    ticket.

5.  If the z-node is not healthy, address the issue specified in the
    output. If the issue is not in this recipe or entire runbook, create
    a Prod Ops issue Trello card for CTL Devops and ask for a recipe

**Resolution**:

1.  In the Z-Group’s Provisioner, inspect
    /var/log/celery/celery-provisioning.log. Search for the keyword
    “Exception occurred.. Attempting to recreate server..”. Scroll down
    until traceback is seen.

    1.  If the error is caused by API failure such as shown below,
        create a ticket to the Tier3 NOC to fix the issue.

    2.  APIFailedResponse: Response code 400.  The request is invalid.
        POST <https://api.ctl.ioservers/ZGP>

    3.  APIFailedResponse: Response code 400.  CPU limit exceeded -&gt;
        available: 0, requested: 4
        POST [https://api.ctl.io](https://api.ctl.io/)

    4.  APIFailedResponse: Response code 400.  Memory limit exceeded
        -&gt; available: 0, requested: 4
        POST [https://api.ctl.io](https://api.ctl.io/)

    5.  APIFailedResponse: Response code 500.  An error has occurred.
        POST <https://api.ctl.io/v2/servers/ZGP> (**FIX**: Try manually
        creating a CentOS 6 server in the datacenter in question. If it
        fails, find the blueprint and build log
        in <https://control.ctl.io/Queue> (filter failed and
        datacenter). Report the build log to help@ctl.io)

    6.  For other issues not documented you can use [this recipe to
        triage CTL's Control
        API](https://cascadeo.atlassian.net/wiki/pages/viewpage.action?spaceKey=CLCDEV&title=CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-HOWTO:VerifyCTL/PlatformAPIIssue).

 

1.  This error could also be caused by multiple reprovisioning of znodes
    due to heartbeat or health failure. If so, fix znode issue first
    before proceeding to the next step.

    1.  Once the root cause is fixed, reprovisioning of nodes can be
        restarted by executing the following in the provisioner node.

                                                    i.     \$ redis-cli

                                                   ii.     redis
127.0.0.1:6379&gt; del heartbeat\_timeout provisioning\_timeout

                                                  iii.     redis
127.0.0.1:6379&gt; del &lt;NODENAME&gt;

                                                  iv.     redis
127.0.0.1:6379&gt; quit

                                                   v.     **or:** \#
redis-cli hgetall heartbeat\_timeout; redis-cli hgetall
provisioning\_timeout

                                                  vi.     \# redis-cli
del provisioning\_timeout 

3.     The provisioner will then try to create the node that was deleted
in the state table. Inspect /var/log/celery/celery-heartbeat.log for any
issues.

a.     If you don't see a blueprint / build queued
in <https://control.ctl.io/Queue> (filter by pending and datacenter)
after around 5 minutes, try to restart the supervisor process and retry
reprovisioning the node in question 

b.     \# supervisorctl stop celery-heartbeat celery-provisioning

c.      \#redis-cli

d.     del &lt;znode&gt;

e.     exit

f.       \# supervisorctl start celery-heartbeat celery-provisioning

4.     If no error was identified in the celery-provisioning.log,
try resetting the timeout and then trigger replacement. Then tail
celery-provisioning log for inspect error.  

5.     If you still get an error, create a ticket by sending an email
to [help@ctl.io](mailto:noc@tier3.com) CC <ctl@cascadeo.com.> Include
the traceback error and your [Support
PIN](https://cascadeo.atlassian.net/wiki/display/CLCDEV/CTL+Zenoss+Incident+Response+Recipes#CTLZenossIncidentResponseRecipes-ChecklistforEscalatedSupport) in
the email. The issue will be handled by CTL's NOC. Updates will go the
requester and <ctl@cascadeo.com>. 

#### Re: \[Sentry\] \[Cascadeo Internal\] &lt;SOME EXCEPTION MESSAGE&gt;

Example: <https://cascadeo.zendesk.com/agent/tickets/410929>

Notice *this is different* from a Sentry notification with the
subject Re: \[Sentry\] \[Cascadeo zcomms\] ERROR
(example: <https://cascadeo.zendesk.com/agent/tickets/406680>). The
latter is from the zcomms project while the former is from the internal
(to Sentry) project in Sentry.

You can close the ticket and move to Trello (assign to Prem) to deep
dive the Sentry tool.

#### How to modify the IP address of a device if requested by CTL teams

 1. Go to <http://10.128.131.39:8080/docs/#!/Device/setManageIp>

 2. Click "Device" to expand then
choose [/devices/{dc}/{name}/setManageIp/{ipaddress}](http://10.128.131.39:8080/docs/#!/Device/setManageIp)

Note: Go to <http://10.128.131.100/inventory> to check the device
inventory details.

3\. Input the data center name in "**dc**" field where the device is
hosted and in the "**name**" field input the name of device

4\. Lastly, put the new management IP address of the device in "**ip
address**" field.

5\. Click "**Try it out**!" button to take effect. 

#### How to re-mediate Z-console slow down

Two options available to solve this problem:

1.  Re-index via zendmd 

2.  clean mysql data dir and restore zenbackup

##### **Re-index via zendmd**

SSH to the z-console and execute the following:

\# change to zenoss user\
su - zenoss

\# run zendmd\
zendmd

\# while in python/zendmd interpreter\
reindex()\
exit()

\# restart zenoss\
zenoss restart

\# Check zodb integrity\
zenossdbpack\
zodbscan\
findposkeyerror -v10

##### Clean mysql data dir and restore zenbackup

SSH to the z-console and execute the commands below:

Shrink ibdata

\# BEFORE, check size\
ls -l /var/lib/mysql/ | grep ib\
\# As zenoss, backup\
su - zenoss\
zenbackup --no-perfdata --no-eventsdb --no-zepindexes\
\# note the zenbackup file - /opt/zenoss/backups/zenbackup\_xxxxxx.tgz\
exit

\# As root, stop services\
/etc/init.d/zenoss stop\
/etc/init.d/mysql stop\
/etc/init.d/rabbitmq-server stop

\# Move ibdata files to tmp folder\
mv -f /var/lib/mysql/ib\* /tmp

\# Start services\
/etc/init.d/mysql start\
/etc/init.d/rabbitmq-server start

\# As zenoss, restore backup\
su - zenoss\
zenrestore --file=/opt/zenoss/backups/zenbackup\_xxxxx.tgz

\# Recreate zodb\_session db\
grep zep-password /opt/zenoss/etc/global.conf\
zep-password xxxxxx \# get password\
mysql -p\
Enter password: xxxxxx\
...\
mysql&gt; show databases;\
drop database zodb\_session; create database zodb\_session;\
mysql&gt; show databases;

\# Start zenoss\
zenoss start

\# Attempt to login to Zenoss UI.

1.  useful logs in the ticket. Also make sure to specify the IP address
    of the device. Also remove the -event and -vsphere suffix of the
    device name when put it in the ticket.

\# Check zodb integrity\
zenossdbpack\
zodbscan\
findposkeyerror -v10

\# After, check size\
ls -l /var/lib/mysql/ | grep ib

\# Cleanup if all goes well\
rm -f /tmp/ib\*

**Notes: **

Shrinking ib data is only necessary if disk is full, but still try if
issue persists. 

#### **PROBLEM: Unable to update ZNODE details in Z-Console - needs manual update**

#### **PROBLEM: Unable to set state of &lt;ZNODE&gt; to production in z-console. Reset state manually in z-console**

**Background:** Provisioner automatically updates zconsole once a znode
has been reprovisioned. There are times, however, that z-console become
unresponsive or a bug prevents the provisioner from updating the
z-console. In which case a ticket is generated to update z-console.
Before running the steps below, make sure that the underlying z-console
issues are resolved first - e.g. zenoss service is not running, etc.

**Solution(s):**

1.  SSH to zconsole 10.128.131.100

2.  Execute \`\`\`python /opt/zconsole/scripts/update\_znodes.py admin
    &lt;zconsole admin password&gt;\`\`\`

#### **PROBLEM: Error running parser error**

**Refence Ticket:** Sample ticket Ticket 154359 : \[GLOBAL Z-CONSOLE\]
GB3R8RC2ZGPZTRAP01 Error
running parser&lt;Products.DataCollector.Plugins.PluginLoader instance
at 0xb66d290&gt;

**Solution(s):**

1.  Check the node if it is being replaced. If yes, it is related to
    replacement.

2.  Once the replacement is done, clear the event manually.

3.  If it re-occurs (while node is not being replaced). Investgate/check
     status of rabbitmq in the znode. 

#### **PROBLEM: **ReadConflictError in NODE\_NAME, device DEVICE\_NAME" &lt; --- title message = "DEVICE\_NAME modeling encountered 'ReadConflictError: database read conflict error

**Sample Ticket:** <https://cascadeo.zendesk.com/agent/tickets/437733>

**Solution(s):**

1.  [Re-seed the z-node](https://goo.gl/ITvN6m). Wait for the z-node to
    be in the SEEDED state.

2.  If the device related still doesn't show in DMS,

    1.  SSH to the z-node 

        1.  ssh\_node &lt;Node DNS&gt;

    2.  Login as the zenoss user and remodel the device

        1.  su - zenoss

        2.  zenmodeler run -d &lt;device name&gt;

3.  If the ReadConflictError (RCE) exception keeps coming back making
    modeling impossible, create a Trello card under Production Ops
    Issues and assign to CTL Devops.

**Validation:** The last modeled time should be close to the current
time or when last modeled.

#### PROBLEM: \[zenoss\] global z-console from &lt;DC&gt;z-console-zenoss-http-check Datasource HttpMonitor - ZENOSS/ZENOSS command timed out

#### **PROBLEM: HTTPmonitor connection timed out from &lt;DC&gt; to va1**

**Background:** This is a Ping test if zconsole is reachabe from other
DC's. Verify the problem using ping and mtr command.

**Solution (s):**

1.   SSH into the "IP" indicated in event details of the ticket.

2.  Ping or use traceroute(MTR) in any VA1 server in 10.128.131.0/24
    subnet. If there is a reply, VA1 is reachable.

Example ticket :

https://cascadeo.zendesk.com/agent/tickets/412670

Event Detail:
http://10.81.25.35:8080/zport/dmd/Events/viewDetail?evid=000c29a4-9454-92e5-11e6-cdc39fe7481d

Indicated IP = 10.81.25.35 (WA1R82ZGPZTRAP07)

\#**Ping test from WA1 to VA1(zconsole)**

> \[root@VA1ZGPCHEF-W01 \~\]\# ssh 10.81.25.35
>
> \[root@WA1R82ZGPZTRAP07 \~\]\# ping 10.128.131.100
>
> PING 10.128.131.100 (10.128.131.100) 56(84) bytes of data.
>
> 64 bytes from 10.128.131.100: icmp\_seq=1 ttl=62 time=70.0 ms
>
> 64 bytes from 10.128.131.100: icmp\_seq=2 ttl=62 time=70.0 ms
>
> 64 bytes from 10.128.131.100: icmp\_seq=3 ttl=62 time=70.1 ms
>
> 64 bytes from 10.128.131.100: icmp\_seq=4 ttl=62 time=70.0 ms
>
> 64 bytes from 10.128.131.100: icmp\_seq=5 ttl=62 time=69.9 ms

\#**MTR test from WA1 to VA1(zconsole)**

>  \[root@WA1R82ZGPZTRAP07 \~\]\# mtr -rw -c 30 10.128.131.100
>
>  Start: Tue Jan  3 15:30:36 2017
>
>  HOST: WA1R82ZGPZTRAP07 Loss%   Snt   Last   Avg  Best  Wrst StDev
>
>   1.|-- 10.81.25.1        0.0%    30    0.4   0.3   0.3   0.4   0.0
>
>   2.|-- 206.128.131.38   46.7%    30   69.9  69.9  69.8  70.2   0.0
>
>   3.|-- 10.128.131.100    0.0%    30   70.1  70.1  69.9  70.9   0.0

#### **Problem: XXXR82ZGPPROVISIONER \[Errno 32\] Broken pipe**

**Information**: Trace back error should look like this.

Traceback (most recent call last):

File
"/usr/lib/python2.6/site-packages/celery/app/[trace.py](http://trace.py/)",
line 240, in tracetask\
R = retval = fun(*args, \*\*kwargs)\
File
"/usr/lib/python2.6/site-packages/celery/app/[trace.py](http://trace.py/)",
line 437, in \_protected\_call\
return self.run(*args, \*\*kwargs)\
File
"/home/zenoss/zcomms/heartbeat/[heartbeat.py](http://heartbeat.py/)",
line 109, in run\
self.provisioner\_heartbeat()\
File
"/home/zenoss/zcomms/heartbeat/[heartbeat.py](http://heartbeat.py/)",
line 152, in provisioner\_heartbeat\
self.\_monitor\_celery\_workers()\
File
"/home/zenoss/zcomms/heartbeat/[heartbeat.py](http://heartbeat.py/)",
line 294, in \_monitor\_celery\_workers\
workers = app.control.inspect().reserved()\
File
"/usr/lib/python2.6/site-packages/celery/app/[control.py](http://control.py/)",
line 87, in reserved\
return self.\_request('dump\_reserved', safe=safe)\
File
"/usr/lib/python2.6/site-packages/celery/app/[control.py](http://control.py/)",
line 71, in \_request\
timeout=self.timeout, reply=True,\
File
"/usr/lib/python2.6/site-packages/celery/app/[control.py](http://control.py/)",
line 307, in broadcast\
limit, callback, channel=channel,\
File
"/usr/lib/python2.6/site-packages/kombu/[pidbox.py](http://pidbox.py/)",
line 294, in \_broadcast\
serializer=serializer)\
File
"/usr/lib/python2.6/site-packages/kombu/[pidbox.py](http://pidbox.py/)",
line 259, in \_publish\
maybe\_declare(self.reply\_queue(channel))\
File
"/usr/lib/python2.6/site-packages/kombu/[common.py](http://common.py/)",
line 113, in maybe\_declare\
return \_maybe\_declare(entity, declared, ident, channel)\
File
"/usr/lib/python2.6/site-packages/kombu/[common.py](http://common.py/)",
line 120, in \_maybe\_declare\
entity.declare()\
File
"/usr/lib/python2.6/site-packages/kombu/[entity.py](http://entity.py/)",
line 521, in declare\
self.exchange.declare(nowait)\
File
"/usr/lib/python2.6/site-packages/kombu/[entity.py](http://entity.py/)",
line 174, in declare\
nowait=nowait, passive=passive,\
File
"/usr/lib/python2.6/site-packages/amqp/[channel.py](http://channel.py/)",
line 615, in exchange\_declare\
self.\_send\_method((40, 10), args)\
File "/usr/lib/python2.6/site-packages/amqp/abstract\_channel.py", line
56, in \_send\_method\
self.channel\_id, method\_sig, args, content,\
File "/usr/lib/python2.6/site-packages/amqp/method\_framing.py", line
221, in write\_method\
write\_frame(1, channel, payload)\
File
"/usr/lib/python2.6/site-packages/amqp/[transport.py](http://transport.py/)",
line 182, in write\_frame\
frame\_type, channel, size, payload, 0xce,\
File "&lt;string&gt;", line 1, in sendall\
error: \[Errno 32\] Broken pipe

**Solution(s):** Follow the recipe** \[MISSING\] &lt;Datacenter&gt;
RABBITMQ hasn'tcheckedin**

PROBLEM: \[zenoss\] global z-console from
&lt;DC&gt;z-console-zenoss-http-check Datasource HttpMonitor -
ZENOSS/ZENOSS command timed out\
Background: This is a Ping test if zconsole is reachabe from other DC's.
Verify the problem using the ping and mtr command.Cause : Packet drops
from other DC's to VA1 or vice versa.\
Solution (s): 1. SSH into the "IP" indicated in event details of the
ticket.  2. Ping or use traceroute(MTR) in any VA1 server in
10.128.131.0/24 subnet. If there is a reply, VA1 is reachable.\
example ticket :https://cascadeo.zendesk.com/agent/tickets/412670Event
Detail:
http://10.81.25.35:8080/zport/dmd/Events/viewDetail?evid=000c29a4-9454-92e5-11e6-cdc39fe7481d\
Indicated IP = 10.81.25.35 (WA1R82ZGPZTRAP07)\
\
\
\#Ping test from WA1 to VA1(zconsole)\
1. \[root@VA1ZGPCHEF-W01 \~\]\# ssh 10.81.25.352.
\[root@WA1R82ZGPZTRAP07 \~\]\# ping 10.128.131.100PING 10.128.131.100
(10.128.131.100) 56(84) bytes of data.64 bytes from 10.128.131.100:
icmp\_seq=1 ttl=62 time=70.0 ms64 bytes from 10.128.131.100: icmp\_seq=2
ttl=62 time=70.0 ms64 bytes from 10.128.131.100: icmp\_seq=3 ttl=62
time=70.1 ms64 bytes from 10.128.131.100: icmp\_seq=4 ttl=62 time=70.0
ms64 bytes from 10.128.131.100: icmp\_seq=5 ttl=62 time=69.9 ms\
\
\#MTR test from WA1 to VA1(zconsole)\
\[root@WA1R82ZGPZTRAP07 \~\]\# mtr -rw -c 30 10.128.131.100Start: Tue
Jan  3 15:30:36 2017HOST: WA1R82ZGPZTRAP07 Loss%   Snt   Last   Avg
 Best  Wrst StDev  1.|-- 10.81.25.1        0.0%    30    0.4   0.3   0.3
  0.4   0.0  2.|-- 206.128.131.38   46.7%    30   69.9  69.9  69.8  70.2
  0.0  3.|-- 10.128.131.100    0.0%    30   70.1  70.1  69.9  70.9   0.0

**Problem : localhost RRD Unable to save data for process-monitor RRD
&lt;link&gt;/cpu**

Manifestation : sample ticket
<https://cascadeo.zendesk.com/agent/tickets/412916>

Actions/Solution/s :\
1. Have the T2's relate it to a node replacement and consider the issue
resolve. If no correlation found, follow on next step.\
2. Create an escalation thru trello.

**HOWTO: Add subnets for auto-discovery**

Pre-requisites:

1.  Sync-Gateway credentials

2.  Postman client setup

Using Couchbase Sync Gateway - (Follow sync gateway
[setup](https://docs.google.com/presentation/d/1JjyovfWh-3CrbxURIzPgk0ySEKkvnVPxH6OY1hnhEAw/edit#slide=id.p)*)*

1.  Get current manifest setup using Postman.

2.  Copy the result for manifest revision.

3.  Paste the result from step 2 to the body of the PUT request.

4.  Look for the “ip\_subnets” section and add the new subnet.

5.  Submit the request. Make sure you enter the right credentials. If
    successful it will return a JSON response. See response below:

> {
>
> "id": "manifest\_de1\_r82\_zgp",
>
> "ok": true,
>
> "rev": "12776-11bbf69d104095918cee12122eec00c1"
>
> }

1.  Login to <https://control.ctl.io/> and get the login info for the
    DC’s z-master.

2.  SSH to the zmaster and run the ‘chef-client’ command. If successful
    will return a similar response.

3.  To confirm if new devices are discovered run the ff command:\
    /bin/bash -lc '/usr/bin/perl
    /usr/local/bin/perpetual-autodiscovery.l | /bin/logger -p info'

4.  Check the result using the ff command:

> cat /tmp/global.csv | grep &lt;new\_ip\_subnet&gt;
>
> Ex: cat /tmp/global.csv | grep 10.114.199.\*
>
> Newly discovered devices for the added subnet should appear in the
> list. See example below:

Any nodes that are swapping or suffering from disk fill need to be
replaced via theswagger API at https://zen.mon.ctl.io/docs

#### requires operator intervention as it will almost certainly not clear itself.

#### HOWTO: find a rogue z-node sending alerts for devices already set to maintenance mode (prodstate=300)

The objective is to look for lines coming from the same znode but with
different prod states. The lines should be close (in terms of lastTime).

Given this sample event:

Device: ca2t3nkms02

Component:

Severity: 5

Time: 2017/02/21 16:11:15.000

Message:

ca2t3nkms02 is DOWN!

== Additional Information ==

Hostname: ca2t3nkms02

IP address: 172.17.1.21

Device class: /Server/Microsoft/Windows/T3N/T3NKMS/SNMP

Event class: /Status/Ping

Data Center: /CA2

Proxy URL:
https://zen.mon.ctl.io/zport/dmd/Devices/Server/Microsoft/Windows/T3N/T3NKMS/SNMP/devices/ca2t3nkms02/devicedetail\#deviceDetailNav:device\_overview

Steps to look in Kibana:

1.  Select under index "\[ie\_zenoss-\][YYYY.MM](http://yyyy.mm/).DD"

2.  Add filters. e.g.

    -   header.messageType: "zenossEvent"

    -   zenossEvent.device: "ca2t3nkms02"

    -   zenossEvent.eventProperties.eventClass: "/Status/Ping"

3.  You may select columns for summarised view of results: 

    -   zenossEvent.eventProperties.originalTime

    -   hostname

    -   zenossEvent.eventProperties.productionState

    -   zenossEvent.eventProperties.lastTime

4.  You can check from the zenossEvent.eventProperties.lastTime column
    for the nearest matching time of the event. NOTE: lastTime is in
    UTC+8.

Sample in
Kibana: <https://kibana-cascadeo.analytics.ctl.io/goto/ec274b60daeaf8f79741b8667982a8ab>

**Note owner:** Prem R. Date : 09/25-26: 8pm-4am PDT Added by : NOC
Hieve Validity : indefinite Client : CTL NOTE: From Prem: If you find
broken screenshots of Kibana graph (Error serving file.), just ask T2 to
check. The problem is on slack's end and not ours.

**HOWTO: Check how long a node has been lingering in some state**

> Go to the provisioner of the node.
>
> \[root@CA2R82ZGPPROVISIONER \~\]\# redis-cli hget CA2R82ZGPZNODE06
> state\_time\
> "1488922268.386704"
>
> \[root@CA2R82ZGPPROVISIONER \~\]\# date -d @1483697608\
> Fri Jan 6 10:13:28 UTC 2017
>
> \[root@CA2R82ZGPPROVISIONER \~\]\# redis-cli hget
> CA2R82ZGPZNODE06 state\
> "SEEDING"
>
> In this example, it shows that CA2R82ZGPZNODE06 is switch to SEEDING
> state at 10:13pm. If it is stuck for 30 min, then reseed node.

#### PROBLEM: Get devices does not return device after adding device in zen.mon.ctl.io

<http://zen.mon.ctl.io> does not are not updated in real-time. A device
will only be added once a znode is actively monitoring the device. 

If an error such as this occurs: "message": "Warning: Unable to update
znodes. Changes will be applied to znodes in few minutes.", the device
has been saved in the manifest, but not in the znode. This can happen if
at the time of adding, the znode is being replaced or provisioned.
Another possible reason is that Zope is down, but there is a periodic
task that monitors the manifest and adds the missing devices in the
node. 

To check if a device has been successfully added in the manifest, GET
 http://10.128.131.39:8080/api/devices/{DC}/{DEVICE}
