# AWS::WAFv2::RuleGroup StatementThree<a name="aws-properties-wafv2-rulegroup-statementthree"></a>

Rules statement\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-statementthree-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-statementthree-syntax.json"></a>

```
{
  "[ByteMatchStatement](#cfn-wafv2-rulegroup-statementthree-bytematchstatement)" : ByteMatchStatement,
  "[GeoMatchStatement](#cfn-wafv2-rulegroup-statementthree-geomatchstatement)" : GeoMatchStatement,
  "[IPSetReferenceStatement](#cfn-wafv2-rulegroup-statementthree-ipsetreferencestatement)" : IPSetReferenceStatement,
  "[LabelMatchStatement](#cfn-wafv2-rulegroup-statementthree-labelmatchstatement)" : LabelMatchStatement,
  "[RegexPatternSetReferenceStatement](#cfn-wafv2-rulegroup-statementthree-regexpatternsetreferencestatement)" : RegexPatternSetReferenceStatement,
  "[SizeConstraintStatement](#cfn-wafv2-rulegroup-statementthree-sizeconstraintstatement)" : SizeConstraintStatement,
  "[SqliMatchStatement](#cfn-wafv2-rulegroup-statementthree-sqlimatchstatement)" : SqliMatchStatement,
  "[XssMatchStatement](#cfn-wafv2-rulegroup-statementthree-xssmatchstatement)" : XssMatchStatement
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-statementthree-syntax.yaml"></a>

```
  [ByteMatchStatement](#cfn-wafv2-rulegroup-statementthree-bytematchstatement): 
    ByteMatchStatement
  [GeoMatchStatement](#cfn-wafv2-rulegroup-statementthree-geomatchstatement): 
    GeoMatchStatement
  [IPSetReferenceStatement](#cfn-wafv2-rulegroup-statementthree-ipsetreferencestatement): 
    IPSetReferenceStatement
  [LabelMatchStatement](#cfn-wafv2-rulegroup-statementthree-labelmatchstatement): 
    LabelMatchStatement
  [RegexPatternSetReferenceStatement](#cfn-wafv2-rulegroup-statementthree-regexpatternsetreferencestatement): 
    RegexPatternSetReferenceStatement
  [SizeConstraintStatement](#cfn-wafv2-rulegroup-statementthree-sizeconstraintstatement): 
    SizeConstraintStatement
  [SqliMatchStatement](#cfn-wafv2-rulegroup-statementthree-sqlimatchstatement): 
    SqliMatchStatement
  [XssMatchStatement](#cfn-wafv2-rulegroup-statementthree-xssmatchstatement): 
    XssMatchStatement
```

## Properties<a name="aws-properties-wafv2-rulegroup-statementthree-properties"></a>

`ByteMatchStatement`  <a name="cfn-wafv2-rulegroup-statementthree-bytematchstatement"></a>
A rule statement that defines a string match search for AWS WAF to apply to web requests\. The byte match statement provides the bytes to search for, the location in requests that you want AWS WAF to search, and other settings\. The bytes to search for are typically a string that corresponds with ASCII characters\. In the AWS WAF console and the developer guide, this is refered to as a string match statement\.  
*Required*: No  
*Type*: [ByteMatchStatement](aws-properties-wafv2-rulegroup-bytematchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeoMatchStatement`  <a name="cfn-wafv2-rulegroup-statementthree-geomatchstatement"></a>
Statement used to identify web requests based on country of origin\.  
*Required*: No  
*Type*: [GeoMatchStatement](aws-properties-wafv2-rulegroup-geomatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IPSetReferenceStatement`  <a name="cfn-wafv2-rulegroup-statementthree-ipsetreferencestatement"></a>
Statement that references a set of IP addresses to compare to incoming requests\.   
*Required*: No  
*Type*: [IPSetReferenceStatement](aws-properties-wafv2-rulegroup-ipsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelMatchStatement`  <a name="cfn-wafv2-rulegroup-statementthree-labelmatchstatement"></a>
A rule statement that defines a string match search against labels that have been added to the web request by rules that have already run in the web ACL\.   
The label match statement provides the label or namespace string to search for\. The label string can represent a part or all of the fully qualified label name that had been added to the web request\. Fully qualified labels have a prefix, optional namespaces, and label name\. The prefix identifies the rule group or web ACL context of the rule that added the label\. If you do not provide the fully qualified name in your label match string, AWS WAF performs the search for labels that were added in the same context as the label match statement\.   
*Required*: No  
*Type*: [LabelMatchStatement](aws-properties-wafv2-rulegroup-labelmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegexPatternSetReferenceStatement`  <a name="cfn-wafv2-rulegroup-statementthree-regexpatternsetreferencestatement"></a>
A rule statement used to search web request components for matches with regular expressions\. To use this, create a RegexPatternSet with the expressions that you want to detect, then use that set in this statement\. A web request matches the pattern set rule statement if the request component matches any of the patterns in the set\.  
*Required*: No  
*Type*: [RegexPatternSetReferenceStatement](aws-properties-wafv2-rulegroup-regexpatternsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeConstraintStatement`  <a name="cfn-wafv2-rulegroup-statementthree-sizeconstraintstatement"></a>
A rule statement that compares a number of bytes against the size of a request component, using a comparison operator, such as greater than or less than\. For example, you can use a size constraint statement to look for query strings that are longer than 100 bytes\.  
If you configure AWS WAF to inspect the request body, AWS WAF inspects only the first 8192 bytes \(8 KB\)\. If the request body for your web requests never exceeds 8192 bytes, you can create a size constraint condition and block requests that have a request body greater than 8192 bytes\.  
If you choose URI for the value of Part of the request to filter on, the slash \(/\) in the URI counts as one character\. For example, the URI /logo\.jpg is nine characters long\.  
*Required*: No  
*Type*: [SizeConstraintStatement](aws-properties-wafv2-rulegroup-sizeconstraintstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqliMatchStatement`  <a name="cfn-wafv2-rulegroup-statementthree-sqlimatchstatement"></a>
Attackers sometimes insert malicious SQL code into web requests in an effort to extract data from your database\. To allow or block web requests that appear to contain malicious SQL code, create one or more SQL injection match conditions\. An SQL injection match condition identifies the part of web requests, such as the URI or the query string, that you want AWS WAF to inspect\. Later in the process, when you create a web ACL, you specify whether to allow or block requests that appear to contain malicious SQL code\.  
*Required*: No  
*Type*: [SqliMatchStatement](aws-properties-wafv2-rulegroup-sqlimatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XssMatchStatement`  <a name="cfn-wafv2-rulegroup-statementthree-xssmatchstatement"></a>
A rule statement that defines a cross\-site scripting \(XSS\) match search for AWS WAF to apply to web requests\. XSS attacks are those where the attacker uses vulnerabilities in a benign website as a vehicle to inject malicious client\-site scripts into other legitimate web browsers\. The XSS match statement provides the location in requests that you want AWS WAF to search and text transformations to use on the search area before AWS WAF searches for character sequences that are likely to be malicious strings\.  
*Required*: No  
*Type*: [XssMatchStatement](aws-properties-wafv2-rulegroup-xssmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)