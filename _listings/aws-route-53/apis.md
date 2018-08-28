---
name: AWS Route 53
x-slug: aws-route-53
description: Amazon Route 53 is a highly available and scalable cloud Domain Name
  System (DNS) web service. It is designed to give developers and businesses an extremely
  reliable and cost effective way to route end users to Internet applications by translating
  names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers
  use to connect to each other. Amazon Route 53 is fully compliant with IPv6 as well.Amazon
  Route 53 effectively connects user requests to infrastructure running in AWS &ndash;
  such as Amazon EC2 instances, Elastic Load Balancing load balancers, or Amazon S3
  buckets &ndash; and can also be used to route users to infrastructure outside of
  AWS. You can use Amazon Route 53 to configure DNS health checks to route traffic
  to healthy endpoints or to independently monitor the health of your application
  and its endpoints. Amazon Route 53 Traffic Flow makes it easy for you to manage
  traffic globally through a variety of routing types, including Latency Based Routing,
  Geo DNS, and Weighted Round Robin&mdash;all of which can be combined with DNS Failover
  in order to enable a variety of low-latency, fault-tolerant architectures. Using
  Amazon Route 53 Traffic Flow&rsquo;s simple visual editor, you can easily manage
  how your end-users are routed to your application&rsquo;s endpoints&mdash;whether
  in a single AWS region or distributed around the globe. Amazon Route 53 also offers
  Domain Name Registration &ndash; you can purchase and manage domain names such as
  example.com and Amazon Route 53 will automatically configure DNS settings for your
  domains.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Traffic Policies
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/apis.md
specificationVersion: "0.14"
apis:
- name: AWS Route 53 API - Create Traffic Policy
  x-api-slug: 20130401trafficpolicy-post
  description: Creates a traffic policy, which you use to create multiple DNS resource
    record sets forone domain name (such as example.com) or one subdomain name (such
    aswww.example.com).Send a POST request to the /2013-04-01/trafficpolicy resource.
    The request body must include a documentwith a CreateTrafficPolicyRequest element.
    The response includes theCreateTrafficPolicyResponse element, which contains information
    about the newtraffic policy.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicy-post-openapi.md
- name: AWS Route 53 API - Create Traffic Policy Instance
  x-api-slug: 20130401trafficpolicyinstance-post
  description: Creates resource record sets in a specified hosted zone based on the
    settings in aspecified traffic policy version. In addition, CreateTrafficPolicyInstanceassociates
    the resource record sets with a specified domain name (such as example.com) orsubdomain
    name (such as www.example.com). Amazon Route 53 responds to DNS queries for the
    domain orsubdomain name by using the resource record sets that CreateTrafficPolicyInstancecreated.Send
    a POST request to the /2013-04-01/trafficpolicyinstance resource. The request
    body must include adocument with a CreateTrafficPolicyRequest element. The response
    returns theCreateTrafficPolicyInstanceResponse element, which contains information
    aboutthe traffic policy instance.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyinstance-post-openapi.md
- name: AWS Route 53 API - Create Traffic Policy Version
  x-api-slug: 20130401trafficpolicyid-post
  description: Creates a new version of an existing traffic policy. When you create
    a new version of atraffic policy, you specify the ID of the traffic policy that
    you want to update and aJSON-formatted document that describes the new version.
    You use traffic policies to createmultiple DNS resource record sets for one domain
    name (such as example.com) or one subdomainname (such as www.example.com). You
    can create a maximum of 1000 versions of a traffic policy.If you reach the limit
    and need to create another version, you'll need to start a new trafficpolicy.Send
    a POST request to the /2013-04-01/trafficpolicy/ resource. The request body includes
    a document witha CreateTrafficPolicyVersionRequest element. The response returns
    theCreateTrafficPolicyVersionResponse element, which contains information aboutthe
    new version of the traffic policy.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyid-post-openapi.md
- name: AWS Route 53 API - Delete Traffic Policy
  x-api-slug: 20130401trafficpolicyidversion-delete
  description: Deletes a traffic policy.Send a DELETE request to the /Amazon Route
    53 APIversion/trafficpolicy resource.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyidversion-delete-openapi.md
