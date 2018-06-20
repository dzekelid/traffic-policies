---
swagger: "2.0"
x-collection-name: AWS Route 53
x-complete: 1
info:
  title: AWS Route 53 API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2013-04-01/trafficpolicy:
    post:
      summary: Create Traffic Policy
      description: Creates a traffic policy, which you use to create multiple DNS
        resource record sets forone domain name (such as example.com) or one subdomain
        name (such aswww.example.com).Send a POST request to the /2013-04-01/trafficpolicy
        resource. The request body must include a documentwith a CreateTrafficPolicyRequest
        element. The response includes theCreateTrafficPolicyResponse element, which
        contains information about the newtraffic policy.
      operationId: createtrafficpolicy
      x-api-path-slug: 20130401trafficpolicy-post
      parameters:
      - in: body
        name: Comment
        description: (Optional) Any comments that you want to include about the traffic
          policy
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: CreateTrafficPolicyRequest
        description: Root level tag for the CreateTrafficPolicyRequest parameters
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Document
        description: The definition of this traffic policy in JSON format
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Name
        description: The name of the traffic policy
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  /2013-04-01/trafficpolicyinstance:
    post:
      summary: Create Traffic Policy Instance
      description: Creates resource record sets in a specified hosted zone based on
        the settings in aspecified traffic policy version. In addition, CreateTrafficPolicyInstanceassociates
        the resource record sets with a specified domain name (such as example.com)
        orsubdomain name (such as www.example.com). Amazon Route 53 responds to DNS
        queries for the domain orsubdomain name by using the resource record sets
        that CreateTrafficPolicyInstancecreated.Send a POST request to the /2013-04-01/trafficpolicyinstance
        resource. The request body must include adocument with a CreateTrafficPolicyRequest
        element. The response returns theCreateTrafficPolicyInstanceResponse element,
        which contains information aboutthe traffic policy instance.
      operationId: createtrafficpolicyinstance
      x-api-path-slug: 20130401trafficpolicyinstance-post
      parameters:
      - in: body
        name: CreateTrafficPolicyInstanceRequest
        description: Root level tag for the CreateTrafficPolicyInstanceRequest parameters
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: HostedZoneId
        description: The ID of the hosted zone in which you want Amazon Route 53 to
          create resource record sets byusing the configuration in a traffic policy
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Name
        description: The domain name (such as example
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: TrafficPolicyId
        description: The ID of the traffic policy that you want to use to create resource
          record sets in thespecified hosted zone
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: TrafficPolicyVersion
        description: The version of the traffic policy that you want to use to create
          resource record setsin the specified hosted zone
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: TTL
        description: (Optional) The TTL that you want Amazon Route 53 to assign to
          all of the resource record setsthat it creates in the specified hosted zone
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  /2013-04-01/trafficpolicy/Id:
    post:
      summary: Create Traffic Policy Version
      description: Creates a new version of an existing traffic policy. When you create
        a new version of atraffic policy, you specify the ID of the traffic policy
        that you want to update and aJSON-formatted document that describes the new
        version. You use traffic policies to createmultiple DNS resource record sets
        for one domain name (such as example.com) or one subdomainname (such as www.example.com).
        You can create a maximum of 1000 versions of a traffic policy.If you reach
        the limit and need to create another version, you'll need to start a new trafficpolicy.Send
        a POST request to the /2013-04-01/trafficpolicy/ resource. The request body
        includes a document witha CreateTrafficPolicyVersionRequest element. The response
        returns theCreateTrafficPolicyVersionResponse element, which contains information
        aboutthe new version of the traffic policy.
      operationId: createtrafficpolicyversion
      x-api-path-slug: 20130401trafficpolicyid-post
      parameters:
      - in: body
        name: Comment
        description: The comment that you specified in the CreateTrafficPolicyVersion
          request,if any
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: CreateTrafficPolicyVersionRequest
        description: Root level tag for the CreateTrafficPolicyVersionRequest parameters
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Document
        description: The definition of this version of the traffic policy, in JSON
          format
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: Id
        description: The ID of the traffic policy for which you want to create a new
          version
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  /2013-04-01/trafficpolicy/Id/Version:
    delete:
      summary: Delete Traffic Policy
      description: Deletes a traffic policy.Send a DELETE request to the /Amazon Route
        53 APIversion/trafficpolicy resource.
      operationId: deletetrafficpolicy
      x-api-path-slug: 20130401trafficpolicyidversion-delete
      parameters:
      - in: path
        name: Id
        description: The ID of the traffic policy that you want to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
    get:
      summary: Get Traffic Policy
      description: Gets information about a specific traffic policy version.Send a
        GET request to the /Amazon Route 53 APIversion/trafficpolicy resource.
      operationId: gettrafficpolicy
      x-api-path-slug: 20130401trafficpolicyidversion-get
      parameters:
      - in: path
        name: Id
        description: The ID of the traffic policy that you want to get information
          about
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
    post:
      summary: Update Traffic Policy Comment
      description: Updates the comment for a specified traffic policy version.Send
        a POST request to the /2013-04-01/trafficpolicy/ resource.The request body
        must include a document with anUpdateTrafficPolicyCommentRequest element.
      operationId: updatetrafficpolicycomment
      x-api-path-slug: 20130401trafficpolicyidversion-post
      parameters:
      - in: body
        name: Comment
        description: The new comment for the specified traffic policy and version
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: Id
        description: The value of Id for the traffic policy for which you want to
          update thecomment
        type: string
      - in: body
        name: UpdateTrafficPolicyCommentRequest
        description: Root level tag for the UpdateTrafficPolicyCommentRequest parameters
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  /2013-04-01/trafficpolicyinstance/Id:
    delete:
      summary: Delete Traffic Policy Instance
      description: Deletes a traffic policy instance and all of the resource record
        sets that Amazon Route 53created when you created the instance.Send a DELETE
        request to the /Amazon Route 53 APIversion/trafficpolicy/traffic policy instance
        ID            resource.NoteIn the Amazon Route 53 console, traffic policy
        instances are known as policy records.
      operationId: deletetrafficpolicyinstance
      x-api-path-slug: 20130401trafficpolicyinstanceid-delete
      parameters:
      - in: path
        name: Id
        description: The ID of the traffic policy instance that you want to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
    get:
      summary: Get Traffic Policy Instance
      description: Gets information about a specified traffic policy instance.Send
        a GET request to the /Amazon Route 53 APIversion/trafficpolicyinstance resource.NoteAfter
        you submit a CreateTrafficPolicyInstance or anUpdateTrafficPolicyInstance
        request, there's a brief delay while Amazon Route 53creates the resource record
        sets that are specified in the traffic policy definition. Formore information,
        see the State response element.NoteIn the Amazon Route 53 console, traffic
        policy instances are known as policy records.
      operationId: gettrafficpolicyinstance
      x-api-path-slug: 20130401trafficpolicyinstanceid-get
      parameters:
      - in: path
        name: Id
        description: The ID of the traffic policy instance that you want to get information
          about
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
    post:
      summary: Update Traffic Policy Instance
      description: Updates the resource record sets in a specified hosted zone that
        were created based onthe settings in a specified traffic policy version.Send
        a POST request to the /2013-04-01/trafficpolicyinstance/traffic policy ID            resource.
        The request body must include a document with anUpdateTrafficPolicyInstanceRequest
        element.When you update a traffic policy instance, Amazon Route 53 continues
        to respond to DNS queriesfor the root resource record set name (such as example.com)
        while it replaces one group ofresource record sets with another. Amazon Route
        53 performs the following operations:Amazon Route 53 creates a new group of
        resource record sets based on the specified trafficpolicy. This is true regardless
        of how substantial the differences are between theexisting resource record
        sets and the new resource record sets. When all of the new resource record
        sets have been created, Amazon Route 53 starts to respondto DNS queries for
        the root resource record set name (such as example.com) by using thenew resource
        record sets.Amazon Route 53 deletes the old group of resource record sets
        that are associated with theroot resource record set name.
      operationId: updatetrafficpolicyinstance
      x-api-path-slug: 20130401trafficpolicyinstanceid-post
      parameters:
      - in: path
        name: Id
        description: The ID of the traffic policy instance that you want to update
        type: string
      - in: body
        name: TrafficPolicyId
        description: The ID of the traffic policy that you want Amazon Route 53 to
          use to update resource record setsfor the specified traffic policy instance
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: TrafficPolicyVersion
        description: The version of the traffic policy that you want Amazon Route
          53 to use to update resource recordsets for the specified traffic policy
          instance
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: TTL
        description: The TTL that you want Amazon Route 53 to assign to all of the
          updated resource recordsets
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: UpdateTrafficPolicyInstanceRequest
        description: Root level tag for the UpdateTrafficPolicyInstanceRequest parameters
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  /2013-04-01/trafficpolicyinstancecount:
    get:
      summary: Get Traffic Policy Instance Count
      description: Gets the number of traffic policy instances that are associated
        with the current AWSaccount.To get the number of traffic policy instances,
        send a GET request to the/2013-04-01/trafficpolicyinstancecount resource.
      operationId: gettrafficpolicyinstancecount
      x-api-path-slug: 20130401trafficpolicyinstancecount-get
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  /2013-04-01/trafficpolicies&amp;maxitems=MaxItems?trafficpolicyid=TrafficPolicyIdMarker:
    get:
      summary: List Traffic Policies
      description: 'Gets information about the latest version for every traffic policy
        that is associatedwith the current AWS account. Send a GET request to the
        /Amazon Route 53API version/trafficpolicy resource.Amazon Route 53 returns
        a maximum of 100 items in each response. If you have a lot of trafficpolicies,
        you can use the maxitems parameter to list them in groups of up to100.The
        response includes three values that help you navigate from one group ofmaxitems
        traffic policies to the next:             IsTruncated           If the value
        of IsTruncated in the response is true,there are more traffic policies associated
        with the current AWS account.If IsTruncated is false, this response includes
        the lasttraffic policy that is associated with the current account.             TrafficPolicyIdMarker           If
        IsTruncated is true,TrafficPolicyIdMarker is the ID of the first traffic policy
        in the nextgroup of MaxItems traffic policies. If you want to list more trafficpolicies,
        make another call to ListTrafficPolicies, and specify the value ofthe TrafficPolicyIdMarker
        element from the response in theTrafficPolicyIdMarker request parameter.If
        IsTruncated is false, theTrafficPolicyIdMarker element is omitted from the
        response.             MaxItems           The value that you specified for
        the MaxItems parameter in the requestthat produced the current response.'
      operationId: listtrafficpolicies
      x-api-path-slug: 20130401trafficpoliciesampmaxitemsmaxitemstrafficpolicyidtrafficpolicyidmarker-get
      parameters:
      - in: path
        name: maxitems
        description: (Optional) The maximum number of traffic policies to be included
          in the response bodyfor this request
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  ? /2013-04-01/trafficpolicyinstances?hostedzoneid=HostedZoneIdMarker&amp;maxitems=MaxItems&amp;trafficpolicyinstancename=TrafficPolicyInstanceNameMarker&amp;trafficpolicyinstancetype=TrafficPolicyInstanceTypeMarker
  : get:
      summary: List Traffic Policy Instances
      description: 'Gets information about the traffic policy instances that you created
        by using thecurrent AWS account.NoteAfter you submit an UpdateTrafficPolicyInstance
        request, there''s a briefdelay while Amazon Route 53 creates the resource
        record sets that are specified in the traffic policydefinition. For more information,
        see the State response element.Send a GET request to the /Amazon Route 53
        APIversion/trafficpolicyinstance resource.Amazon Route 53 returns a maximum
        of 100 items in each response. If you have a lot of trafficpolicy instances,
        you can use the MaxItems parameter to list them in groups of upto 100.The
        response includes five values that help you navigate from one group ofMaxItems
        traffic policy instances to the next:             IsTruncated           If
        the value of IsTruncated in the response is true,there are more traffic policy
        instances associated with the current AWSaccount.If IsTruncated is false,
        this response includes the lasttraffic policy instance that is associated
        with the current account.             MaxItems           The value that you
        specified for the MaxItems parameter in the requestthat produced the current
        response.                  HostedZoneIdMarker, TrafficPolicyInstanceNameMarker,
        and TrafficPolicyInstanceTypeMarker               If IsTruncated is true,
        these three values in theresponse represent the first traffic policy instance
        in the next group ofMaxItems traffic policy instances. To list more traffic
        policy instances,make another call to ListTrafficPolicyInstances, and specify
        these values inthe corresponding request parameters.If IsTruncated is false,
        all three elements are omittedfrom the response.'
      operationId: listtrafficpolicyinstances
      x-api-path-slug: 20130401trafficpolicyinstanceshostedzoneidhostedzoneidmarkerampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
      parameters:
      - in: path
        name: hostedzoneid
        description: For the first request to ListTrafficPolicyInstances, omit thisvalue
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  ? /2013-04-01/trafficpolicyinstances/hostedzone?id=HostedZoneId&amp;maxitems=MaxItems&amp;trafficpolicyinstancename=TrafficPolicyInstanceNameMarker&amp;trafficpolicyinstancetype=TrafficPolicyInstanceTypeMarker
  : get:
      summary: List Traffic Policy Instances By Hosted Zone
      description: 'Gets information about the traffic policy instances that you created
        in a specifiedhosted zone.NoteAfter you submit an UpdateTrafficPolicyInstance
        request, there''s a briefdelay while Amazon Route 53 creates the resource
        record sets that are specified in the traffic policydefinition. For more information,
        see the State response element.Send a GET request to the /Amazon Route 53
        APIversion/trafficpolicyinstance resource and include the ID of the hostedzone.Amazon
        Route 53 returns a maximum of 100 items in each response. If you have a lot
        of trafficpolicy instances, you can use the MaxItems parameter to list them
        in groups of upto 100.The response includes four values that help you navigate
        from one group ofMaxItems traffic policy instances to the next:             IsTruncated               If
        the value of IsTruncated in the response is true, there aremore traffic policy
        instances associated with the current AWS account.If IsTruncated is false,
        this response includes the lasttraffic policy instance that is associated
        with the current account.             MaxItems           The value that you
        specified for the MaxItems parameter in the requestthat produced the current
        response.                  TrafficPolicyInstanceNameMarker and TrafficPolicyInstanceTypeMarker               If
        IsTruncated is true, these two values in the responserepresent the first traffic
        policy instance in the next group of MaxItemstraffic policy instances. To
        list more traffic policy instances, make another call toListTrafficPolicyInstancesByHostedZone,
        and specify these values in thecorresponding request parameters.If IsTruncated
        is false, all three elements are omittedfrom the response.'
      operationId: listtrafficpolicyinstancesbyhostedzone
      x-api-path-slug: 20130401trafficpolicyinstanceshostedzoneidhostedzoneidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
      parameters:
      - in: path
        name: id
        description: The ID of the hosted zone for which you want to list traffic
          policyinstances
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  /2013-04-01/trafficpolicies/Id/versions&amp;maxitems=MaxItems?trafficpolicyversion=TrafficPolicyVersionMarker:
    get:
      summary: List Traffic Policy Versions
      description: 'Gets information about all of the versions for a specified traffic
        policy.Send a GET request to the /Amazon Route 53 APIversion/trafficpolicy
        resource and specify the ID of the traffic policyfor which you want to list
        versions.Amazon Route 53 returns a maximum of 100 items in each response.
        If you have a lot of trafficpolicies, you can use the maxitems parameter to
        list them in groups of up to100.The response includes three values that help
        you navigate from one group ofmaxitems traffic policies to the next:             IsTruncated           If
        the value of IsTruncated in the response is true,there are more traffic policy
        versions associated with the specified trafficpolicy.If IsTruncated is false,
        this response includes the lasttraffic policy version that is associated with
        the specified traffic policy.             TrafficPolicyVersionMarker           The
        ID of the next traffic policy version that is associated with the current
        AWSaccount. If you want to list more traffic policies, make another call toListTrafficPolicyVersions,
        and specify the value of theTrafficPolicyVersionMarker element in theTrafficPolicyVersionMarker
        request parameter.If IsTruncated is false, Amazon Route 53 omits theTrafficPolicyVersionMarker
        element from the response.             MaxItems           The value that you
        specified for the MaxItems parameter in the requestthat produced the current
        response.'
      operationId: listtrafficpolicyversions
      x-api-path-slug: 20130401trafficpoliciesidversionsampmaxitemsmaxitemstrafficpolicyversiontrafficpolicyversionmarker-get
      parameters:
      - in: path
        name: Id
        description: Specify the value of Id of the traffic policy for which you want
          to listall versions
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
  ? /2013-04-01/trafficpolicyinstances/trafficpolicy&amp;hostedzoneid=HostedZoneIdMarker?id=TrafficPolicyId&amp;maxitems=MaxItems&amp;trafficpolicyinstancename=TrafficPolicyInstanceNameMarker&amp;trafficpolicyinstancetype=TrafficPolicyInstanceTypeMarker&
  : get:
      summary: List Traffic Policy Instances By Policy
      description: 'Gets information about the traffic policy instances that you created
        by using a specifytraffic policy version.NoteAfter you submit a CreateTrafficPolicyInstance
        or anUpdateTrafficPolicyInstance request, there''s a brief delay while Amazon
        Route 53creates the resource record sets that are specified in the traffic
        policy definition. Formore information, see the State response element.Send
        a GET request to the /Route 53 APIversion/trafficpolicyinstance resource and
        include the ID and version ofthe traffic policy.Amazon Route 53 returns a
        maximum of 100 items in each response. If you have a lot of trafficpolicy
        instances, you can use the MaxItems parameter to list them in groups of upto
        100.The response includes five values that help you navigate from one group
        ofMaxItems traffic policy instances to the next:             IsTruncated               If
        the value of IsTruncated in the response is true,there are more traffic policy
        instances associated with the specified trafficpolicy.If IsTruncated is false,
        this response includes the lasttraffic policy instance that is associated
        with the specified traffic policy.             MaxItems               The
        value that you specified for the MaxItems parameter in the requestthat produced
        the current response.                  HostedZoneIdMarker, TrafficPolicyInstanceNameMarker,
        and TrafficPolicyInstanceTypeMarker               If IsTruncated is true,
        these values in the responserepresent the first traffic policy instance in
        the next group of MaxItemstraffic policy instances. To list more traffic policy
        instances, make another call toListTrafficPolicyInstancesByPolicy, and specify
        these values in thecorresponding request parameters.If IsTruncated is false,
        all three elements are omittedfrom the response.'
      operationId: listtrafficpolicyinstancesbypolicy
      x-api-path-slug: 20130401trafficpolicyinstancestrafficpolicyamphostedzoneidhostedzoneidmarkeridtrafficpolicyidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
      parameters:
      - in: query
        name: CapacityId
        description: The ID that identifies the provisioned capacity unit
        type: string
      - in: query
        name: ExpirationDate
        description: The date that the provisioned capacity unit expires, in Coordinated                            Universal
          Time (UTC)
        type: string
      - in: path
        name: hostedzoneid
        description: For the first request to ListTrafficPolicyInstancesByPolicy,
          omit thisvalue
        type: string
      - in: query
        name: StartDate
        description: The date that the provisioned capacity unit was purchased, in
          Coordinated                            Universal Time (UTC)
        type: string
      - in: query
        name: TagKeys
        description: A list of tag keys
        type: string
      - in: query
        name: Tags
        description: The tags attached to the vault
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
---