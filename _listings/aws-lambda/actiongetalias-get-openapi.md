---
swagger: "2.0"
x-collection-name: AWS Lambda
x-complete: 0
info:
  title: AWS Lambda API Get Alias
  version: 1.0.0
  description: "Returns the specified alias information such as the alias ARN, description,
    and function version it \n      is pointing to."
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AddPermission:
    get:
      summary: Add Permission
      description: Adds a permission to the resource policy associated with the specified
        AWS Lambda function.
      operationId: addPermission
      x-api-path-slug: actionaddpermission-get
      parameters:
      - in: query
        name: FunctionName
        description: Name of the Lambda function whose resource policy you are updating
          by adding a new permission
        type: string
      - in: query
        name: Qualifier
        description: You can use this optional query parameter to describe a qualified
          ARN using a function version or an alias name
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /?Action=CreateAlias:
    get:
      summary: Create Alias
      description: Creates an alias that points to the specified Lambda function version.
      operationId: createAlias
      x-api-path-slug: actioncreatealias-get
      parameters:
      - in: query
        name: FunctionName
        description: Name of the Lambda function for which you want to create an alias
        type: string
      responses:
        200:
          description: OK
      tags:
      - Aliases
  /?Action=CreateEventSourceMapping:
    get:
      summary: Create Event Source Mapping
      description: Identifies a stream as an event source for a Lambda function.
      operationId: createEventSourceMapping
      x-api-path-slug: actioncreateeventsourcemapping-get
      parameters:
      - in: query
        name: BatchSize
        description: The largest number of records that AWS Lambda will retrieve from
          your event source at the time of invoking your function
        type: string
      - in: query
        name: Enabled
        description: Indicates whether AWS Lambda should begin polling the event source
        type: string
      - in: query
        name: EventSourceArn
        description: The Amazon Resource Name (ARN) of the Amazon Kinesis or the Amazon
          DynamoDB stream that is the event source
        type: string
      - in: query
        name: FunctionName
        description: The Lambda function to invoke when AWS Lambda detects an event
          on the stream
        type: string
      - in: query
        name: StartingPosition
        description: The position in the stream where AWS Lambda should start reading
        type: string
      - in: query
        name: StartingPositionTimestamp
        description: The timestamp of the data record from which to start reading
        type: string
      responses:
        200:
          description: OK
      tags:
      - Event Sources
  /?Action=CreateFunction:
    get:
      summary: Create Function
      description: Creates a new Lambda function.
      operationId: createFunction
      x-api-path-slug: actioncreatefunction-get
      parameters:
      - in: query
        name: Code
        description: The code for the Lambda function
        type: string
      - in: query
        name: DeadLetterConfig
        description: The parent object that contains the target Amazon Resource Name
          (ARN) of an Amazon SQS queue or Amazon SNS topic
        type: string
      - in: query
        name: Description
        description: A short, user-defined function description
        type: string
      - in: query
        name: Environment
        description: The parent object that contains your environments configuration
          settings
        type: string
      - in: query
        name: FunctionName
        description: The name you want to assign to the function you are uploading
        type: string
      - in: query
        name: Handler
        description: The function within your code that Lambda calls to begin execution
        type: string
      - in: query
        name: KMSKeyArn
        description: The Amazon Resource Name (ARN) of the KMS key used to encrypt
          your functions environment variables
        type: string
      - in: query
        name: MemorySize
        description: The amount of memory, in MB, your Lambda function is given
        type: string
      - in: query
        name: Publish
        description: This boolean parameter can be used to request AWS Lambda to create
          the Lambda function and publish a version as an atomic operation
        type: string
      - in: query
        name: Role
        description: The Amazon Resource Name (ARN) of the IAM role that Lambda assumes       when
          it executes your function to access any other Amazon Web Services (AWS)
          resources
        type: string
      - in: query
        name: Runtime
        description: The runtime environment for the Lambda function you are uploading
        type: string
      - in: query
        name: Timeout
        description: The function execution time at which Lambda should terminate
          the function
        type: string
      - in: query
        name: VpcConfig
        description: If your Lambda function accesses resources in a VPC, you provide
          this parameter identifying the list of security group IDs and subnet IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Functions
  /?Action=DeleteAlias:
    get:
      summary: Delete Alias
      description: Deletes the specified Lambda function alias.
      operationId: deleteAlias
      x-api-path-slug: actiondeletealias-get
      parameters:
      - in: query
        name: FunctionName
        description: The Lambda function name for which the alias is created
        type: string
      - in: query
        name: Name
        description: Name of the alias to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Aliases
  /?Action=DeleteEventSourceMapping:
    get:
      summary: Delete Event Source Mapping
      description: Removes an event source mapping.
      operationId: deleteEventSourceMapping
      x-api-path-slug: actiondeleteeventsourcemapping-get
      parameters:
      - in: query
        name: UUID
        description: The event source mapping ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Event Sources
  /?Action=DeleteFunction:
    get:
      summary: Delete Function
      description: Deletes the specified Lambda function code and configuration.
      operationId: deleteFunction
      x-api-path-slug: actiondeletefunction-get
      parameters:
      - in: query
        name: FunctionName
        description: The Lambda function to delete
        type: string
      - in: query
        name: Qualifier
        description: Using this optional parameter you can specify a function version       (but
          not the $LATEST version) to direct AWS Lambda to delete a       specific
          function version
        type: string
      responses:
        200:
          description: OK
      tags:
      - Functions
  /?Action=GetAccountSettings:
    get:
      summary: Get Account Settings
      description: Returns a customer's account settings.
      operationId: getAccountSettings
      x-api-path-slug: actiongetaccountsettings-get
      parameters:
      - in: query
        name: AccountLimit
        description: Provides limits of code size and concurrency associated with
          the current account and region
        type: string
      - in: query
        name: AccountUsage
        description: Provides code size usage and function count associated with the
          current account and region
        type: string
      responses:
        200:
          description: OK
      tags:
      - Accounts
  /?Action=GetAlias:
    get:
      summary: Get Alias
      description: "Returns the specified alias information such as the alias ARN,
        description, and function version it \n      is pointing to."
      operationId: getAlias
      x-api-path-slug: actiongetalias-get
      parameters:
      - in: query
        name: FunctionName
        description: Function name for which the alias is created
        type: string
      - in: query
        name: Name
        description: Name of the alias for which you want to retrieve information
        type: string
      responses:
        200:
          description: OK
      tags:
      - Aliases
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---