- name: AWS Route 53 API - Delete Traffic Policy Instance
  x-api-slug: 20130401trafficpolicyinstanceid-delete
  description: Deletes a traffic policy instance and all of the resource record sets
    that Amazon Route 53created when you created the instance.Send a DELETE request
    to the /Amazon Route 53 APIversion/trafficpolicy/traffic policy instance ID            resource.NoteIn
    the Amazon Route 53 console, traffic policy instances are known as policy records.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyinstanceid-delete-openapi.md
- name: AWS Route 53 API - Get Traffic Policy
  x-api-slug: 20130401trafficpolicyidversion-get
  description: Gets information about a specific traffic policy version.Send a GET
    request to the /Amazon Route 53 APIversion/trafficpolicy resource.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyidversion-get-openapi.md
- name: AWS Route 53 API - Get Traffic Policy Instance
  x-api-slug: 20130401trafficpolicyinstanceid-get
  description: Gets information about a specified traffic policy instance.Send a GET
    request to the /Amazon Route 53 APIversion/trafficpolicyinstance resource.NoteAfter
    you submit a CreateTrafficPolicyInstance or anUpdateTrafficPolicyInstance request,
    there's a brief delay while Amazon Route 53creates the resource record sets that
    are specified in the traffic policy definition. Formore information, see the State
    response element.NoteIn the Amazon Route 53 console, traffic policy instances
    are known as policy records.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyinstanceid-get-openapi.md
- name: AWS Route 53 API - Get Traffic Policy Instance Count
  x-api-slug: 20130401trafficpolicyinstancecount-get
  description: Gets the number of traffic policy instances that are associated with
    the current AWSaccount.To get the number of traffic policy instances, send a GET
    request to the/2013-04-01/trafficpolicyinstancecount resource.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyinstancecount-get-openapi.md
- name: AWS Route 53 API - List Traffic Policies
  x-api-slug: 20130401trafficpoliciesampmaxitemsmaxitemstrafficpolicyidtrafficpolicyidmarker-get
  description: 'Gets information about the latest version for every traffic policy
    that is associatedwith the current AWS account. Send a GET request to the /Amazon
    Route 53API version/trafficpolicy resource.Amazon Route 53 returns a maximum of
    100 items in each response. If you have a lot of trafficpolicies, you can use
    the maxitems parameter to list them in groups of up to100.The response includes
    three values that help you navigate from one group ofmaxitems traffic policies
    to the next:             IsTruncated           If the value of IsTruncated in
    the response is true,there are more traffic policies associated with the current
    AWS account.If IsTruncated is false, this response includes the lasttraffic policy
    that is associated with the current account.             TrafficPolicyIdMarker           If
    IsTruncated is true,TrafficPolicyIdMarker is the ID of the first traffic policy
    in the nextgroup of MaxItems traffic policies. If you want to list more trafficpolicies,
    make another call to ListTrafficPolicies, and specify the value ofthe TrafficPolicyIdMarker
    element from the response in theTrafficPolicyIdMarker request parameter.If IsTruncated
    is false, theTrafficPolicyIdMarker element is omitted from the response.             MaxItems           The
    value that you specified for the MaxItems parameter in the requestthat produced
    the current response.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpoliciesampmaxitemsmaxitemstrafficpolicyidtrafficpolicyidmarker-get-openapi.md
- name: AWS Route 53 API - List Traffic Policy Instances
  x-api-slug: 20130401trafficpolicyinstanceshostedzoneidhostedzoneidmarkerampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
  description: 'Gets information about the traffic policy instances that you created
    by using thecurrent AWS account.NoteAfter you submit an UpdateTrafficPolicyInstance
    request, there''s a briefdelay while Amazon Route 53 creates the resource record
    sets that are specified in the traffic policydefinition. For more information,
    see the State response element.Send a GET request to the /Amazon Route 53 APIversion/trafficpolicyinstance
    resource.Amazon Route 53 returns a maximum of 100 items in each response. If you
    have a lot of trafficpolicy instances, you can use the MaxItems parameter to list
    them in groups of upto 100.The response includes five values that help you navigate
    from one group ofMaxItems traffic policy instances to the next:             IsTruncated           If
    the value of IsTruncated in the response is true,there are more traffic policy
    instances associated with the current AWSaccount.If IsTruncated is false, this
    response includes the lasttraffic policy instance that is associated with the
    current account.             MaxItems           The value that you specified for
    the MaxItems parameter in the requestthat produced the current response.                  HostedZoneIdMarker,
    TrafficPolicyInstanceNameMarker, and TrafficPolicyInstanceTypeMarker               If
    IsTruncated is true, these three values in theresponse represent the first traffic
    policy instance in the next group ofMaxItems traffic policy instances. To list
    more traffic policy instances,make another call to ListTrafficPolicyInstances,
    and specify these values inthe corresponding request parameters.If IsTruncated
    is false, all three elements are omittedfrom the response.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyinstanceshostedzoneidhostedzoneidmarkerampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get-openapi.md
- name: AWS Route 53 API - List Traffic Policy Instances By Hosted Zone
  x-api-slug: 20130401trafficpolicyinstanceshostedzoneidhostedzoneidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
  description: 'Gets information about the traffic policy instances that you created
    in a specifiedhosted zone.NoteAfter you submit an UpdateTrafficPolicyInstance
    request, there''s a briefdelay while Amazon Route 53 creates the resource record
    sets that are specified in the traffic policydefinition. For more information,
    see the State response element.Send a GET request to the /Amazon Route 53 APIversion/trafficpolicyinstance
    resource and include the ID of the hostedzone.Amazon Route 53 returns a maximum
    of 100 items in each response. If you have a lot of trafficpolicy instances, you
    can use the MaxItems parameter to list them in groups of upto 100.The response
    includes four values that help you navigate from one group ofMaxItems traffic
    policy instances to the next:             IsTruncated               If the value
    of IsTruncated in the response is true, there aremore traffic policy instances
    associated with the current AWS account.If IsTruncated is false, this response
    includes the lasttraffic policy instance that is associated with the current account.             MaxItems           The
    value that you specified for the MaxItems parameter in the requestthat produced
    the current response.                  TrafficPolicyInstanceNameMarker and TrafficPolicyInstanceTypeMarker               If
    IsTruncated is true, these two values in the responserepresent the first traffic
    policy instance in the next group of MaxItemstraffic policy instances. To list
    more traffic policy instances, make another call toListTrafficPolicyInstancesByHostedZone,
    and specify these values in thecorresponding request parameters.If IsTruncated
    is false, all three elements are omittedfrom the response.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyinstanceshostedzoneidhostedzoneidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get-openapi.md
- name: AWS Route 53 API - List Traffic Policy Versions
  x-api-slug: 20130401trafficpoliciesidversionsampmaxitemsmaxitemstrafficpolicyversiontrafficpolicyversionmarker-get
  description: 'Gets information about all of the versions for a specified traffic
    policy.Send a GET request to the /Amazon Route 53 APIversion/trafficpolicy resource
    and specify the ID of the traffic policyfor which you want to list versions.Amazon
    Route 53 returns a maximum of 100 items in each response. If you have a lot of
    trafficpolicies, you can use the maxitems parameter to list them in groups of
    up to100.The response includes three values that help you navigate from one group
    ofmaxitems traffic policies to the next:             IsTruncated           If
    the value of IsTruncated in the response is true,there are more traffic policy
    versions associated with the specified trafficpolicy.If IsTruncated is false,
    this response includes the lasttraffic policy version that is associated with
    the specified traffic policy.             TrafficPolicyVersionMarker           The
    ID of the next traffic policy version that is associated with the current AWSaccount.
    If you want to list more traffic policies, make another call toListTrafficPolicyVersions,
    and specify the value of theTrafficPolicyVersionMarker element in theTrafficPolicyVersionMarker
    request parameter.If IsTruncated is false, Amazon Route 53 omits theTrafficPolicyVersionMarker
    element from the response.             MaxItems           The value that you specified
    for the MaxItems parameter in the requestthat produced the current response.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpoliciesidversionsampmaxitemsmaxitemstrafficpolicyversiontrafficpolicyversionmarker-get-openapi.md
- name: AWS Route 53 API - Update Traffic Policy Comment
  x-api-slug: 20130401trafficpolicyidversion-post
  description: Updates the comment for a specified traffic policy version.Send a POST
    request to the /2013-04-01/trafficpolicy/ resource.The request body must include
    a document with anUpdateTrafficPolicyCommentRequest element.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyidversion-post-openapi.md
- name: AWS Route 53 API - Update Traffic Policy Instance
  x-api-slug: 20130401trafficpolicyinstanceid-post
  description: Updates the resource record sets in a specified hosted zone that were
    created based onthe settings in a specified traffic policy version.Send a POST
    request to the /2013-04-01/trafficpolicyinstance/traffic policy ID            resource.
    The request body must include a document with anUpdateTrafficPolicyInstanceRequest
    element.When you update a traffic policy instance, Amazon Route 53 continues to
    respond to DNS queriesfor the root resource record set name (such as example.com)
    while it replaces one group ofresource record sets with another. Amazon Route
    53 performs the following operations:Amazon Route 53 creates a new group of resource
    record sets based on the specified trafficpolicy. This is true regardless of how
    substantial the differences are between theexisting resource record sets and the
    new resource record sets. When all of the new resource record sets have been created,
    Amazon Route 53 starts to respondto DNS queries for the root resource record set
    name (such as example.com) by using thenew resource record sets.Amazon Route 53
    deletes the old group of resource record sets that are associated with theroot
    resource record set name.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyinstanceid-post-openapi.md
- name: AWS Route 53 API - List Traffic Policy Instances By Policy
  x-api-slug: 20130401trafficpolicyinstancestrafficpolicyamphostedzoneidhostedzoneidmarkeridtrafficpolicyidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
  description: 'Gets information about the traffic policy instances that you created
    by using a specifytraffic policy version.NoteAfter you submit a CreateTrafficPolicyInstance
    or anUpdateTrafficPolicyInstance request, there''s a brief delay while Amazon
    Route 53creates the resource record sets that are specified in the traffic policy
    definition. Formore information, see the State response element.Send a GET request
    to the /Route 53 APIversion/trafficpolicyinstance resource and include the ID
    and version ofthe traffic policy.Amazon Route 53 returns a maximum of 100 items
    in each response. If you have a lot of trafficpolicy instances, you can use the
    MaxItems parameter to list them in groups of upto 100.The response includes five
    values that help you navigate from one group ofMaxItems traffic policy instances
    to the next:             IsTruncated               If the value of IsTruncated
    in the response is true,there are more traffic policy instances associated with
    the specified trafficpolicy.If IsTruncated is false, this response includes the
    lasttraffic policy instance that is associated with the specified traffic policy.             MaxItems               The
    value that you specified for the MaxItems parameter in the requestthat produced
    the current response.                  HostedZoneIdMarker, TrafficPolicyInstanceNameMarker,
    and TrafficPolicyInstanceTypeMarker               If IsTruncated is true, these
    values in the responserepresent the first traffic policy instance in the next
    group of MaxItemstraffic policy instances. To list more traffic policy instances,
    make another call toListTrafficPolicyInstancesByPolicy, and specify these values
    in thecorresponding request parameters.If IsTruncated is false, all three elements
    are omittedfrom the response.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic-policies/master/_listings/aws-route-53/20130401trafficpolicyinstancestrafficpolicyamphostedzoneidhostedzoneidmarkeridtrafficpolicyidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://aws.rekognition.api.gallery.streamdata.io
- type: x-api-stack
  url: http://aws.route.53.stack.network
- type: x-documentation
  url: http://docs.aws.amazon.com/Route53/latest/APIReference/
- type: x-faq
  url: https://aws.amazon.com/route53/faqs/
- type: x-forum
  url: https://forums.aws.amazon.com/forum.jspa?forumID=87
- type: x-pricing
  url: https://aws.amazon.com/route53/pricing/
- type: x-registrar-policies
  url: https://aws.amazon.com/route53/amazon-registrar-policies/
- type: x-service-health
  url: http://status.aws.amazon.com/
- type: x-service-level-agreement
  url: https://aws.amazon.com/route53/sla
- type: x-sla
  url: https://aws.amazon.com/route53/sla/
- type: x-website
  url: https://aws.amazon.com/route53/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---